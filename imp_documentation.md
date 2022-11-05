Project template 
----------------------------

https://docs.openshift.com/container-platform/4.10/applications/projects/configuring-project-creation.html


Secrets 
----------------------------

https://docs.openshift.com/container-platform/4.10/nodes/pods/nodes-pods-secrets.html


Self-Signed Certificate
-------------------------------------------

https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/4/html/system_administration_guide/apache_http_secure_server_configuration-creating_a_self_signed_certificate


user creation, authentication and permissions
----------------------------------------------------------------

https://docs.openshift.com/container-platform/4.10/authentication/identity_providers/configuring-htpasswd-identity-provider.html


https://docs.openshift.com/container-platform/4.10/authentication/remove-kubeadmin.html



limits, quotas
--------------------------------------------

https://docs.openshift.com/container-platform/4.10/applications/quotas/quotas-setting-across-multiple-projects.html

review below information with some examples:

We use Limits to set a limit (the maximum amount of a resource that a pod can use) and requests (the amount of resources a pod needs and is ensured) on containers and pods.
You can use a limit to set the maximum amount of CPU usage by a pod or container to 1 CPU
You can ensure a pod or container always gets 512Mi of Memory using a request


We use LimitRanges to set a default, minimum or maximum of the resources each pod can get.
We can use a LimitRange to set a default Memory request for all pods
A LimitRange can limit the maximum amount of CPU a pod can request to 200m
We use ResourceQuota to set the maximum number of objects in a namespace or to enforce the usage of a limit and the total amount of resources a namespace can use


A quota in a namespace can limit the sum of all CPU requests to 2 CPU’s (2000m or 2)
You can limit the amount of routes you can have in a namespace to 1
You can force pod’s to have a set limit or request


And we can use a ClusterResourceQuota to span a quota over multiple namespaces based on a field tag or the requester (owner) of a project.
With a cluster quota we can set a limit of 20 pods that can be running by a user
We can limit the amount of CPU used to 4 (4000m) of several namespaces that we have tagd as production=true
All in all, pretty usefull stuf. 



 Taints and Tolerations 
---------------------------------------

https://docs.openshift.com/container-platform/4.10/nodes/scheduling/nodes-scheduler-taints-tolerations.html


https://docs.openshift.com/container-platform/4.10/nodes/scheduling/nodes-scheduler-taints-tolerations.html#nodes-scheduler-taints-tolerations-all_nodes-scheduler-taints-tolerations


https://docs.openshift.com/container-platform/4.10/nodes/scheduling/nodes-scheduler-taints-tolerations.html#nodes-scheduler-taints-tolerations-about_nodes-scheduler-taints-tolerations



Deployment and DeploymentConfig 
-------------------------------------------------------


https://docs.openshift.com/container-platform/4.10/applications/deployments/what-deployments-are.html


https://docs.openshift.com/container-platform/4.10/applications/deployments/managing-deployment-processes.html


https://docs.openshift.com/container-platform/4.10/nodes/pods/nodes-pods-autoscaling.html






