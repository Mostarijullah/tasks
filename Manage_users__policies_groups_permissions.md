<pre> Restoring authentication settings to installation defaults:
 · Removing &apos;cluster-admin&apos; role from the &apos;admin&apos; user.........  <font color="#34E2E2"><b>SUCCESS</b></font>
 · Remove HTPasswd secret: &apos;htpasswd-secret&apos;...................  <font color="#34E2E2"><b>SUCCESS</b></font>
 · Remove all configured Identity Providers....................  <font color="#34E2E2"><b>SUCCESS</b></font>

Overall start status...........................................  <font color="#34E2E2"><b>SUCCESS</b></font>

[student@workstation ~]$ oc whoami
error: Missing or incomplete configuration info.  Please point to an existing, complete config file:


  1. Via the command-line flag --kubeconfig
  2. Via the KUBECONFIG environment variable
  3. In your home directory as ~/.kube/config

To view or setup config directly use the &apos;config&apos; command.
[student@workstation ~]$ cd /usr/local/etc/
[student@workstation etc]$ ls
ocp4.config  <font color="#00D700">ocp4.defaults</font>
[student@workstation etc]$ cat ocp4.
cat: ocp4.: No such file or directory
[student@workstation etc]$ cat ocp4.config 
RHT_OCP4_MASTER_API=https://api.ocp4.example.com:6443
RHT_OCP4_WILDCARD_DOMAIN=apps.ocp4.example.com
RHT_OCP4_KUBEADM_PASSWD=waoWn-5S9VM-6cSsy-kMAyk
RHT_OCP4_USER_PASSWD=redhat
[student@workstation etc]$ oc login -u kubeadmin -p waoWn-5S9VM-6cSsy-kMAyk https://api.ocp4.example.com:6443
Login successful.

You have access to 59 projects, the list has been suppressed. You can list all projects with &apos; projects&apos;

Using project &quot;default&quot;.
Welcome! See &apos;oc help&apos; to get started.
[student@workstation etc]$ clear

[student@workstation etc]$ cd ~
[student@workstation ~]$ pwd
/home/student
[student@workstation ~]$ oc whoami
kube:admin
[student@workstation ~]$ oc whoami --show-console
https://console-openshift-console.apps.ocp4.example.com
[student@workstation ~]$ sudo yum install httpd-tools
Last metadata expiration check: 0:12:54 ago on Fri 04 Nov 2022 12:14:31 AM EDT.
Package httpd-tools-2.4.37-21.module+el8.2.0+5008+cca404a3.x86_64 is already installed.
Dependencies resolved.
Nothing to do.
Complete!
[student@workstation ~]$ ls
<font color="#0087FF">Desktop</font>  <font color="#0087FF">DO280</font>  <font color="#0087FF">Documents</font>  <font color="#0087FF">Downloads</font>  <font color="#0087FF">Music</font>  <font color="#0087FF">Pictures</font>  <font color="#0087FF">Public</font>  <font color="#0087FF">Templates</font>  <font color="#0087FF">venv</font>  <font color="#0087FF">Videos</font>
[student@workstation ~]$ cd DO280/
[student@workstation DO280]$ ls
<font color="#0087FF">labs</font>  <font color="#0087FF">solutions</font>
[student@workstation DO280]$ cd labs/
[student@workstation labs]$ ls
<font color="#0087FF">auth-provider</font>
[student@workstation labs]$ cd auth-provider/
[student@workstation auth-provider]$ ls
oauth.yaml
[student@workstation auth-provider]$ htpasswd -c -B -b htpasswd-file Michael redhat
Adding password for user Michael
[student@workstation auth-provider]$ htpasswd -B -b htpasswd-file Pam redhat
Adding password for user Pam
[student@workstation auth-provider]$ htpasswd -B -b htpasswd-file Dwight redhat
Adding password for user Dwight
[student@workstation auth-provider]$ htpasswd -B -b htpasswd-file Jim redhat
Adding password for user Jim
[student@workstation auth-provider]$ htpasswd -B -b htpasswd-file admin redhat
Adding password for user admin
[student@workstation auth-provider]$ htpasswd -B -b htpasswd-file Sidd redhat
Adding password for user Sidd
[student@workstation auth-provider]$ cat htpasswd-file 
Michael:$2y$05$aglpVM9zQ0yU27pYrYUET.6cgT09gYQ4dy9cWA5YRZGLSfMjuI/wu
Pam:$2y$05$CXBj8zL7x2RPA4DeDPu3huYFggphv0XzyjGfWzV3sziBekwvINsiy
Dwight:$2y$05$vWS81nPTDeLiyb5ycRWUheISMDdtKdFOWlVNyFw8c95gBaALDonTa
Jim:$2y$05$XC7kb2oyZJkUGk2FTtyGee6qMKLOnLIsOUeqZbV6vc5rPhv5l6nB.
admin:$2y$05$M5pjN2f6tdOoXGN6C21H8.Zaegz76W10ONOF8fADQCgOR45meEWnS
Sidd:$2y$05$nY.q13go9cSv8Mt1xp09ZOBXGgymtFYF73ug/HYzjuklpeQwVwkgy
[student@workstation auth-provider]$ oc create secret generic htpasswd-source --from-file=htpasswd=htpasswd-file -n openshift-config
secret/htpasswd-source created
[student@workstation auth-provider]$ ls
htpasswd-file  oauth.yaml
[student@workstation auth-provider]$ mv oauth.yaml oauth.yaml.bk 
[student@workstation auth-provider]$ ls
htpasswd-file  oauth.yaml.bk
[student@workstation auth-provider]$ oc get oauth cluster -o yaml &gt; oauth.yaml
[student@workstation auth-provider]$ ls
htpasswd-file  oauth.yaml  oauth.yaml.bk
[student@workstation auth-provider]$ vi oauth.yaml
[student@workstation auth-provider]$ watch oc get pods -n openshift-authentication
[student@workstation auth-provider]$ oc replace -f oauth.yaml 
oauth.config.openshift.io/cluster replaced
[student@workstation auth-provider]$ watch oc get pods -n openshift-authentication
[student@workstation auth-provider]$ oc adm policy add-cluster-role-to-user cluster-admin admin
Warning: User &apos;admin&apos; not found
clusterrole.rbac.authorization.k8s.io/cluster-admin added: &quot;admin&quot;
[student@workstation auth-provider]$ oc get users
No resources found
[student@workstation auth-provider]$ oc get identity
No resources found
[student@workstation auth-provider]$ watch oc get pods -n openshift-authentication
[student@workstation auth-provider]$ oc login -u admin -p redhat
Login successful.

You have access to 59 projects, the list has been suppressed. You can list all projects with &apos; projects&apos;

Using project &quot;default&quot;.
[student@workstation auth-provider]$ oc get users
NAME    UID                                    FULL NAME   IDENTITIES
admin   5d4a17bb-4aca-4122-bd85-7ca5d8046a07               cluster-users:admin
[student@workstation auth-provider]$ oc get identity
NAME                  IDP NAME        IDP USER NAME   USER NAME   USER UID
cluster-users:admin   cluster-users   admin           admin       5d4a17bb-4aca-4122-bd85-7ca5d8046a07
[student@workstation auth-provider]$ oc adm groups new managers
group.user.openshift.io/managers created
[student@workstation auth-provider]$ oc adm groups add-users managers Michael
group.user.openshift.io/managers added: &quot;Michael&quot;
[student@workstation auth-provider]$ oc get groups
NAME       USERS
managers   Michael
[student@workstation auth-provider]$ oc adm groups new sales Jim Dwight
group.user.openshift.io/sales created
[student@workstation auth-provider]$ oc get groups
NAME       USERS
managers   Michael
sales      Jim, Dwight
[student@workstation auth-provider]$ oc adm groups new reception Pam
group.user.openshift.io/reception created
[student@workstation auth-provider]$ oc get groups
NAME        USERS
managers    Michael
reception   Pam
sales       Jim, Dwight
[student@workstation auth-provider]$ oc adm groups add-users managers Sidd
group.user.openshift.io/managers added: &quot;Sidd&quot;
[student@workstation auth-provider]$ oc new-project sales
Now using project &quot;sales&quot; on server &quot;https://api.ocp4.example.com:6443&quot;.

You can add applications to this project with the &apos;new-app&apos; command. For example, try:

    oc new-app rails-postgresql-example

to build a new example application in Ruby. Or use kubectl to deploy a simple Kubernetes application:

    kubectl create deployment hello-node --image=k8s.gcr.io/serve_hostname

[student@workstation auth-provider]$ oc adm policy add-role-to-group edit sales \
&gt;   --namespace sales
clusterrole.rbac.authorization.k8s.io/edit added: &quot;sales&quot;
[student@workstation auth-provider]$ oc adm policy add-role-to-group view reception --namespace sales
clusterrole.rbac.authorization.k8s.io/view added: &quot;reception&quot;
[student@workstation auth-provider]$ oc describe rolebinding.rbac -n sale
No resources found in sale namespace.
[student@workstation auth-provider]$ oc describe rolebinding.rbac -n sales
Name:         admin
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
Role:
  Kind:  ClusterRole
  Name:  admin
Subjects:
  Kind  Name   Namespace
  ----  ----   ---------
  User  admin  


Name:         edit
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
Role:
  Kind:  ClusterRole
  Name:  edit
Subjects:
  Kind   Name   Namespace
  ----   ----   ---------
  Group  sales  


Name:         system:deployers
Labels:       &lt;none&gt;
Annotations:  openshift.io/description:
                Allows deploymentconfigs in this namespace to rollout pods in this namespace.  It is auto-managed by a controller; remove subjects to disa...
Role:
  Kind:  ClusterRole
  Name:  system:deployer
Subjects:
  Kind            Name      Namespace
  ----            ----      ---------
  ServiceAccount  deployer  sales


Name:         system:image-builders
Labels:       &lt;none&gt;
Annotations:  openshift.io/description:
                Allows builds in this namespace to push images to this namespace.  It is auto-managed by a controller; remove subjects to disable.
Role:
  Kind:  ClusterRole
  Name:  system:image-builder
Subjects:
  Kind            Name     Namespace
  ----            ----     ---------
  ServiceAccount  builder  sales


Name:         system:image-pullers
Labels:       &lt;none&gt;
Annotations:  openshift.io/description:
                Allows all pods in this namespace to pull images from this namespace.  It is auto-managed by a controller; remove subjects to disable.
Role:
  Kind:  ClusterRole
  Name:  system:image-puller
Subjects:
  Kind   Name                          Namespace
  ----   ----                          ---------
  Group  system:serviceaccounts:sales  


Name:         view
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
Role:
  Kind:  ClusterRole
  Name:  view
Subjects:
  Kind   Name       Namespace
  ----   ----       ---------
  Group  reception  
[student@workstation auth-provider]$ oc adm policy add-role-to-group admin managers --namespace sales
clusterrole.rbac.authorization.k8s.io/admin added: &quot;managers&quot;
[student@workstation auth-provider]$ oc describe rolebinding.rbac -n sales
Name:         admin
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
Role:
  Kind:  ClusterRole
  Name:  admin
Subjects:
  Kind  Name   Namespace
  ----  ----   ---------
  User  admin  


Name:         admin-0
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
Role:
  Kind:  ClusterRole
  Name:  admin
Subjects:
  Kind   Name      Namespace
  ----   ----      ---------
  Group  managers  


Name:         edit
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
Role:
  Kind:  ClusterRole
  Name:  edit
Subjects:
  Kind   Name   Namespace
  ----   ----   ---------
  Group  sales  


Name:         system:deployers
Labels:       &lt;none&gt;
Annotations:  openshift.io/description:
                Allows deploymentconfigs in this namespace to rollout pods in this namespace.  It is auto-managed by a controller; remove subjects to disa...
Role:
  Kind:  ClusterRole
  Name:  system:deployer
Subjects:
  Kind            Name      Namespace
  ----            ----      ---------
  ServiceAccount  deployer  sales


Name:         system:image-builders
Labels:       &lt;none&gt;
Annotations:  openshift.io/description:
                Allows builds in this namespace to push images to this namespace.  It is auto-managed by a controller; remove subjects to disable.
Role:
  Kind:  ClusterRole
  Name:  system:image-builder
Subjects:
  Kind            Name     Namespace
  ----            ----     ---------
  ServiceAccount  builder  sales


Name:         system:image-pullers
Labels:       &lt;none&gt;
Annotations:  openshift.io/description:
                Allows all pods in this namespace to pull images from this namespace.  It is auto-managed by a controller; remove subjects to disable.
Role:
  Kind:  ClusterRole
  Name:  system:image-puller
Subjects:
  Kind   Name                          Namespace
  ----   ----                          ---------
  Group  system:serviceaccounts:sales  


Name:         view
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
Role:
  Kind:  ClusterRole
  Name:  view
Subjects:
  Kind   Name       Namespace
  ----   ----       ---------
  Group  reception  
[student@workstation auth-provider]$ oc whoami
admin
[student@workstation auth-provider]$ oc delete secrets kubeadmin -n kube-system
secret &quot;kubeadmin&quot; deleted
[student@workstation auth-provider]$ 
</pre>
