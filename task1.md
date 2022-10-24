
<pre>

[student@workstation ~]$ oc whoami
kube:admin
[student@workstation ~]$ sudo yum install httpd-tools
Last metadata expiration check: 0:07:46 ago on Mon 24 Oct 2022 08:09:27 AM EDT.
Package httpd-tools-2.4.37-21.module+el8.2.0+5008+cca404a3.x86_64 is already installed.
Dependencies resolved.
Nothing to do.
Complete!
[student@workstation ~]$ htpasswd -c -b -B /tmp/htpasswd-users admin redhat
Adding password for user admin
[student@workstation ~]$ htpasswd -b -B /tmp/htpasswd-users anouk redhat
Adding password for user anouk
[student@workstation ~]$ htpasswd -b -B /tmp/htpasswd-users developer redhat
Adding password for user developer
[student@workstation ~]$ htpasswd -b -B /tmp/htpasswd-users linda redhat
Adding password for user linda
[student@workstation ~]$ htpasswd -b -B /tmp/htpasswd-users lisa redhat
Adding password for user lisa
[student@workstation ~]$ cat /tmp/htpasswd-users 
admin:$2y$05$hGzH7m5WP1HyoYULdYwSXuLrXBPiTub4/lqwmpWbqNbAp/FKrp836
anouk:$2y$05$ROSipRsObga6OREwiKWfV.bdTENnt8S6Heu7NIui3i8Xdfb9DdR/u
developer:$2y$05$zg.jVPKTxSglLTEIVehDUeXUEabGhZfMw72f88oBwkBC6YWOc55um
linda:$2y$05$maZSOY5uk7wu8coX7rhscuhi45DE5/F4kDUQxyr4x1lXmNoSlnJuS
lisa:$2y$05$039X6pKWTNMUVmDledbxlOnS/VQvwg9BHfddHQu2gsCHDwxiSu8P2
[student@workstation ~]$ oc get oauth cluster -o yaml &gt; /tmp/oauth.yaml
[student@workstation ~]$ vi /tmp/oauth.yaml 
[student@workstation ~]$ oc create secret generic htpass-users --from-file htpasswd=/tmp/htpasswd-users -n openshift-config
secret/htpass-users created
[student@workstation ~]$ oc get nodes
NAME       STATUS   ROLES           AGE    VERSION
master01   Ready    master,worker   468d   v1.19.0+b00ba52
master02   Ready    master,worker   468d   v1.19.0+b00ba52
master03   Ready    master,worker   468d   v1.19.0+b00ba52
[student@workstation ~]$ oc replace -f /tmp/oauth.yaml 
oauth.config.openshift.io/cluster replaced
[student@workstation ~]$ oc get pods -n openshift-authentication
NAME                               READY   STATUS    RESTARTS   AGE
oauth-openshift-75d8555cd4-2smzx   1/1     Running   0          16m
oauth-openshift-75d8555cd4-hxclt   1/1     Running   0          14m
[student@workstation ~]$ oc get pods -n openshift-config
No resources found in openshift-config namespace.
[student@workstation ~]$ oc get oauth cluster -o yaml &gt; /tmp/oauth.yaml -n openshift-config
[student@workstation ~]$ vi /tmp/oauth.yaml 
[student@workstation ~]$ oc replace -f /tmp/oauth.yaml 
oauth.config.openshift.io/cluster replaced
[student@workstation ~]$ oc get secrets -n openshift-con
openshift-config                       openshift-console                      openshift-controller-manager-operator
openshift-config-managed               openshift-console-operator             
openshift-config-operator              openshift-controller-manager           
[student@workstation ~]$ oc get secrets -n openshift-config
NAME                                  TYPE                                  DATA   AGE
builder-dockercfg-f2fcd               kubernetes.io/dockercfg               1      468d
builder-token-gfj78                   kubernetes.io/service-account-token   4      468d
builder-token-vz4dm                   kubernetes.io/service-account-token   4      468d
classroom-tls                         kubernetes.io/tls                     2      467d
default-dockercfg-ctgjm               kubernetes.io/dockercfg               1      468d
default-token-bkv6c                   kubernetes.io/service-account-token   4      468d
default-token-hp4s4                   kubernetes.io/service-account-token   4      468d
deployer-dockercfg-7b8hr              kubernetes.io/dockercfg               1      468d
deployer-token-bnfvl                  kubernetes.io/service-account-token   4      468d
deployer-token-nztc7                  kubernetes.io/service-account-token   4      468d
etcd-client                           SecretTypeTLS                         2      468d
etcd-metric-client                    SecretTypeTLS                         2      468d
etcd-metric-signer                    SecretTypeTLS                         2      468d
etcd-signer                           SecretTypeTLS                         2      468d
htpass-users                          Opaque                                1      10m
htpasswd-secret                       Opaque                                1      467d
initial-service-account-private-key   Opaque                                1      468d
pull-secret                           kubernetes.io/dockerconfigjson        1      468d
[student@workstation ~]$ vi /tmp/oauth.yaml 
[student@workstation ~]$ oc login -u admin -p redhat
Login successful.

You have access to 59 projects, the list has been suppressed. You can list all projects with &apos; projects&apos;

Using project &quot;default&quot;.
[student@workstation ~]$ oc login -u linda -p redhat
Login failed (401 Unauthorized)
Verify you have provided correct credentials.
[student@workstation ~]$ oc get identifies
error: the server doesn&apos;t have a resource type &quot;identifies&quot;
[student@workstation ~]$ oc get identities
NAME                      IDP NAME            IDP USER NAME   USER NAME   USER UID
htpasswd_provider:admin   htpasswd_provider   admin           admin       0fd6231d-a13c-4e7a-9589-d0775028d4ed
[student@workstation ~]$ vi /tmp/oauth.yaml 
[student@workstation ~]$ oc replace -f /tmp/oauth.yaml
Error from server (Conflict): error when replacing &quot;/tmp/oauth.yaml&quot;: Operation cannot be fulfilled on oauths.config.openshift.io &quot;cluster&quot;: the object has been modified; please apply your changes to the latest version and try again
[student@workstation ~]$ oc apply -f /tmp/oauth.yaml
Error from server (Conflict): error when applying patch:
{&quot;metadata&quot;:{&quot;annotations&quot;:{&quot;kubectl.kubernetes.io/last-applied-configuration&quot;:&quot;{\&quot;apiVersion\&quot;:\&quot;config.openshift.io/v1\&quot;,\&quot;kind\&quot;:\&quot;OAuth\&quot;,\&quot;metadata\&quot;:{\&quot;annotations\&quot;:{\&quot;release.openshift.io/create-only\&quot;:\&quot;true\&quot;},\&quot;creationTimestamp\&quot;:\&quot;2021-07-13T12:14:15Z\&quot;,\&quot;generation\&quot;:3,\&quot;managedFields\&quot;:[{\&quot;apiVersion\&quot;:\&quot;config.openshift.io/v1\&quot;,\&quot;fieldsType\&quot;:\&quot;FieldsV1\&quot;,\&quot;fieldsV1\&quot;:{\&quot;f:metadata\&quot;:{\&quot;f:annotations\&quot;:{\&quot;.\&quot;:{},\&quot;f:release.openshift.io/create-only\&quot;:{}}},\&quot;f:spec\&quot;:{}},\&quot;manager\&quot;:\&quot;cluster-version-operator\&quot;,\&quot;operation\&quot;:\&quot;Update\&quot;,\&quot;time\&quot;:\&quot;2021-07-13T12:14:15Z\&quot;},{\&quot;apiVersion\&quot;:\&quot;config.openshift.io/v1\&quot;,\&quot;fieldsType\&quot;:\&quot;FieldsV1\&quot;,\&quot;fieldsV1\&quot;:{\&quot;f:metadata\&quot;:{\&quot;f:annotations\&quot;:{\&quot;f:kubectl.kubernetes.io/last-applied-configuration\&quot;:{}}},\&quot;f:spec\&quot;:{\&quot;f:identityProviders\&quot;:{}}},\&quot;manager\&quot;:\&quot;kubectl-replace\&quot;,\&quot;operation\&quot;:\&quot;Update\&quot;,\&quot;time\&quot;:\&quot;2022-10-24T12:25:53Z\&quot;}],\&quot;name\&quot;:\&quot;cluster\&quot;,\&quot;resourceVersion\&quot;:\&quot;72145\&quot;,\&quot;selfLink\&quot;:\&quot;/apis/config.openshift.io/v1/oauths/cluster\&quot;,\&quot;uid\&quot;:\&quot;c1d4f788-a51a-4e01-b162-d1bb686a2e14\&quot;},\&quot;spec\&quot;:{\&quot;identityProviders\&quot;:[{\&quot;htpasswd\&quot;:{\&quot;fileData\&quot;:{\&quot;name\&quot;:\&quot;htpass-users\&quot;}},\&quot;mappingMethod\&quot;:\&quot;claim\&quot;,\&quot;name\&quot;:\&quot;htpasswd-users\&quot;,\&quot;type\&quot;:\&quot;HTPasswd\&quot;}]}}\n&quot;},&quot;managedFields&quot;:[{&quot;apiVersion&quot;:&quot;config.openshift.io/v1&quot;,&quot;fieldsType&quot;:&quot;FieldsV1&quot;,&quot;fieldsV1&quot;:{&quot;f:metadata&quot;:{&quot;f:annotations&quot;:{&quot;.&quot;:{},&quot;f:release.openshift.io/create-only&quot;:{}}},&quot;f:spec&quot;:{}},&quot;manager&quot;:&quot;cluster-version-operator&quot;,&quot;operation&quot;:&quot;Update&quot;,&quot;time&quot;:&quot;2021-07-13T12:14:15Z&quot;},{&quot;apiVersion&quot;:&quot;config.openshift.io/v1&quot;,&quot;fieldsType&quot;:&quot;FieldsV1&quot;,&quot;fieldsV1&quot;:{&quot;f:metadata&quot;:{&quot;f:annotations&quot;:{&quot;f:kubectl.kubernetes.io/last-applied-configuration&quot;:{}}},&quot;f:spec&quot;:{&quot;f:identityProviders&quot;:{}}},&quot;manager&quot;:&quot;kubectl-replace&quot;,&quot;operation&quot;:&quot;Update&quot;,&quot;time&quot;:&quot;2022-10-24T12:25:53Z&quot;}],&quot;resourceVersion&quot;:&quot;72145&quot;},&quot;spec&quot;:{&quot;identityProviders&quot;:[{&quot;htpasswd&quot;:{&quot;fileData&quot;:{&quot;name&quot;:&quot;htpass-users&quot;}},&quot;mappingMethod&quot;:&quot;claim&quot;,&quot;name&quot;:&quot;htpasswd-users&quot;,&quot;type&quot;:&quot;HTPasswd&quot;}]}}
to:
Resource: &quot;config.openshift.io/v1, Resource=oauths&quot;, GroupVersionKind: &quot;config.openshift.io/v1, Kind=OAuth&quot;
Name: &quot;cluster&quot;, Namespace: &quot;&quot;
for: &quot;/tmp/oauth.yaml&quot;: Operation cannot be fulfilled on oauths.config.openshift.io &quot;cluster&quot;: the object has been modified; please apply your changes to the latest version and try again
[student@workstation ~]$ oc set data secret/htpasswd-secret \
&gt; --from-file htpasswd=/tmp/htpasswd-users -n openshift-config
secret/htpasswd-secret data updated
[student@workstation ~]$ oc login -u linda -p redhat
Login successful.

You don&apos;t have any projects. You can try to create a new project, by running

    oc new-project &lt;projectname&gt;

[student@workstation ~]$ oc adm policy -h
Manage policy on the cluster

 These commands allow you to assign and manage the roles and policies that apply to users. The reconcile commands allow
you to reset and upgrade your system policies to the latest default policies.

 To see more information on roles and policies, use the &apos;get&apos; and &apos;describe&apos; commands on the following resources:
&apos;clusterroles&apos;, &apos;clusterpolicy&apos;, &apos;clusterrolebindings&apos;, &apos;roles&apos;, &apos;policy&apos;, &apos;rolebindings&apos;, and &apos;scc&apos;.

Usage:
  oc adm policy [flags]

Discover:
  who-can                        List who can perform the specified action on a resource
  scc-subject-review             Check whether a user or a ServiceAccount can create a Pod.
  scc-review                     Checks which ServiceAccount can create a Pod

Manage project membership:
  remove-user                    Remove user from the current project
  remove-group                   Remove group from the current project

Assign roles to users and groups:
  add-role-to-user               Add a role to users or serviceaccounts for the current project
  add-role-to-group              Add a role to groups for the current project
  remove-role-from-user          Remove a role from users for the current project
  remove-role-from-group         Remove a role from groups for the current project

Assign cluster roles to users and groups:
  add-cluster-role-to-user       Add a role to users for all projects in the cluster
  add-cluster-role-to-group      Add a role to groups for all projects in the cluster
  remove-cluster-role-from-user  Remove a role from users for all projects in the cluster
  remove-cluster-role-from-group Remove a role from groups for all projects in the cluster

Manage policy on pods and containers:
  add-scc-to-user                Add security context constraint to users or a service account
  add-scc-to-group               Add security context constraint to groups
  remove-scc-from-user           Remove user from scc
  remove-scc-from-group          Remove group from scc

Use &quot;oc adm policy &lt;command&gt; --help&quot; for more information about a given command.
Use &quot;oc adm options&quot; for a list of global command-line options (applies to all commands).
[student@workstation ~]$ oc adm policy add-cluster-role-to-user cluster-admin admin
Error from server (Forbidden): clusterrolebindings.rbac.authorization.k8s.io is forbidden: User &quot;linda&quot; cannot list resource &quot;clusterrolebindings&quot; in API group &quot;rbac.authorization.k8s.io&quot; at the cluster scope
[student@workstation ~]$ oc login -u kubeadmin -p ${RHT_OCP4_KUBEADM_PASSWD}     https://api.ocp4.example.com:6443
Login successful.

You have access to 59 projects, the list has been suppressed. You can list all projects with &apos; projects&apos;

Using project &quot;default&quot;.
[student@workstation ~]$ oc adm policy add-cluster-role-to-user cluster-admin admin
clusterrole.rbac.authorization.k8s.io/cluster-admin added: &quot;admin&quot;
[student@workstation ~]$ oc login -u admin -p redhat
Login successful.

You have access to 59 projects, the list has been suppressed. You can list all projects with &apos; projects&apos;

Using project &quot;default&quot;.
[student@workstation ~]$ oc delete secrets kubeadmin -n kube-system
secret &quot;kubeadmin&quot; deleted
[student@workstation ~]$ oc adm groups new admins
group.user.openshift.io/admins created
[student@workstation ~]$ oc adm groups new developers
group.user.openshift.io/developers created
[student@workstation ~]$ oc adm groups new viewers
group.user.openshift.io/viewers created
[student@workstation ~]$ oc adm groups add-users admins admin
group.user.openshift.io/admins added: &quot;admin&quot;
[student@workstation ~]$ oc adm groups add-users admins anna
group.user.openshift.io/admins added: &quot;anna&quot;
[student@workstation ~]$ oc adm groups add-users developers linda 
group.user.openshift.io/developers added: &quot;linda&quot;
[student@workstation ~]$ oc adm groups add-users developers developer
group.user.openshift.io/developers added: &quot;developer&quot;
[student@workstation ~]$ oc adm groups add-users viewers lisa
group.user.openshift.io/viewers added: &quot;lisa&quot;
[student@workstation ~]$ 
</pre>
