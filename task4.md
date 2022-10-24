<pre>Created:	48 seconds ago
Labels:		name=myproject
Annotations:	openshift.io/description=
		openshift.io/display-name=
		openshift.io/requester=admin
		openshift.io/sa.scc.mcs=s0:c25,c20
		openshift.io/sa.scc.supplemental-groups=1000640000/10000
		openshift.io/sa.scc.uid-range=1000640000/10000
Display Name:	&lt;none&gt;
Description:	&lt;none&gt;
Status:		Active
Node Selector:	&lt;none&gt;
Quota:
	Name:		myproject-compute-resources
	Resource	Used	Hard
	--------	----	----
	limits.cpu	0	4
	limits.memory	0	4Gi
	pods		0	20
	requests.cpu	0	2
	requests.memory	0	1Gi
Resource limits:
	Name:		myproject-resource-limits
	Type		Resource	Min	Max	Default Request	Default Limit	Max Limit/Request Ratio
	----		--------	---	---	---------------	-------------	-----------------------
	Container	memory		-	2Gi	100Mi		2Gi		-
	Container	cpu		-	2	100m		2		-
[student@workstation ~]$ vi template.yaml 
[student@workstation ~]$ 
[student@workstation ~]$ 
[student@workstation ~]$ 
[student@workstation ~]$ 
[student@workstation ~]$ 
[student@workstation ~]$ 
[student@workstation ~]$ 
[student@workstation ~]$ 
[student@workstation ~]$ 
[student@workstation ~]$ 
[student@workstation ~]$ clear

[student@workstation ~]$ oc whoami
admin
[student@workstation ~]$ oc login -u developer -p redhat
Login successful.

You have access to 61 projects, the list has been suppressed. You can list all projects with &apos; projects&apos;

Using project &quot;myproject&quot;.
[student@workstation ~]$ oc new-project local-project
Now using project &quot;local-project&quot; on server &quot;https://api.ocp4.example.com:6443&quot;.

You can add applications to this project with the &apos;new-app&apos; command. For example, try:

    oc new-app rails-postgresql-example

to build a new example application in Ruby. Or use kubectl to deploy a simple Kubernetes application:

    kubectl create deployment hello-node --image=k8s.gcr.io/serve_hostname

[student@workstation ~]$ oc describe project local-project
Name:		local-project
Created:	23 seconds ago
Labels:		name=local-project
Annotations:	openshift.io/description=
		openshift.io/display-name=
		openshift.io/requester=developer
		openshift.io/sa.scc.mcs=s0:c26,c0
		openshift.io/sa.scc.supplemental-groups=1000650000/10000
		openshift.io/sa.scc.uid-range=1000650000/10000
Display Name:	&lt;none&gt;
Description:	&lt;none&gt;
Status:		Active
Node Selector:	&lt;none&gt;
Quota:
	Name:		local-project-compute-resources
	Resource	Used	Hard
	--------	----	----
	limits.cpu	0	4
	limits.memory	0	4Gi
	pods		0	20
	requests.cpu	0	2
	requests.memory	0	1Gi
Resource limits:
	Name:		local-project-resource-limits
	Type		Resource	Min	Max	Default Request	Default Limit	Max Limit/Request Ratio
	----		--------	---	---	---------------	-------------	-----------------------
	Container	cpu		-	2	100m		2		-
	Container	memory		-	2Gi	100Mi		2Gi		-
[student@workstation ~]$ 
</pre>
