<pre>[student@workstation ~]$ ls
<font color="#0087FF">Desktop</font>  <font color="#0087FF">DO280</font>  <font color="#0087FF">Documents</font>  <font color="#0087FF">Downloads</font>  <font color="#0087FF">Music</font>  <font color="#0087FF">Pictures</font>  <font color="#0087FF">Public</font>  <font color="#0087FF">tasks</font>  <font color="#0087FF">Templates</font>  <font color="#0087FF">venv</font>  <font color="#0087FF">Videos</font>
[student@workstation ~]$ cd tasks/
[student@workstation tasks]$ oc login -u admin -p redhat
Unable to connect to the server: EOF
[student@workstation tasks]$ cat /usr/local/etc/ocp4.config 
RHT_OCP4_MASTER_API=https://api.ocp4.example.com:6443
RHT_OCP4_WILDCARD_DOMAIN=apps.ocp4.example.com
RHT_OCP4_KUBEADM_PASSWD=waoWn-5S9VM-6cSsy-kMAyk
RHT_OCP4_USER_PASSWD=redhat
[student@workstation tasks]$ 
[student@workstation tasks]$ oc login -u admin -p redhat https://api.ocp4.example.com:6443
Login successful.

You have access to 63 projects, the list has been suppressed. You can list all projects with &apos; projects&apos;

Using project &quot;proj-creation-test01&quot;.
[student@workstation tasks]$ oc get nodes -o wide
NAME       STATUS   ROLES           AGE    VERSION           INTERNAL-IP     EXTERNAL-IP   OS-IMAGE                                                       KERNEL-VERSION                 CONTAINER-RUNTIME
master01   Ready    master,worker   479d   v1.19.0+b00ba52   192.168.50.10   &lt;none&gt;        Red Hat Enterprise Linux CoreOS 46.82.202106181041-0 (Ootpa)   4.18.0-193.56.1.el8_2.x86_64   cri-o://1.19.2-6.rhaos4.6.git686e6d9.el8
master02   Ready    master,worker   479d   v1.19.0+b00ba52   192.168.50.11   &lt;none&gt;        Red Hat Enterprise Linux CoreOS 46.82.202106181041-0 (Ootpa)   4.18.0-193.56.1.el8_2.x86_64   cri-o://1.19.2-6.rhaos4.6.git686e6d9.el8
master03   Ready    master,worker   479d   v1.19.0+b00ba52   192.168.50.12   &lt;none&gt;        Red Hat Enterprise Linux CoreOS 46.82.202106181041-0 (Ootpa)   4.18.0-193.56.1.el8_2.x86_64   cri-o://1.19.2-6.rhaos4.6.git686e6d9.el8
[student@workstation tasks]$ oc get ns
NAME                                               STATUS   AGE
default                                            Active   479d
kube-node-lease                                    Active   479d
kube-public                                        Active   479d
kube-system                                        Active   479d
nfs-client-provisioner                             Active   479d
openshift                                          Active   479d
openshift-apiserver                                Active   479d
openshift-apiserver-operator                       Active   479d
openshift-authentication                           Active   479d
openshift-authentication-operator                  Active   479d
openshift-cloud-credential-operator                Active   479d
openshift-cluster-csi-drivers                      Active   479d
openshift-cluster-machine-approver                 Active   479d
openshift-cluster-node-tuning-operator             Active   479d
openshift-cluster-samples-operator                 Active   479d
openshift-cluster-storage-operator                 Active   479d
openshift-cluster-version                          Active   479d
openshift-config                                   Active   479d
openshift-config-managed                           Active   479d
openshift-config-operator                          Active   479d
openshift-console                                  Active   479d
openshift-console-operator                         Active   479d
openshift-controller-manager                       Active   479d
openshift-controller-manager-operator              Active   479d
openshift-dns                                      Active   479d
openshift-dns-operator                             Active   479d
openshift-etcd                                     Active   479d
openshift-etcd-operator                            Active   479d
openshift-image-registry                           Active   479d
openshift-infra                                    Active   479d
openshift-ingress                                  Active   479d
openshift-ingress-operator                         Active   479d
openshift-insights                                 Active   479d
openshift-kni-infra                                Active   479d
openshift-kube-apiserver                           Active   479d
openshift-kube-apiserver-operator                  Active   479d
openshift-kube-controller-manager                  Active   479d
openshift-kube-controller-manager-operator         Active   479d
openshift-kube-scheduler                           Active   479d
openshift-kube-scheduler-operator                  Active   479d
openshift-kube-storage-version-migrator            Active   479d
openshift-kube-storage-version-migrator-operator   Active   479d
openshift-machine-api                              Active   479d
openshift-machine-config-operator                  Active   479d
openshift-marketplace                              Active   479d
openshift-monitoring                               Active   479d
openshift-multus                                   Active   479d
openshift-network-operator                         Active   479d
openshift-node                                     Active   479d
openshift-oauth-apiserver                          Active   479d
openshift-openstack-infra                          Active   479d
openshift-operator-lifecycle-manager               Active   479d
openshift-operators                                Active   479d
openshift-ovirt-infra                              Active   479d
openshift-sdn                                      Active   479d
openshift-service-ca                               Active   479d
openshift-service-ca-operator                      Active   479d
openshift-user-workload-monitoring                 Active   479d
openshift-vsphere-infra                            Active   479d
proj-creation-test                                 Active   21h
proj-creation-test01                               Active   21h
sales                                              Active   22h
test-proj                                          Active   21h
[student@workstation tasks]$ o get co
bash: o: command not found...
[student@workstation tasks]$ oc get co
NAME                                       VERSION   AVAILABLE   PROGRESSING   DEGRADED   SINCE
authentication                             4.6.36    True        False         False      37s
cloud-credential                           4.6.36    True        False         False      479d
cluster-autoscaler                         4.6.36    True        False         False      479d
config-operator                            4.6.36    True        False         False      479d
console                                    4.6.36    True        False         False      23h
csi-snapshot-controller                    4.6.36    True        False         False      23h
dns                                        4.6.36    True        False         False      104s
etcd                                       4.6.36    True        False         False      479d
image-registry                             4.6.36    True        False         False      23h
ingress                                    4.6.36    True        False         False      62s
insights                                   4.6.36    True        False         False      479d
kube-apiserver                             4.6.36    True        False         False      479d
kube-controller-manager                    4.6.36    True        False         False      479d
kube-scheduler                             4.6.36    True        False         False      479d
kube-storage-version-migrator              4.6.36    True        False         False      23h
machine-api                                4.6.36    True        False         False      479d
machine-approver                           4.6.36    True        False         False      479d
machine-config                             4.6.36    True        False         False      479d
marketplace                                4.6.36    True        False         False      57s
monitoring                                 4.6.36    True        False         False      5s
network                                    4.6.36    True        False         False      479d
node-tuning                                4.6.36    True        False         False      479d
openshift-apiserver                        4.6.36    True        False         False      95s
openshift-controller-manager               4.6.36    True        False         False      479d
openshift-samples                          4.6.36    True        False         False      479d
operator-lifecycle-manager                 4.6.36    True        False         False      479d
operator-lifecycle-manager-catalog         4.6.36    True        False         False      479d
operator-lifecycle-manager-packageserver   4.6.36    True        False         False      23h
service-ca                                 4.6.36    True        False         False      479d
storage                                    4.6.36    True        False         False      479d
[student@workstation tasks]$ oc adm taint node master03  linux=good:NoSchedule
node/master03 tainted
[student@workstation tasks]$ oc new-project tainted-love
Now using project &quot;tainted-love&quot; on server &quot;https://api.ocp4.example.com:6443&quot;.

You can add applications to this project with the &apos;new-app&apos; command. For example, try:

    oc new-app rails-postgresql-example

to build a new example application in Ruby. Or use kubectl to deploy a simple Kubernetes application:

    kubectl create deployment hello-node --image=k8s.gcr.io/serve_hostname

[student@workstation tasks]$  oc new-app --name i-like-linux --docker-image bitnami/nginx
--&gt; Found container image 09dbf44 (2 days old) from Docker Hub for &quot;bitnami/nginx&quot;

    * An image stream tag will be created as &quot;i-like-linux:latest&quot; that will track this image

--&gt; Creating resources ...
    imagestream.image.openshift.io &quot;i-like-linux&quot; created
    deployment.apps &quot;i-like-linux&quot; created
    service &quot;i-like-linux&quot; created
--&gt; Success
    Application is not exposed. You can expose services to the outside world by executing one or more of the commands below:
     &apos;oc expose service/i-like-linux&apos; 
    Run &apos;oc status&apos; to view your app.
[student@workstation tasks]$ oc get pod
NAME                            READY   STATUS              RESTARTS   AGE
i-like-linux-7864d55cc4-n6wp7   0/1     ContainerCreating   0          12s
[student@workstation tasks]$ oc describe pod i-like-linux-7864d55cc4-n6wp7 
Name:         i-like-linux-7864d55cc4-n6wp7
Namespace:    tainted-love
Priority:     0
Node:         master01/192.168.50.10
Start Time:   Fri, 04 Nov 2022 23:33:46 -0400
Labels:       deployment=i-like-linux
              pod-template-hash=7864d55cc4
Annotations:  k8s.v1.cni.cncf.io/network-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.8.0.10&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              k8s.v1.cni.cncf.io/networks-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.8.0.10&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              kubernetes.io/limit-ranger: LimitRanger plugin set: cpu request for container i-like-linux; cpu limit for container i-like-linux
              openshift.io/generated-by: OpenShiftNewApp
              openshift.io/scc: restricted
Status:       Running
IP:           10.8.0.10
IPs:
  IP:           10.8.0.10
Controlled By:  ReplicaSet/i-like-linux-7864d55cc4
Containers:
  i-like-linux:
    Container ID:   cri-o://8bd35d494efad8bb81122ac90b649e475c8504295a5f46309f0f980545c108ff
    Image:          bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67
    Image ID:       docker.io/bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67
    Ports:          8080/TCP, 8443/TCP
    Host Ports:     0/TCP, 0/TCP
    State:          Running
      Started:      Fri, 04 Nov 2022 23:34:04 -0400
    Ready:          True
    Restart Count:  0
    Limits:
      cpu:  50m
    Requests:
      cpu:        50m
    Environment:  &lt;none&gt;
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-svcb6 (ro)
Conditions:
  Type              Status
  Initialized       True 
  Ready             True 
  ContainersReady   True 
  PodScheduled      True 
Volumes:
  default-token-svcb6:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  default-token-svcb6
    Optional:    false
QoS Class:       Burstable
Node-Selectors:  &lt;none&gt;
Tolerations:     node.kubernetes.io/memory-pressure:NoSchedule op=Exists
                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                 node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type    Reason          Age   From               Message
  ----    ------          ----  ----               -------
  Normal  Scheduled       21s   default-scheduler  Successfully assigned tainted-love/i-like-linux-7864d55cc4-n6wp7 to master01
  Normal  AddedInterface  18s   multus             Add eth0 [10.8.0.10/23]
  Normal  Pulling         14s   kubelet            Pulling image &quot;bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67&quot;
  Normal  Pulled          5s    kubelet            Successfully pulled image &quot;bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67&quot; in 8.46219875s
  Normal  Created         3s    kubelet            Created container i-like-linux
  Normal  Started         3s    kubelet            Started container i-like-linux
[student@workstation tasks]$ oc adm taint node master01  linux=good:NoExecute
node/master01 tainted
[student@workstation tasks]$ oc get pod
NAME                            READY   STATUS              RESTARTS   AGE
i-like-linux-7864d55cc4-n6wp7   0/1     Terminating         0          109s
i-like-linux-7864d55cc4-wlvt6   0/1     ContainerCreating   0          6s
[student@workstation tasks]$ oc get pod
NAME                            READY   STATUS              RESTARTS   AGE
i-like-linux-7864d55cc4-wlvt6   0/1     ContainerCreating   0          14s
[student@workstation tasks]$ oc get pod
NAME                            READY   STATUS    RESTARTS   AGE
i-like-linux-7864d55cc4-wlvt6   1/1     Running   0          29s
[student@workstation tasks]$ oc describe pod i-like-linux-7864d55cc4-wlvt6 
Name:         i-like-linux-7864d55cc4-wlvt6
Namespace:    tainted-love
Priority:     0
Node:         master02/192.168.50.11
Start Time:   Fri, 04 Nov 2022 23:35:30 -0400
Labels:       deployment=i-like-linux
              pod-template-hash=7864d55cc4
Annotations:  k8s.v1.cni.cncf.io/network-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.9.0.36&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              k8s.v1.cni.cncf.io/networks-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.9.0.36&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              kubernetes.io/limit-ranger: LimitRanger plugin set: cpu request for container i-like-linux; cpu limit for container i-like-linux
              openshift.io/generated-by: OpenShiftNewApp
              openshift.io/scc: restricted
Status:       Running
IP:           10.9.0.36
IPs:
  IP:           10.9.0.36
Controlled By:  ReplicaSet/i-like-linux-7864d55cc4
Containers:
  i-like-linux:
    Container ID:   cri-o://938988bd1c1d2b6ab98b579887c9a9b0897b09b463b792bc83a8415d81541cb8
    Image:          bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67
    Image ID:       docker.io/bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67
    Ports:          8080/TCP, 8443/TCP
    Host Ports:     0/TCP, 0/TCP
    State:          Running
      Started:      Fri, 04 Nov 2022 23:35:48 -0400
    Ready:          True
    Restart Count:  0
    Limits:
      cpu:  50m
    Requests:
      cpu:        50m
    Environment:  &lt;none&gt;
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-svcb6 (ro)
Conditions:
  Type              Status
  Initialized       True 
  Ready             True 
  ContainersReady   True 
  PodScheduled      True 
Volumes:
  default-token-svcb6:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  default-token-svcb6
    Optional:    false
QoS Class:       Burstable
Node-Selectors:  &lt;none&gt;
Tolerations:     node.kubernetes.io/memory-pressure:NoSchedule op=Exists
                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                 node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type    Reason          Age   From               Message
  ----    ------          ----  ----               -------
  Normal  Scheduled       39s   default-scheduler  Successfully assigned tainted-love/i-like-linux-7864d55cc4-wlvt6 to master02
  Normal  AddedInterface  37s   multus             Add eth0 [10.9.0.36/23]
  Normal  Pulling         32s   kubelet            Pulling image &quot;bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67&quot;
  Normal  Pulled          23s   kubelet            Successfully pulled image &quot;bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67&quot; in 8.863325738s
  Normal  Created         21s   kubelet            Created container i-like-linux
  Normal  Started         21s   kubelet            Started container i-like-linux
[student@workstation tasks]$ oc adm taint node master02  linux=good:NoExecute
node/master02 tainted
[student@workstation tasks]$ oc get pod
NAME                            READY   STATUS        RESTARTS   AGE
i-like-linux-7864d55cc4-ktb8s   0/1     Pending       0          6s
i-like-linux-7864d55cc4-wlvt6   0/1     Terminating   0          110s
[student@workstation tasks]$ oc get pod
NAME                            READY   STATUS        RESTARTS   AGE
i-like-linux-7864d55cc4-ktb8s   0/1     Pending       0          12s
i-like-linux-7864d55cc4-wlvt6   0/1     Terminating   0          116s
[student@workstation tasks]$ oc get nodes -o wide
NAME       STATUS   ROLES           AGE    VERSION           INTERNAL-IP     EXTERNAL-IP   OS-IMAGE                                                       KERNEL-VERSION                 CONTAINER-RUNTIME
master01   Ready    master,worker   479d   v1.19.0+b00ba52   192.168.50.10   &lt;none&gt;        Red Hat Enterprise Linux CoreOS 46.82.202106181041-0 (Ootpa)   4.18.0-193.56.1.el8_2.x86_64   cri-o://1.19.2-6.rhaos4.6.git686e6d9.el8
master02   Ready    master,worker   479d   v1.19.0+b00ba52   192.168.50.11   &lt;none&gt;        Red Hat Enterprise Linux CoreOS 46.82.202106181041-0 (Ootpa)   4.18.0-193.56.1.el8_2.x86_64   cri-o://1.19.2-6.rhaos4.6.git686e6d9.el8
master03   Ready    master,worker   479d   v1.19.0+b00ba52   192.168.50.12   &lt;none&gt;        Red Hat Enterprise Linux CoreOS 46.82.202106181041-0 (Ootpa)   4.18.0-193.56.1.el8_2.x86_64   cri-o://1.19.2-6.rhaos4.6.git686e6d9.el8
[student@workstation tasks]$ oc get nodes
NAME       STATUS   ROLES           AGE    VERSION
master01   Ready    master,worker   479d   v1.19.0+b00ba52
master02   Ready    master,worker   479d   v1.19.0+b00ba52
master03   Ready    master,worker   479d   v1.19.0+b00ba52
[student@workstation tasks]$ oc get pods
NAME                            READY   STATUS        RESTARTS   AGE
i-like-linux-7864d55cc4-ktb8s   0/1     Pending       0          45s
i-like-linux-7864d55cc4-wlvt6   0/1     Terminating   0          2m29s
[student@workstation tasks]$ watch oc get pods
[student@workstation tasks]$ watch oc get pods
[student@workstation tasks]$ oc describe pod i-like-linux-7864d55cc4-ktb8s 
Name:           i-like-linux-7864d55cc4-ktb8s
Namespace:      tainted-love
Priority:       0
Node:           &lt;none&gt;
Labels:         deployment=i-like-linux
                pod-template-hash=7864d55cc4
Annotations:    kubernetes.io/limit-ranger: LimitRanger plugin set: cpu request for container i-like-linux; cpu limit for container i-like-linux
                openshift.io/generated-by: OpenShiftNewApp
                openshift.io/scc: restricted
Status:         Pending
IP:             
IPs:            &lt;none&gt;
Controlled By:  ReplicaSet/i-like-linux-7864d55cc4
Containers:
  i-like-linux:
    Image:       bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67
    Ports:       8080/TCP, 8443/TCP
    Host Ports:  0/TCP, 0/TCP
    Limits:
      cpu:  50m
    Requests:
      cpu:        50m
    Environment:  &lt;none&gt;
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-svcb6 (ro)
Conditions:
  Type           Status
  PodScheduled   False 
Volumes:
  default-token-svcb6:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  default-token-svcb6
    Optional:    false
QoS Class:       Burstable
Node-Selectors:  &lt;none&gt;
Tolerations:     node.kubernetes.io/memory-pressure:NoSchedule op=Exists
                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                 node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type     Reason            Age                  From               Message
  ----     ------            ----                 ----               -------
  Warning  FailedScheduling  45s (x10 over 2m1s)  default-scheduler  0/3 nodes are available: 3 node(s) had taint {linux: good}, that the pod didn&apos;t tolerate.
[student@workstation tasks]$ oc describe pod i-like-linux-7864d55cc4-wlvt6 
Name:                      i-like-linux-7864d55cc4-wlvt6
Namespace:                 tainted-love
Priority:                  0
Node:                      master02/192.168.50.11
Start Time:                Fri, 04 Nov 2022 23:35:30 -0400
Labels:                    deployment=i-like-linux
                           pod-template-hash=7864d55cc4
Annotations:               k8s.v1.cni.cncf.io/network-status:
                             [{
                                 &quot;name&quot;: &quot;&quot;,
                                 &quot;interface&quot;: &quot;eth0&quot;,
                                 &quot;ips&quot;: [
                                     &quot;10.9.0.36&quot;
                                 ],
                                 &quot;default&quot;: true,
                                 &quot;dns&quot;: {}
                             }]
                           k8s.v1.cni.cncf.io/networks-status:
                             [{
                                 &quot;name&quot;: &quot;&quot;,
                                 &quot;interface&quot;: &quot;eth0&quot;,
                                 &quot;ips&quot;: [
                                     &quot;10.9.0.36&quot;
                                 ],
                                 &quot;default&quot;: true,
                                 &quot;dns&quot;: {}
                             }]
                           kubernetes.io/limit-ranger: LimitRanger plugin set: cpu request for container i-like-linux; cpu limit for container i-like-linux
                           openshift.io/generated-by: OpenShiftNewApp
                           openshift.io/scc: restricted
Status:                    Terminating (lasts 104s)
Termination Grace Period:  30s
IP:                        10.9.0.36
IPs:
  IP:           10.9.0.36
Controlled By:  ReplicaSet/i-like-linux-7864d55cc4
Containers:
  i-like-linux:
    Container ID:   cri-o://938988bd1c1d2b6ab98b579887c9a9b0897b09b463b792bc83a8415d81541cb8
    Image:          bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67
    Image ID:       docker.io/bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67
    Ports:          8080/TCP, 8443/TCP
    Host Ports:     0/TCP, 0/TCP
    State:          Terminated
      Reason:       Completed
      Exit Code:    0
      Started:      Fri, 04 Nov 2022 23:35:48 -0400
      Finished:     Fri, 04 Nov 2022 23:37:14 -0400
    Ready:          False
    Restart Count:  0
    Limits:
      cpu:  50m
    Requests:
      cpu:        50m
    Environment:  &lt;none&gt;
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-svcb6 (ro)
Conditions:
  Type              Status
  Initialized       True 
  Ready             False 
  ContainersReady   False 
  PodScheduled      True 
Volumes:
  default-token-svcb6:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  default-token-svcb6
    Optional:    false
QoS Class:       Burstable
Node-Selectors:  &lt;none&gt;
Tolerations:     node.kubernetes.io/memory-pressure:NoSchedule op=Exists
                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                 node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type    Reason          Age    From               Message
  ----    ------          ----   ----               -------
  Normal  Scheduled       3m57s  default-scheduler  Successfully assigned tainted-love/i-like-linux-7864d55cc4-wlvt6 to master02
  Normal  AddedInterface  3m55s  multus             Add eth0 [10.9.0.36/23]
  Normal  Pulling         3m50s  kubelet            Pulling image &quot;bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67&quot;
  Normal  Pulled          3m41s  kubelet            Successfully pulled image &quot;bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67&quot; in 8.863325738s
  Normal  Created         3m39s  kubelet            Created container i-like-linux
  Normal  Started         3m39s  kubelet            Started container i-like-linux
  Normal  Killing         2m14s  kubelet            Stopping container i-like-linux
[student@workstation tasks]$ oc get pods
NAME                            READY   STATUS        RESTARTS   AGE
i-like-linux-7864d55cc4-ktb8s   0/1     Pending       0          2m29s
i-like-linux-7864d55cc4-wlvt6   0/1     Terminating   0          4m13s
[student@workstation tasks]$ oc get deployment i-like-linux -o yaml &gt; tolerate_app.yaml
[student@workstation tasks]$ vi tolerate_app.yaml 
[student@workstation tasks]$ vi tolerate_app.yaml 
[student@workstation tasks]$ oc apply -f tolerate_app.yaml
Warning: oc apply should be used on resource created by either oc create --save-config or oc apply
deployment.apps/i-like-linux configured
[student@workstation tasks]$ oc get pods
NAME                            READY   STATUS              RESTARTS   AGE
i-like-linux-5979857ff4-tmc6c   0/1     ContainerCreating   0          15s
i-like-linux-7864d55cc4-ktb8s   0/1     Pending             0          7m10s
[student@workstation tasks]$ oc get pods
NAME                            READY   STATUS    RESTARTS   AGE
i-like-linux-5979857ff4-tmc6c   1/1     Running   0          25s
[student@workstation tasks]$ oc describe pod i-like-linux-5979857ff4-tmc6c 
Name:         i-like-linux-5979857ff4-tmc6c
Namespace:    tainted-love
Priority:     0
Node:         master03/192.168.50.12
Start Time:   Fri, 04 Nov 2022 23:44:08 -0400
Labels:       deployment=i-like-linux
              pod-template-hash=5979857ff4
Annotations:  k8s.v1.cni.cncf.io/network-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.10.0.41&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              k8s.v1.cni.cncf.io/networks-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.10.0.41&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              kubernetes.io/limit-ranger: LimitRanger plugin set: cpu request for container i-like-linux; cpu limit for container i-like-linux
              openshift.io/generated-by: OpenShiftNewApp
              openshift.io/scc: restricted
Status:       Running
IP:           10.10.0.41
IPs:
  IP:           10.10.0.41
Controlled By:  ReplicaSet/i-like-linux-5979857ff4
Containers:
  i-like-linux:
    Container ID:   cri-o://4f5c3a0e72005c8d64b6f76750fad4bf661a3de2ad80eb83358c380e05a1379f
    Image:          bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67
    Image ID:       docker.io/bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67
    Ports:          8080/TCP, 8443/TCP
    Host Ports:     0/TCP, 0/TCP
    State:          Running
      Started:      Fri, 04 Nov 2022 23:44:25 -0400
    Ready:          True
    Restart Count:  0
    Limits:
      cpu:  50m
    Requests:
      cpu:        50m
    Environment:  &lt;none&gt;
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-svcb6 (ro)
Conditions:
  Type              Status
  Initialized       True 
  Ready             True 
  ContainersReady   True 
  PodScheduled      True 
Volumes:
  default-token-svcb6:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  default-token-svcb6
    Optional:    false
QoS Class:       Burstable
Node-Selectors:  &lt;none&gt;
Tolerations:     linux=good:NoSchedule
                 node.kubernetes.io/memory-pressure:NoSchedule op=Exists
                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                 node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type    Reason          Age   From               Message
  ----    ------          ----  ----               -------
  Normal  Scheduled       36s   default-scheduler  Successfully assigned tainted-love/i-like-linux-5979857ff4-tmc6c to master03
  Normal  AddedInterface  34s   multus             Add eth0 [10.10.0.41/23]
  Normal  Pulling         29s   kubelet            Pulling image &quot;bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67&quot;
  Normal  Pulled          21s   kubelet            Successfully pulled image &quot;bitnami/nginx@sha256:5c59f16d6fadf17400163ffb7d2f7af99b5a9b4081684aaccb3a930edd30aa67&quot; in 8.045264067s
  Normal  Created         19s   kubelet            Created container i-like-linux
  Normal  Started         19s   kubelet            Started container i-like-linux
[student@workstation tasks]$ oc adm taint node master02  linux=good:NoExecute-
node/master02 untainted
[student@workstation tasks]$ oc adm taint node master01  linux=good:NoExecute-
node/master01 untainted
[student@workstation tasks]$ oc adm taint node master03  linux=good:NoSchedule-
node/master03 untainted
[student@workstation tasks]$ oc get nodes
NAME       STATUS   ROLES           AGE    VERSION
master01   Ready    master,worker   479d   v1.19.0+b00ba52
master02   Ready    master,worker   479d   v1.19.0+b00ba52
master03   Ready    master,worker   479d   v1.19.0+b00ba52
[student@workstation tasks]$ git status
On branch main
Your branch is up to date with &apos;origin/main&apos;.

Untracked files:
  (use &quot;git add &lt;file&gt;...&quot; to include in what will be committed)

	<font color="#CC0000">template-by-sidd.yaml</font>
	<font color="#CC0000">tolerate_app.yaml</font>

nothing added to commit but untracked files present (use &quot;git add&quot; to track)
[student@workstation tasks]$ 
</pre>
