<pre>  110  oc edit project.config.openshift.io/cluster 
  111  watch oc get pods -n openshift-apiserver
  112  ls
  113  cd ~
  114  cd tasks/
  115  ls
  116  oc get users
  117  os get identity
  118  os get identities
  119  oc get identities
  120  oc get groups
  121  watch oc get pods -n openshift-apiserver
  122  oc get pods -n openshift-apiserver
  123  oc new-project template-test-project
  124  vi our-template.yaml 
  125  oc whoami
  126  oc new-project template-test-project
  127  oc edit project.config.openshift.io/cluster
  128  ls
  129  mv our-template.yaml template-by-sidd.yaml
  130  ls
  131  oc apply -f template-by-sidd.yaml -n openshift-config
  132  oc edit project.config.openshift.io/cluster
  133  watch oc get pods -n openshift-apiserver
  134  oc get pods -n openshift-apiserver
  135  oc get templates.template.openshift.io -n openshift-config
  136  oc new-project test-proj
  137  vi template-by-sidd.yaml 
  138  oc apply -f template-by-sidd.yaml -n openshift-config
  139  oc get templates.template.openshift.io -n openshift-config
  140  oc new-project test-proj
  141  oc get limitrange
  142  oc adm policy add-cluster-role-to-group self-provisioner managers
  143  oc describe clusterrolebindings self-provisioners
  144  oc adm policy remove-cluster-role-from-group self-provisioner system:authenticated:oauth
  145  oc describe clusterrolebindings self-provisioners
  146  oc login -u Sidd -p redhat
  147  oc new-project proj-creation-test
  148  oc get groups
</pre>
<pre> 78  oc describe clusterrolebindings self-provisioners
   79  oc adm policy remove-cluster-role-from-group self-provisioner system:authenticated:oauth
   80  oc describe clusterrolebindings self-provisioners
   81  oc whoami
   82  oc describe clusterrolebindings self-provisioners
   83  oc adm policy add-cluster-role-to-group --rolebinding-name=self-provisioners  self-provisioner system:authenticated:oauth
   84  oc describe clusterrolebindings self-provisioners
   85  oc adm create-bootstrap-project-template -o yaml &gt; our-template.yaml
   86  vi our-template.yaml 
   87  watch oc get pods -n openshift-apiserver
   88  oc apply -f our-template.yaml -n openshift-config
   89  vi our-template.yaml 
   90  oc apply -f our-template.yaml -n openshift-config
   91  watch oc get pods -n openshift-apiserver
   92  oc edit project.config.openshift.io/cluster 
   93  watch oc get pods -n openshift-apiserver
   94  oc get templates.template.openshift.io -n openshift-config
   95  watch oc get pods -n openshift-apiserver
   96  oc get pods -n openshift-apiserver
   97  oc new-project template-test-project
   98  cd tasks/
   99  ls
  100  watch oc get pods -n openshift-apiserver
  101  oc whoami
  102  oc whoami --show-console
  103  cd /usr/local/etc/
  104  ls
  105  cat ocp4.config 
  106  oc login -u admin -p redhat https://api.ocp4.example.com:6443
  107  clear
  108  watch oc get pods -n openshift-apiserver
  109  oc get templates.template.openshift.io -n openshift-config
  110  oc edit project.config.openshift.io/cluster 
  111  watch oc get pods -n openshift-apiserver
</pre>


<pre># Please edit the object below. Lines beginning with a &apos;#&apos; will be ignored,
# and an empty file will abort the edit. If an error occurs while saving this file will be
# reopened with the relevant failures.
#
apiVersion: config.openshift.io/v1
kind: Project
metadata:
  annotations:
    release.openshift.io/create-only: &quot;true&quot;
  creationTimestamp: &quot;2021-07-13T12:14:16Z&quot;
  generation: 3
  name: cluster
  resourceVersion: &quot;88845&quot;
  selfLink: /apis/config.openshift.io/v1/projects/cluster
  uid: 79393776-5d05-4f9c-a7ba-19711eed9060
spec:
  projectRequestTemplate:
    name: template-by-sidd
<font color="#729FCF">~                                                                                                               </font>
<font color="#729FCF">~                                  </font></pre>


<pre>[student@workstation tasks]$  oc get templates.template.openshift.io -n openshift-config
NAME               DESCRIPTION   PARAMETERS    OBJECTS
template-by-sidd                 5 (5 blank)   3
[student@workstation tasks]$ oc edit projects cluster
Error from server (NotFound): namespaces &quot;cluster&quot; not found
[student@workstation tasks]$ oc edit template cluster
Error from server (NotFound): templates.template.openshift.io &quot;cluster&quot; not found
[student@workstation tasks]$ oc edit projects.config.openshift.io/cluster
Edit cancelled, no changes made.
</pre>
