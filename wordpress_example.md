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
[student@workstation tasks]$ vi taints_tolerations.md
[student@workstation tasks]$ git add .
[student@workstation tasks]$ git commit -m &quot;added taint, project template excercise&quot;
[main 5c3f632] added taint, project template excercise
 Committer: Student User &lt;student@workstation.lab.example.com&gt;
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name &quot;Your Name&quot;
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 3 files changed, 825 insertions(+)
 create mode 100644 taints_tolerations.md
 create mode 100644 template-by-sidd.yaml
 create mode 100644 tolerate_app.yaml
[student@workstation tasks]$ git push
Username for &apos;https://github.com&apos;: Mostarijullah
Password for &apos;https://Mostarijullah@github.com&apos;: 
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 2 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 6.80 KiB | 6.80 MiB/s, done.
Total 5 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Mostarijullah/tasks.git
   0474be6..5c3f632  main -&gt; main
[student@workstation tasks]$ histroy
bash: histroy: command not found...
[student@workstation tasks]$ history 
    1  pwd
    2  lab auth-provider 
    3  lab auth-provider start
    4  oc whoami
    5  cd /usr/local/etc/
    6  ls
    7  cat ocp4.
    8  cat ocp4.config 
    9  oc login -u kubeadmin -p waoWn-5S9VM-6cSsy-kMAyk https://api.ocp4.example.com:6443
   10  clear
   11  cd ~
   12  pwd
   13  oc whoami
   14  oc whoami --show-console
   15  sudo yum install httpd-tools
   16  ls
   17  cd DO280/
   18  ls
   19  cd labs/
   20  ls
   21  cd auth-provider/
   22  ls
   23  htpasswd -c -B -b htpasswd-file Michael redhat
   24  htpasswd -B -b htpasswd-file Pam redhat
   25  htpasswd -B -b htpasswd-file Dwight redhat
   26  htpasswd -B -b htpasswd-file Jim redhat
   27  htpasswd -B -b htpasswd-file admin redhat
   28  htpasswd -B -b htpasswd-file Sidd redhat
   29  cat htpasswd-file 
   30  oc create secret generic htpasswd-source --from-file=htpasswd=htpasswd-file -n openshift-config
   31  ls
   32  mv oauth.yaml oauth.yaml.bk 
   33  ls
   34  oc get oauth cluster -o yaml &gt; oauth.yaml
   35  ls
   36  vi oauth.yaml
   37  watch oc get pods -n openshift-authentication
   38  oc replace -f oauth.yaml 
   39  watch oc get pods -n openshift-authentication
   40  oc adm policy add-cluster-role-to-user cluster-admin admin
   41  oc get users
   42  oc get identity
   43  watch oc get pods -n openshift-authentication
   44  oc login -u admin -p redhat
   45  oc get users
   46  oc get identity
   47  oc adm groups new managers
   48  oc adm groups add-users managers Michael
   49  oc get groups
   50  oc adm groups new sales Jim Dwight
   51  oc get groups
   52  oc adm groups new reception Pam
   53  oc get groups
   54  oc adm groups add-users managers Sidd
   55  oc new-project sales
   56  oc adm policy add-role-to-group edit sales   --namespace sales
   57  oc adm policy add-role-to-group view reception --namespace sales
   58  oc describe rolebinding.rbac -n sale
   59  oc describe rolebinding.rbac -n sales
   60  oc adm policy add-role-to-group admin managers --namespace sales
   61  oc describe rolebinding.rbac -n sales
   62  oc whoami
   63  oc delete secrets kubeadmin -n kube-system
   64  cd ..
   65  ls
   66  cd ..
   67  git clone https://github.com/Mostarijullah/tasks.git
   68  cd tasks/
   69  ls
   70  vi Manage_users__policies_groups_permissions.md
   71  git status 
   72  git add .
   73  git commit -m &quot;added excercise for managing users, roles and permission&quot;
   74  git config --global credential.helper &apos;cache --timeout=3600&apos;
   75  git push
   76  ls
   77  clear
   78  oc describe clusterrolebindings self-provisioners
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
  149  oc -u admin -p redhat
  150  oc login -u admin -p redhat
  151  oc get groups
  152  oc login -u Jim -p redhat
  153  oc new-project proj-creation-test01
  154  oc login -u Pam -p redhat
  155  oc new-project proj-creation-test01
  156  oc login -u Michael -p redhat
  157  oc new-project proj-creation-test01
  158  oc login -u admin -p redhat
  159  oc adm policy add-cluster-role-to-group --rolebinding-name=self-provisioners  self-provisioner system:authenticated:oauth
  160  oc whoami
  161  oc describe clusterrolebindings self-provisioners
  162  ls
  163  cd tasks/
  164  oc login -u admin -p redhat
  165  cat /usr/local/etc/ocp4.config 
  166  oc login -u admin -p redhat https://api.ocp4.example.com:6443
  167  oc get nodes -o wide
  168  oc get ns
  169  o get co
  170  oc get co
  171  oc adm taint node master03  linux=good:NoSchedule
  172  oc new-project tainted-love
  173   oc new-app --name i-like-linux --docker-image bitnami/nginx
  174  oc get pod
  175  oc describe pod i-like-linux-7864d55cc4-n6wp7 
  176  oc adm taint node master01  linux=good:NoExecute
  177  oc get pod
  178  oc describe pod i-like-linux-7864d55cc4-wlvt6 
  179  oc adm taint node master02  linux=good:NoExecute
  180  oc get pod
  181  oc get nodes -o wide
  182  oc get nodes
  183  oc get pods
  184  watch oc get pods
  185  oc describe pod i-like-linux-7864d55cc4-ktb8s 
  186  oc describe pod i-like-linux-7864d55cc4-wlvt6 
  187  oc get pods
  188  oc get deployment i-like-linux -o yaml &gt; tolerate_app.yaml
  189  vi tolerate_app.yaml 
  190  oc apply -f tolerate_app.yaml
  191  oc get pods
  192  oc describe pod i-like-linux-5979857ff4-tmc6c 
  193  oc adm taint node master02  linux=good:NoExecute-
  194  oc adm taint node master01  linux=good:NoExecute-
  195  oc adm taint node master03  linux=good:NoSchedule-
  196  oc get nodes
  197  git status
  198  vi taints_tolerations.md
  199  git add .
  200  git commit -m &quot;added taint, project template excercise&quot;
  201  git push
  202  histroy
  203  history 
[student@workstation tasks]$  oc get templates.template.openshift.io -n openshift-config
NAME               DESCRIPTION   PARAMETERS    OBJECTS
template-by-sidd                 5 (5 blank)   3
[student@workstation tasks]$ oc edit projects cluster
Error from server (NotFound): namespaces &quot;cluster&quot; not found
[student@workstation tasks]$ oc edit template cluster
Error from server (NotFound): templates.template.openshift.io &quot;cluster&quot; not found
[student@workstation tasks]$ oc edit projects.config.openshift.io/cluster
Edit cancelled, no changes made.
[student@workstation tasks]$ oc whoami
admin
[student@workstation tasks]$ oc login -u Sidd -p redhat
Login successful.

You have access to the following projects and can switch between them with &apos; project &lt;projectname&gt;&apos;:

  * proj-creation-test
    sales

Using project &quot;proj-creation-test&quot;.
[student@workstation tasks]$ oc create new-project wordpress-proj
Error: must specify one of -f and -k

error: unknown command &quot;new-project wordpress-proj&quot;
See &apos;oc create -h&apos; for help and examples
[student@workstation tasks]$ oc new-project wordpress-proj
Now using project &quot;wordpress-proj&quot; on server &quot;https://api.ocp4.example.com:6443&quot;.

You can add applications to this project with the &apos;new-app&apos; command. For example, try:

    oc new-app rails-postgresql-example

to build a new example application in Ruby. Or use kubectl to deploy a simple Kubernetes application:

    kubectl create deployment hello-node --image=k8s.gcr.io/serve_hostname

[student@workstation tasks]$ oc create secret generic mysql --from-literal=password=redhat
secret/mysql created
[student@workstation tasks]$ oc new-app --name mysql --docker-image=registry.redhat.io/rhel8/mysql-80:1-139
--&gt; Found container image a2a7718 (17 months old) from registry.redhat.io for &quot;registry.redhat.io/rhel8/mysql-80:1-139&quot;

    MySQL 8.0 
    --------- 
    MySQL is a multi-user, multi-threaded SQL database server. The container image provides a containerized packaging of the MySQL mysqld daemon and client application. The mysqld server daemon accepts connections from clients and provides access to content from MySQL databases on behalf of the clients.

    Tags: database, mysql, mysql80, mysql-80

    * An image stream tag will be created as &quot;mysql:1-139&quot; that will track this image

--&gt; Creating resources ...
    imagestream.image.openshift.io &quot;mysql&quot; created
    deployment.apps &quot;mysql&quot; created
    service &quot;mysql&quot; created
--&gt; Success
    Application is not exposed. You can expose services to the outside world by executing one or more of the commands below:
     &apos;oc expose service/mysql&apos; 
    Run &apos;oc status&apos; to view your app.
[student@workstation tasks]$ oc set env deployment/mysql --from=secret/mysql --prefix=MYSQL_ROOT_
deployment.apps/mysql updated
[student@workstation tasks]$ vi config.env
[student@workstation tasks]$ oc whoami --show-console
https://console-openshift-console.apps.ocp4.example.com
[student@workstation tasks]$ cat /usr/local/etc/ocp4.config 
RHT_OCP4_MASTER_API=https://api.ocp4.example.com:6443
RHT_OCP4_WILDCARD_DOMAIN=apps.ocp4.example.com
RHT_OCP4_KUBEADM_PASSWD=waoWn-5S9VM-6cSsy-kMAyk
RHT_OCP4_USER_PASSWD=redhat
[student@workstation tasks]$ vi config.env 
[student@workstation tasks]$ oc create configmap wordpress-config --from-env-file=config.env
configmap/wordpress-config created
[student@workstation tasks]$ oc set volumes deployment/mysql --add --name=mysql-storage --type pvc --claim-size=2Gi --claim-mode=rwo --mount-path=/var/lib/mysql/data
deployment.apps/mysql volume updated
[student@workstation tasks]$ oc new-app --name wordpress --docker-image=quay.io/redhattraining/wordpress:5.7-php7.4-apache
--&gt; Found container image 4d3c70b (16 months old) from quay.io for &quot;quay.io/redhattraining/wordpress:5.7-php7.4-apache&quot;

    * An image stream tag will be created as &quot;wordpress:5.7-php7.4-apache&quot; that will track this image

--&gt; Creating resources ...
    imagestream.image.openshift.io &quot;wordpress&quot; created
    deployment.apps &quot;wordpress&quot; created
    service &quot;wordpress&quot; created
--&gt; Success
    Application is not exposed. You can expose services to the outside world by executing one or more of the commands below:
     &apos;oc expose service/wordpress&apos; 
    Run &apos;oc status&apos; to view your app.
[student@workstation tasks]$ oc create sa wordpress-sa
serviceaccount/wordpress-sa created
[student@workstation tasks]$ oc adm policy add-scc-to-user anyuid -z wordpress-sa
Error from server (Forbidden): clusterrolebindings.rbac.authorization.k8s.io &quot;system:openshift:scc:anyuid&quot; is forbidden: User &quot;Sidd&quot; cannot get resource &quot;clusterrolebindings&quot; in API group &quot;rbac.authorization.k8s.io&quot; at the cluster scope
[student@workstation tasks]$ oc login -u admin -p redhat
Login successful.

You have access to 65 projects, the list has been suppressed. You can list all projects with &apos; projects&apos;

Using project &quot;wordpress-proj&quot;.
[student@workstation tasks]$ oc adm policy add-scc-to-user anyuid -z wordpress-sa
clusterrole.rbac.authorization.k8s.io/system:openshift:scc:anyuid added: &quot;wordpress-sa&quot;
[student@workstation tasks]$ oc login -u Sidd -p redhat
Login successful.

You have access to the following projects and can switch between them with &apos; project &lt;projectname&gt;&apos;:

    proj-creation-test
    sales
  * wordpress-proj

Using project &quot;wordpress-proj&quot;.
[student@workstation tasks]$ oc set serviceaccount deployment/wordpress wordpress-sa
deployment.apps/wordpress serviceaccount updated
[student@workstation tasks]$ oc get all
NAME                             READY   STATUS    RESTARTS   AGE
pod/mysql-bc88f5c8-mmxsg         1/1     Running   0          3m12s
pod/wordpress-76b6b4565d-wm6vb   0/1     Error     2          50s

NAME                TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)    AGE
service/mysql       ClusterIP   172.30.168.145   &lt;none&gt;        3306/TCP   8m59s
service/wordpress   ClusterIP   172.30.199.124   &lt;none&gt;        80/TCP     2m26s

NAME                        READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/mysql       1/1     1            1           8m59s
deployment.apps/wordpress   0/1     1            0           2m26s

NAME                                   DESIRED   CURRENT   READY   AGE
replicaset.apps/mysql-64d9f4d857       0         0         0       8m58s
replicaset.apps/mysql-77c9c667d5       0         0         0       8m59s
replicaset.apps/mysql-bc88f5c8         1         1         1       3m12s
replicaset.apps/mysql-fbf67ff96        0         0         0       8m32s
replicaset.apps/wordpress-66f777db74   0         0         0       2m25s
replicaset.apps/wordpress-76b6b4565d   1         1         0       50s
replicaset.apps/wordpress-fb6d85d7f    0         0         0       2m26s

NAME                                       IMAGE REPOSITORY                                                            TAGS                UPDATED
imagestream.image.openshift.io/mysql       image-registry.openshift-image-registry.svc:5000/wordpress-proj/mysql       1-139               8 minutes ago
imagestream.image.openshift.io/wordpress   image-registry.openshift-image-registry.svc:5000/wordpress-proj/wordpress   5.7-php7.4-apache   2 minutes ago
[student@workstation tasks]$ oc get events
LAST SEEN   TYPE      REASON                  OBJECT                            MESSAGE
9m15s       Normal    Scheduled               pod/mysql-64d9f4d857-r7fcv        Successfully assigned wordpress-proj/mysql-64d9f4d857-r7fcv to master01
9m12s       Normal    AddedInterface          pod/mysql-64d9f4d857-r7fcv        Add eth0 [10.8.0.24/23]
9m8s        Normal    Pulling                 pod/mysql-64d9f4d857-r7fcv        Pulling image &quot;registry.redhat.io/rhel8/mysql-80@sha256:1c65c90a5ffc40d0454d27e6c8a13b7a746a08ea151ed24edce96c61aeb28801&quot;
8m56s       Normal    Pulled                  pod/mysql-64d9f4d857-r7fcv        Successfully pulled image &quot;registry.redhat.io/rhel8/mysql-80@sha256:1c65c90a5ffc40d0454d27e6c8a13b7a746a08ea151ed24edce96c61aeb28801&quot; in 11.528338711s
8m52s       Normal    Created                 pod/mysql-64d9f4d857-r7fcv        Created container mysql
8m52s       Normal    Started                 pod/mysql-64d9f4d857-r7fcv        Started container mysql
8m53s       Normal    Pulled                  pod/mysql-64d9f4d857-r7fcv        Container image &quot;registry.redhat.io/rhel8/mysql-80@sha256:1c65c90a5ffc40d0454d27e6c8a13b7a746a08ea151ed24edce96c61aeb28801&quot; already present on machine
8m49s       Warning   BackOff                 pod/mysql-64d9f4d857-r7fcv        Back-off restarting failed container
9m15s       Normal    SuccessfulCreate        replicaset/mysql-64d9f4d857       Created pod: mysql-64d9f4d857-r7fcv
8m40s       Normal    SuccessfulDelete        replicaset/mysql-64d9f4d857       Deleted pod: mysql-64d9f4d857-r7fcv
9m16s       Warning   FailedCreate            replicaset/mysql-77c9c667d5       Error creating: Pod &quot;mysql-77c9c667d5-p4ch4&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
9m16s       Warning   FailedCreate            replicaset/mysql-77c9c667d5       Error creating: Pod &quot;mysql-77c9c667d5-5nbmx&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
9m16s       Warning   FailedCreate            replicaset/mysql-77c9c667d5       Error creating: Pod &quot;mysql-77c9c667d5-m7c79&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
9m16s       Warning   FailedCreate            replicaset/mysql-77c9c667d5       Error creating: Pod &quot;mysql-77c9c667d5-sx7b8&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
9m16s       Warning   FailedCreate            replicaset/mysql-77c9c667d5       Error creating: Pod &quot;mysql-77c9c667d5-7hf4q&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
9m16s       Warning   FailedCreate            replicaset/mysql-77c9c667d5       Error creating: Pod &quot;mysql-77c9c667d5-rrf79&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
9m16s       Warning   FailedCreate            replicaset/mysql-77c9c667d5       Error creating: Pod &quot;mysql-77c9c667d5-g9snq&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
9m15s       Warning   FailedCreate            replicaset/mysql-77c9c667d5       Error creating: Pod &quot;mysql-77c9c667d5-vsn8z&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
9m15s       Warning   FailedCreate            replicaset/mysql-77c9c667d5       Error creating: Pod &quot;mysql-77c9c667d5-k28m8&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
8m56s       Warning   FailedCreate            replicaset/mysql-77c9c667d5       (combined from similar events): Error creating: Pod &quot;mysql-77c9c667d5-zb6gl&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
3m29s       Normal    Scheduled               pod/mysql-bc88f5c8-mmxsg          Successfully assigned wordpress-proj/mysql-bc88f5c8-mmxsg to master01
3m26s       Normal    AddedInterface          pod/mysql-bc88f5c8-mmxsg          Add eth0 [10.8.0.27/23]
3m22s       Normal    Pulled                  pod/mysql-bc88f5c8-mmxsg          Container image &quot;registry.redhat.io/rhel8/mysql-80@sha256:1c65c90a5ffc40d0454d27e6c8a13b7a746a08ea151ed24edce96c61aeb28801&quot; already present on machine
3m20s       Normal    Created                 pod/mysql-bc88f5c8-mmxsg          Created container mysql
3m20s       Normal    Started                 pod/mysql-bc88f5c8-mmxsg          Started container mysql
3m29s       Normal    SuccessfulCreate        replicaset/mysql-bc88f5c8         Created pod: mysql-bc88f5c8-mmxsg
8m49s       Normal    Scheduled               pod/mysql-fbf67ff96-t6v2t         Successfully assigned wordpress-proj/mysql-fbf67ff96-t6v2t to master01
8m46s       Normal    AddedInterface          pod/mysql-fbf67ff96-t6v2t         Add eth0 [10.8.0.25/23]
8m42s       Normal    Pulled                  pod/mysql-fbf67ff96-t6v2t         Container image &quot;registry.redhat.io/rhel8/mysql-80@sha256:1c65c90a5ffc40d0454d27e6c8a13b7a746a08ea151ed24edce96c61aeb28801&quot; already present on machine
8m41s       Normal    Created                 pod/mysql-fbf67ff96-t6v2t         Created container mysql
8m40s       Normal    Started                 pod/mysql-fbf67ff96-t6v2t         Started container mysql
3m20s       Normal    Killing                 pod/mysql-fbf67ff96-t6v2t         Stopping container mysql
8m49s       Normal    SuccessfulCreate        replicaset/mysql-fbf67ff96        Created pod: mysql-fbf67ff96-t6v2t
3m20s       Normal    SuccessfulDelete        replicaset/mysql-fbf67ff96        Deleted pod: mysql-fbf67ff96-t6v2t
9m16s       Normal    ScalingReplicaSet       deployment/mysql                  Scaled up replica set mysql-77c9c667d5 to 1
9m15s       Normal    ScalingReplicaSet       deployment/mysql                  Scaled up replica set mysql-64d9f4d857 to 1
8m54s       Normal    ScalingReplicaSet       deployment/mysql                  Scaled down replica set mysql-77c9c667d5 to 0
8m49s       Normal    ScalingReplicaSet       deployment/mysql                  Scaled up replica set mysql-fbf67ff96 to 1
8m40s       Normal    ScalingReplicaSet       deployment/mysql                  Scaled down replica set mysql-64d9f4d857 to 0
3m29s       Normal    ScalingReplicaSet       deployment/mysql                  Scaled up replica set mysql-bc88f5c8 to 1
3m20s       Normal    ScalingReplicaSet       deployment/mysql                  Scaled down replica set mysql-fbf67ff96 to 0
3m29s       Normal    ExternalProvisioning    persistentvolumeclaim/pvc-56xlf   waiting for a volume to be created, either by external provisioner &quot;nfs-storage-provisioner&quot; or manually created by system administrator
3m29s       Normal    Provisioning            persistentvolumeclaim/pvc-56xlf   External provisioner is provisioning volume for claim &quot;wordpress-proj/pvc-56xlf&quot;
3m29s       Normal    ProvisioningSucceeded   persistentvolumeclaim/pvc-56xlf   Successfully provisioned volume pvc-eb6b8f9c-dea3-4b04-afb3-737877805e83
2m42s       Normal    Scheduled               pod/wordpress-66f777db74-hlw64    Successfully assigned wordpress-proj/wordpress-66f777db74-hlw64 to master01
2m40s       Normal    AddedInterface          pod/wordpress-66f777db74-hlw64    Add eth0 [10.8.0.28/23]
2m35s       Normal    Pulling                 pod/wordpress-66f777db74-hlw64    Pulling image &quot;quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b&quot;
2m15s       Normal    Pulled                  pod/wordpress-66f777db74-hlw64    Successfully pulled image &quot;quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b&quot; in 19.673207657s
64s         Normal    Created                 pod/wordpress-66f777db74-hlw64    Created container wordpress
64s         Normal    Started                 pod/wordpress-66f777db74-hlw64    Started container wordpress
66s         Normal    Pulled                  pod/wordpress-66f777db74-hlw64    Container image &quot;quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b&quot; already present on machine
61s         Warning   BackOff                 pod/wordpress-66f777db74-hlw64    Back-off restarting failed container
2m42s       Normal    SuccessfulCreate        replicaset/wordpress-66f777db74   Created pod: wordpress-66f777db74-hlw64
58s         Normal    SuccessfulDelete        replicaset/wordpress-66f777db74   Deleted pod: wordpress-66f777db74-hlw64
67s         Normal    Scheduled               pod/wordpress-76b6b4565d-wm6vb    Successfully assigned wordpress-proj/wordpress-76b6b4565d-wm6vb to master01
65s         Normal    AddedInterface          pod/wordpress-76b6b4565d-wm6vb    Add eth0 [10.8.0.29/23]
26s         Normal    Pulled                  pod/wordpress-76b6b4565d-wm6vb    Container image &quot;quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b&quot; already present on machine
24s         Normal    Created                 pod/wordpress-76b6b4565d-wm6vb    Created container wordpress
24s         Normal    Started                 pod/wordpress-76b6b4565d-wm6vb    Started container wordpress
8s          Warning   BackOff                 pod/wordpress-76b6b4565d-wm6vb    Back-off restarting failed container
67s         Normal    SuccessfulCreate        replicaset/wordpress-76b6b4565d   Created pod: wordpress-76b6b4565d-wm6vb
2m43s       Warning   FailedCreate            replicaset/wordpress-fb6d85d7f    Error creating: Pod &quot;wordpress-fb6d85d7f-wzj2g&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
2m43s       Warning   FailedCreate            replicaset/wordpress-fb6d85d7f    Error creating: Pod &quot;wordpress-fb6d85d7f-xtzkm&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
2m43s       Warning   FailedCreate            replicaset/wordpress-fb6d85d7f    Error creating: Pod &quot;wordpress-fb6d85d7f-hkhrr&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
2m43s       Warning   FailedCreate            replicaset/wordpress-fb6d85d7f    Error creating: Pod &quot;wordpress-fb6d85d7f-rjtq5&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
2m43s       Warning   FailedCreate            replicaset/wordpress-fb6d85d7f    Error creating: Pod &quot;wordpress-fb6d85d7f-n4qr7&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
2m43s       Warning   FailedCreate            replicaset/wordpress-fb6d85d7f    Error creating: Pod &quot;wordpress-fb6d85d7f-qq72s&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
2m43s       Warning   FailedCreate            replicaset/wordpress-fb6d85d7f    Error creating: Pod &quot;wordpress-fb6d85d7f-klw5d&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
2m42s       Warning   FailedCreate            replicaset/wordpress-fb6d85d7f    Error creating: Pod &quot;wordpress-fb6d85d7f-v4qml&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
2m42s       Warning   FailedCreate            replicaset/wordpress-fb6d85d7f    Error creating: Pod &quot;wordpress-fb6d85d7f-8c9j6&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
2m23s       Warning   FailedCreate            replicaset/wordpress-fb6d85d7f    (combined from similar events): Error creating: Pod &quot;wordpress-fb6d85d7f-6xh86&quot; is invalid: spec.containers[0].image: Invalid value: &quot; &quot;: must not have leading or trailing whitespace
2m43s       Normal    ScalingReplicaSet       deployment/wordpress              Scaled up replica set wordpress-fb6d85d7f to 1
2m42s       Normal    ScalingReplicaSet       deployment/wordpress              Scaled up replica set wordpress-66f777db74 to 1
2m14s       Normal    ScalingReplicaSet       deployment/wordpress              Scaled down replica set wordpress-fb6d85d7f to 0
67s         Normal    ScalingReplicaSet       deployment/wordpress              Scaled up replica set wordpress-76b6b4565d to 1
58s         Normal    ScalingReplicaSet       deployment/wordpress              Scaled down replica set wordpress-66f777db74 to 0
[student@workstation tasks]$ oc describe pod wordpress-76b6b4565d-wm6vb 
Name:         wordpress-76b6b4565d-wm6vb
Namespace:    wordpress-proj
Priority:     0
Node:         master01/192.168.50.10
Start Time:   Sat, 05 Nov 2022 01:56:04 -0400
Labels:       deployment=wordpress
              pod-template-hash=76b6b4565d
Annotations:  k8s.v1.cni.cncf.io/network-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.8.0.29&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              k8s.v1.cni.cncf.io/networks-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.8.0.29&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              kubernetes.io/limit-ranger: LimitRanger plugin set: cpu request for container wordpress; cpu limit for container wordpress
              openshift.io/generated-by: OpenShiftNewApp
              openshift.io/scc: anyuid
Status:       Running
IP:           10.8.0.29
IPs:
  IP:           10.8.0.29
Controlled By:  ReplicaSet/wordpress-76b6b4565d
Containers:
  wordpress:
    Container ID:   cri-o://f0b3e0b12cdb0aa56b6fc86b50299630cfafecfdf5bb6c5b4eb18ba5f686bec6
    Image:          quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b
    Image ID:       quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b
    Port:           80/TCP
    Host Port:      0/TCP
    State:          Waiting
      Reason:       CrashLoopBackOff
    Last State:     Terminated
      Reason:       Error
      Exit Code:    1
      Started:      Sat, 05 Nov 2022 01:57:19 -0400
      Finished:     Sat, 05 Nov 2022 01:57:22 -0400
    Ready:          False
    Restart Count:  3
    Limits:
      cpu:  50m
    Requests:
      cpu:        50m
    Environment:  &lt;none&gt;
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from wordpress-sa-token-8krhp (ro)
      /var/www/html from wordpress-volume-1 (rw)
Conditions:
  Type              Status
  Initialized       True 
  Ready             False 
  ContainersReady   False 
  PodScheduled      True 
Volumes:
  wordpress-volume-1:
    Type:       EmptyDir (a temporary directory that shares a pod&apos;s lifetime)
    Medium:     
    SizeLimit:  &lt;unset&gt;
  wordpress-sa-token-8krhp:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  wordpress-sa-token-8krhp
    Optional:    false
QoS Class:       Burstable
Node-Selectors:  &lt;none&gt;
Tolerations:     node.kubernetes.io/memory-pressure:NoSchedule op=Exists
                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                 node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type     Reason          Age                From               Message
  ----     ------          ----               ----               -------
  Normal   Scheduled       97s                default-scheduler  Successfully assigned wordpress-proj/wordpress-76b6b4565d-wm6vb to master01
  Normal   AddedInterface  95s                multus             Add eth0 [10.8.0.29/23]
  Normal   Pulled          24s (x4 over 90s)  kubelet            Container image &quot;quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b&quot; already present on machine
  Normal   Created         22s (x4 over 88s)  kubelet            Created container wordpress
  Normal   Started         22s (x4 over 88s)  kubelet            Started container wordpress
  Warning  BackOff         8s (x5 over 70s)   kubelet            Back-off restarting failed container
[student@workstation tasks]$ oc logs wordpress-76b6b4565d-wm6vb 
apache2-foreground
Checking if WordPress is installed
Error: Error establishing a database connection. This either means that the username and password information in your `wp-config.php` file is incorrect or we can’t contact the database server at `mysql`. This could mean your host’s database server is down.
Installing WordPress with wpcli
/usr/local/bin/docker-entrypoint.sh: line 111: WORDPRESS_URL: unbound variable
[student@workstation tasks]$ oc exec mysql-bc88f5c8-mmxsg 
error: you must specify at least one command for the container
[student@workstation tasks]$ oc exec mysql-bc88f5c8-mmxsg -- /usr/bin/mysql -u root -e &apos;show databases;&apos;
Database
information_schema
mysql
performance_schema
sys
[student@workstation tasks]$ use mysql
bash: use: command not found...
[student@workstation tasks]$ use mysql;
bash: use: command not found...
[student@workstation tasks]$ use mysql();
bash: syntax error near unexpected token `(&apos;
[student@workstation tasks]$ show tables();
bash: syntax error near unexpected token `(&apos;
[student@workstation tasks]$ oc logs mysql-bc88f5c8-mmxsg 
=&gt; sourcing 20-validate-variables.sh ...
=&gt; sourcing 25-validate-replication-variables.sh ...
=&gt; sourcing 30-base-config.sh ...
---&gt; 05:53:52     Processing basic MySQL configuration files ...
=&gt; sourcing 60-replication-config.sh ...
=&gt; sourcing 70-s2i-config.sh ...
---&gt; 05:53:52     Processing additional arbitrary  MySQL configuration provided by s2i ...
=&gt; sourcing 20-default-authentication-plugin.cnf ...
=&gt; sourcing 40-paas.cnf ...
=&gt; sourcing 50-my-tuning.cnf ...
---&gt; 05:53:52     Initializing database ...
---&gt; 05:53:52     Running /usr/libexec/mysqld --initialize --datadir=/var/lib/mysql/data
---&gt; 05:54:45     Starting MySQL server with disabled networking ...
---&gt; 05:54:46     Waiting for MySQL to start ...
---&gt; 05:54:48     Waiting for MySQL to start ...
2022-11-05T05:54:49.054980Z 0 [Warning] [MY-011070] [Server] &apos;Disabling symbolic links using --skip-symbolic-links (or equivalent) is the default. Consider not using this option as it&apos; is deprecated and will be removed in a future release.
2022-11-05T05:54:49.156605Z 0 [System] [MY-010116] [Server] /usr/libexec/mysqld (mysqld 8.0.21) starting as process 81
2022-11-05T05:54:49.352319Z 1 [System] [MY-013576] [InnoDB] InnoDB initialization has started.
---&gt; 05:54:49     Waiting for MySQL to start ...
---&gt; 05:54:51     Waiting for MySQL to start ...
---&gt; 05:54:52     Waiting for MySQL to start ...
2022-11-05T05:54:53.450522Z 1 [System] [MY-013577] [InnoDB] InnoDB initialization has ended.
---&gt; 05:54:54     Waiting for MySQL to start ...
---&gt; 05:54:55     Waiting for MySQL to start ...
---&gt; 05:54:56     Waiting for MySQL to start ...
2022-11-05T05:54:56.952309Z 0 [System] [MY-011323] [Server] X Plugin ready for connections. Socket: /var/lib/mysql/mysqlx.sock
---&gt; 05:54:58     Waiting for MySQL to start ...
---&gt; 05:54:59     Waiting for MySQL to start ...
2022-11-05T05:55:01.880481Z 0 [Warning] [MY-010068] [Server] CA certificate ca.pem is self signed.
2022-11-05T05:55:01.880709Z 0 [System] [MY-013602] [Server] Channel mysql_main configured to support TLS. Encrypted connections are now supported for this channel.
---&gt; 05:55:01     Waiting for MySQL to start ...
2022-11-05T05:55:01.963937Z 0 [Warning] [MY-011810] [Server] Insecure configuration for --pid-file: Location &apos;/var/lib/mysql/data&apos; in the path is accessible to all OS users. Consider choosing a different directory.
2022-11-05T05:55:02.751753Z 0 [System] [MY-010931] [Server] /usr/libexec/mysqld: ready for connections. Version: &apos;8.0.21&apos;  socket: &apos;/tmp/mysql.sock&apos;  port: 0  Source distribution.
---&gt; 05:55:03     MySQL started successfully
---&gt; 05:55:03     Setting password for MySQL root user ...
mysql: [Warning] Using a password on the command line interface can be insecure.
The mysql_upgrade client is now deprecated. The actions executed by the upgrade client are now done by the server.
To upgrade, please start the new MySQL binary with the older data directory. Repairing user tables is done automatically. Restart is not required after upgrade.
The upgrade process automatically starts on running a new MySQL binary with an older data directory. To avoid accidental upgrades, please use the --upgrade=NONE option with the MySQL binary. The option --upgrade=FORCE is also provided to run the server upgrade sequence on demand.
It may be possible that the server upgrade fails due to a number of reasons. In that case, the upgrade sequence will run again during the next MySQL server start. If the server upgrade fails repeatedly, the server can be started with the --upgrade=MINIMAL option to start the server without executing the upgrade sequence, thus allowing users to manually rectify the problem.
---&gt; 05:55:04     Initialization finished
=&gt; sourcing 40-datadir-action.sh ...
---&gt; 05:55:04     Running datadir action: upgrade-warn
---&gt; 05:55:05     Warning: Version of the data could not be determined. It is because the file mysql_upgrade_info is missing in the data directory, which is most probably because it was not created when initialization of data directory. In order to allow seamless updates to the next higher version in the future, the file mysql_upgrade_info will be created. If the data directory was created with a different version than 8.0, it is required to run this container with the MYSQL_DATADIR_ACTION environment variable set to &apos;force&apos;, or run &apos;mysql_upgrade&apos; utility manually; the mysql_upgrade tool checks the tables and creates such a file as well. For upstream documentation about upgrading, see: https://dev.mysql.com/doc/refman/8.0/en/upgrading-from-previous-series.html
---&gt; 05:55:05     Storing version &apos;8.0.21&apos; information into the data dir &apos;/var/lib/mysql/data/mysql_upgrade_info&apos;
=&gt; sourcing 50-passwd-change.sh ...
---&gt; 05:55:05     Setting passwords ...
2022-11-05T05:55:06.053571Z 12 [Warning] [MY-010235] [Server] Following users were specified in CREATE USER IF NOT EXISTS but they already exist. Corresponding entry in binary log used default authentication plugin &apos;caching_sha2_password&apos; to rewrite authentication information (if any) for them: &apos;root&apos;@&apos;%&apos;
---&gt; 05:55:06     Shutting down MySQL ...
2022-11-05T05:55:06.458456Z 13 [System] [MY-013172] [Server] Received SHUTDOWN from user root. Shutting down mysqld (Version: 8.0.21).
2022-11-05T05:55:08.153147Z 0 [System] [MY-010910] [Server] /usr/libexec/mysqld: Shutdown complete (mysqld 8.0.21)  Source distribution.
---&gt; 05:55:08     Cleaning up environment variables MYSQL_USER, MYSQL_PASSWORD, MYSQL_DATABASE and MYSQL_ROOT_PASSWORD ...
---&gt; 05:55:08     Running final exec -- Only MySQL server logs after this point
2022-11-05T05:55:11.151754Z 0 [Warning] [MY-011070] [Server] &apos;Disabling symbolic links using --skip-symbolic-links (or equivalent) is the default. Consider not using this option as it&apos; is deprecated and will be removed in a future release.
2022-11-05T05:55:11.158792Z 0 [System] [MY-010116] [Server] /usr/libexec/mysqld (mysqld 8.0.21) starting as process 1
2022-11-05T05:55:11.449689Z 1 [System] [MY-013576] [InnoDB] InnoDB initialization has started.
2022-11-05T05:55:14.875115Z 1 [System] [MY-013577] [InnoDB] InnoDB initialization has ended.
2022-11-05T05:55:17.254210Z 0 [System] [MY-011323] [Server] X Plugin ready for connections. Bind-address: &apos;::&apos; port: 33060, socket: /var/lib/mysql/mysqlx.sock
2022-11-05T05:55:18.785051Z 0 [Warning] [MY-010068] [Server] CA certificate ca.pem is self signed.
2022-11-05T05:55:18.785268Z 0 [System] [MY-013602] [Server] Channel mysql_main configured to support TLS. Encrypted connections are now supported for this channel.
2022-11-05T05:55:19.066724Z 0 [Warning] [MY-011810] [Server] Insecure configuration for --pid-file: Location &apos;/var/lib/mysql/data&apos; in the path is accessible to all OS users. Consider choosing a different directory.
2022-11-05T05:55:19.451828Z 0 [System] [MY-010931] [Server] /usr/libexec/mysqld: ready for connections. Version: &apos;8.0.21&apos;  socket: &apos;/var/lib/mysql/mysql.sock&apos;  port: 3306  Source distribution.
2022-11-05T05:55:34.954019Z 8 [Warning] [MY-013360] [Server] Plugin sha256_password reported: &apos;&apos;sha256_password&apos; is deprecated and will be removed in a future release. Please use caching_sha2_password instead&apos;
2022-11-05T05:56:10.051964Z 9 [Warning] [MY-013360] [Server] Plugin sha256_password reported: &apos;&apos;sha256_password&apos; is deprecated and will be removed in a future release. Please use caching_sha2_password instead&apos;
2022-11-05T05:56:26.154931Z 10 [Warning] [MY-013360] [Server] Plugin sha256_password reported: &apos;&apos;sha256_password&apos; is deprecated and will be removed in a future release. Please use caching_sha2_password instead&apos;
2022-11-05T05:56:30.850211Z 11 [Warning] [MY-013360] [Server] Plugin sha256_password reported: &apos;&apos;sha256_password&apos; is deprecated and will be removed in a future release. Please use caching_sha2_password instead&apos;
2022-11-05T05:56:50.050464Z 12 [Warning] [MY-013360] [Server] Plugin sha256_password reported: &apos;&apos;sha256_password&apos; is deprecated and will be removed in a future release. Please use caching_sha2_password instead&apos;
2022-11-05T05:57:22.154693Z 13 [Warning] [MY-013360] [Server] Plugin sha256_password reported: &apos;&apos;sha256_password&apos; is deprecated and will be removed in a future release. Please use caching_sha2_password instead&apos;
2022-11-05T05:58:19.450881Z 14 [Warning] [MY-013360] [Server] Plugin sha256_password reported: &apos;&apos;sha256_password&apos; is deprecated and will be removed in a future release. Please use caching_sha2_password instead&apos;
2022-11-05T05:59:43.957816Z 15 [Warning] [MY-013360] [Server] Plugin sha256_password reported: &apos;&apos;sha256_password&apos; is deprecated and will be removed in a future release. Please use caching_sha2_password instead&apos;
2022-11-05T06:02:30.251856Z 17 [Warning] [MY-013360] [Server] Plugin sha256_password reported: &apos;&apos;sha256_password&apos; is deprecated and will be removed in a future release. Please use caching_sha2_password instead&apos;
[student@workstation tasks]$ oc exec mysql-bc88f5c8-mmxsg -- /usr/bin/mysql
ERROR 1045 (28000): Access denied for user &apos;1000620000&apos;@&apos;localhost&apos; (using password: NO)
command terminated with exit code 1
[student@workstation tasks]$ oc exec mysql-bc88f5c8-mmxsg -- /usr/bin/mysql -u root
[student@workstation tasks]$ oc exec mysql-bc88f5c8-mmxsg -- /usr/bin/mysql -u root -p
Enter password: [student@workstation tasks]$ oc exec -it mysql-bc88f5c8-mmxsg -- /usr/bin/mysql -u root
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 21
Server version: 8.0.21 Source distribution

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type &apos;help;&apos; or &apos;\h&apos; for help. Type &apos;\c&apos; to clear the current input statement.

mysql&gt; show databases();
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near &apos;()&apos; at line 1
mysql&gt; show databases()
    -&gt; ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near &apos;()&apos; at line 1
mysql&gt; show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
4 rows in set (0.01 sec)

mysql&gt; create database[student@workstation tasks]$ 
[student@workstation tasks]$ oc exec -it mysql-bc88f5c8-mmxsg -- /usr/bin/mysql -u root
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 22
Server version: 8.0.21 Source distribution

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type &apos;help;&apos; or &apos;\h&apos; for help. Type &apos;\c&apos; to clear the current input statement.

mysql&gt; create database wordpress;
Query OK, 1 row affected (0.02 sec)

mysql&gt; show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
| wordpress          |
+--------------------+
5 rows in set (0.01 sec)

mysql&gt; use wordpress
Database changed
mysql&gt; who tables;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near &apos;who tables&apos; at line 1
mysql&gt; who tables();
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near &apos;who tables()&apos; at line 1
mysql&gt; exit
Bye
[student@workstation tasks]$ oc get all;
NAME                             READY   STATUS             RESTARTS   AGE
pod/mysql-bc88f5c8-mmxsg         1/1     Running            0          13m
pod/wordpress-76b6b4565d-wm6vb   0/1     CrashLoopBackOff   6          11m

NAME                TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)    AGE
service/mysql       ClusterIP   172.30.168.145   &lt;none&gt;        3306/TCP   19m
service/wordpress   ClusterIP   172.30.199.124   &lt;none&gt;        80/TCP     13m

NAME                        READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/mysql       1/1     1            1           19m
deployment.apps/wordpress   0/1     1            0           13m

NAME                                   DESIRED   CURRENT   READY   AGE
replicaset.apps/mysql-64d9f4d857       0         0         0       19m
replicaset.apps/mysql-77c9c667d5       0         0         0       19m
replicaset.apps/mysql-bc88f5c8         1         1         1       13m
replicaset.apps/mysql-fbf67ff96        0         0         0       19m
replicaset.apps/wordpress-66f777db74   0         0         0       13m
replicaset.apps/wordpress-76b6b4565d   1         1         0       11m
replicaset.apps/wordpress-fb6d85d7f    0         0         0       13m

NAME                                       IMAGE REPOSITORY                                                            TAGS                UPDATED
imagestream.image.openshift.io/mysql       image-registry.openshift-image-registry.svc:5000/wordpress-proj/mysql       1-139               19 minutes ago
imagestream.image.openshift.io/wordpress   image-registry.openshift-image-registry.svc:5000/wordpress-proj/wordpress   5.7-php7.4-apache   13 minutes ago
[student@workstation tasks]$ oc logs wordpress-76b6b4565d-wm6vb 
apache2-foreground
Checking if WordPress is installed
[student@workstation tasks]$ oc get pods
NAME                         READY   STATUS             RESTARTS   AGE
mysql-bc88f5c8-mmxsg         1/1     Running            0          14m
wordpress-76b6b4565d-wm6vb   0/1     CrashLoopBackOff   7          12m
[student@workstation tasks]$ oc describe pod wordpress-76b6b4565d-wm6vb 
Name:         wordpress-76b6b4565d-wm6vb
Namespace:    wordpress-proj
Priority:     0
Node:         master01/192.168.50.10
Start Time:   Sat, 05 Nov 2022 01:56:04 -0400
Labels:       deployment=wordpress
              pod-template-hash=76b6b4565d
Annotations:  k8s.v1.cni.cncf.io/network-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.8.0.29&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              k8s.v1.cni.cncf.io/networks-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.8.0.29&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              kubernetes.io/limit-ranger: LimitRanger plugin set: cpu request for container wordpress; cpu limit for container wordpress
              openshift.io/generated-by: OpenShiftNewApp
              openshift.io/scc: anyuid
Status:       Running
IP:           10.8.0.29
IPs:
  IP:           10.8.0.29
Controlled By:  ReplicaSet/wordpress-76b6b4565d
Containers:
  wordpress:
    Container ID:   cri-o://a3b56c62d1f290bed5fb049bcc2225e406550473c3e0327c87f1d0ca0ce8a10c
    Image:          quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b
    Image ID:       quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b
    Port:           80/TCP
    Host Port:      0/TCP
    State:          Waiting
      Reason:       CrashLoopBackOff
    Last State:     Terminated
      Reason:       Error
      Exit Code:    1
      Started:      Sat, 05 Nov 2022 02:07:43 -0400
      Finished:     Sat, 05 Nov 2022 02:07:46 -0400
    Ready:          False
    Restart Count:  7
    Limits:
      cpu:  50m
    Requests:
      cpu:        50m
    Environment:  &lt;none&gt;
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from wordpress-sa-token-8krhp (ro)
      /var/www/html from wordpress-volume-1 (rw)
Conditions:
  Type              Status
  Initialized       True 
  Ready             False 
  ContainersReady   False 
  PodScheduled      True 
Volumes:
  wordpress-volume-1:
    Type:       EmptyDir (a temporary directory that shares a pod&apos;s lifetime)
    Medium:     
    SizeLimit:  &lt;unset&gt;
  wordpress-sa-token-8krhp:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  wordpress-sa-token-8krhp
    Optional:    false
QoS Class:       Burstable
Node-Selectors:  &lt;none&gt;
Tolerations:     node.kubernetes.io/memory-pressure:NoSchedule op=Exists
                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                 node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type     Reason          Age                  From               Message
  ----     ------          ----                 ----               -------
  Normal   Scheduled       12m                  default-scheduler  Successfully assigned wordpress-proj/wordpress-76b6b4565d-wm6vb to master01
  Normal   AddedInterface  12m                  multus             Add eth0 [10.8.0.29/23]
  Normal   Pulled          10m (x5 over 12m)    kubelet            Container image &quot;quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b&quot; already present on machine
  Normal   Created         10m (x5 over 12m)    kubelet            Created container wordpress
  Normal   Started         10m (x5 over 12m)    kubelet            Started container wordpress
  Warning  BackOff         119s (x45 over 11m)  kubelet            Back-off restarting failed container
[student@workstation tasks]$ oc describe deployment wordpress 
Name:                   wordpress
Namespace:              wordpress-proj
CreationTimestamp:      Sat, 05 Nov 2022 01:54:28 -0400
Labels:                 app=wordpress
                        app.kubernetes.io/component=wordpress
                        app.kubernetes.io/instance=wordpress
Annotations:            deployment.kubernetes.io/revision: 3
                        image.openshift.io/triggers:
                          [{&quot;from&quot;:{&quot;kind&quot;:&quot;ImageStreamTag&quot;,&quot;name&quot;:&quot;wordpress:5.7-php7.4-apache&quot;},&quot;fieldPath&quot;:&quot;spec.template.spec.containers[?(@.name==\&quot;wordpress\&quot;...
                        openshift.io/generated-by: OpenShiftNewApp
Selector:               deployment=wordpress
Replicas:               1 desired | 1 updated | 1 total | 0 available | 1 unavailable
StrategyType:           RollingUpdate
MinReadySeconds:        0
RollingUpdateStrategy:  25% max unavailable, 25% max surge
Pod Template:
  Labels:           deployment=wordpress
  Annotations:      openshift.io/generated-by: OpenShiftNewApp
  Service Account:  wordpress-sa
  Containers:
   wordpress:
    Image:        quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b
    Port:         80/TCP
    Host Port:    0/TCP
    Environment:  &lt;none&gt;
    Mounts:
      /var/www/html from wordpress-volume-1 (rw)
  Volumes:
   wordpress-volume-1:
    Type:       EmptyDir (a temporary directory that shares a pod&apos;s lifetime)
    Medium:     
    SizeLimit:  &lt;unset&gt;
Conditions:
  Type           Status  Reason
  ----           ------  ------
  Progressing    True    NewReplicaSetAvailable
  Available      False   MinimumReplicasUnavailable
OldReplicaSets:  &lt;none&gt;
NewReplicaSet:   wordpress-76b6b4565d (1/1 replicas created)
Events:
  Type    Reason             Age   From                   Message
  ----    ------             ----  ----                   -------
  Normal  ScalingReplicaSet  14m   deployment-controller  Scaled up replica set wordpress-fb6d85d7f to 1
  Normal  ScalingReplicaSet  14m   deployment-controller  Scaled up replica set wordpress-66f777db74 to 1
  Normal  ScalingReplicaSet  14m   deployment-controller  Scaled down replica set wordpress-fb6d85d7f to 0
  Normal  ScalingReplicaSet  12m   deployment-controller  Scaled up replica set wordpress-76b6b4565d to 1
  Normal  ScalingReplicaSet  12m   deployment-controller  Scaled down replica set wordpress-66f777db74 to 0
[student@workstation tasks]$ oc get all;
NAME                             READY   STATUS             RESTARTS   AGE
pod/mysql-bc88f5c8-mmxsg         1/1     Running            0          15m
pod/wordpress-76b6b4565d-wm6vb   0/1     CrashLoopBackOff   7          13m

NAME                TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)    AGE
service/mysql       ClusterIP   172.30.168.145   &lt;none&gt;        3306/TCP   21m
service/wordpress   ClusterIP   172.30.199.124   &lt;none&gt;        80/TCP     15m

NAME                        READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/mysql       1/1     1            1           21m
deployment.apps/wordpress   0/1     1            0           15m

NAME                                   DESIRED   CURRENT   READY   AGE
replicaset.apps/mysql-64d9f4d857       0         0         0       21m
replicaset.apps/mysql-77c9c667d5       0         0         0       21m
replicaset.apps/mysql-bc88f5c8         1         1         1       15m
replicaset.apps/mysql-fbf67ff96        0         0         0       21m
replicaset.apps/wordpress-66f777db74   0         0         0       15m
replicaset.apps/wordpress-76b6b4565d   1         1         0       13m
replicaset.apps/wordpress-fb6d85d7f    0         0         0       15m

NAME                                       IMAGE REPOSITORY                                                            TAGS                UPDATED
imagestream.image.openshift.io/mysql       image-registry.openshift-image-registry.svc:5000/wordpress-proj/mysql       1-139               21 minutes ago
imagestream.image.openshift.io/wordpress   image-registry.openshift-image-registry.svc:5000/wordpress-proj/wordpress   5.7-php7.4-apache   15 minutes ago
[student@workstation tasks]$ oc logs wordpress-76b6b4565d-wm6vb 
apache2-foreground
Checking if WordPress is installed
Error: Error establishing a database connection. This either means that the username and password information in your `wp-config.php` file is incorrect or we can’t contact the database server at `mysql`. This could mean your host’s database server is down.
Installing WordPress with wpcli
/usr/local/bin/docker-entrypoint.sh: line 111: WORDPRESS_URL: unbound variable
[student@workstation tasks]$ vi config.env 
[student@workstation tasks]$ oc set env deployment/wordpress \
&gt;    --prefix WORDPRESS_DB_ --from secret/mysql
deployment.apps/wordpress updated
[student@workstation tasks]$ oc get all
NAME                             READY   STATUS        RESTARTS   AGE
pod/mysql-bc88f5c8-mmxsg         1/1     Running       0          25m
pod/wordpress-76b6b4565d-wm6vb   0/1     Terminating   9          23m
pod/wordpress-798f8bb458-n4629   1/1     Running       0          14s

NAME                TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)    AGE
service/mysql       ClusterIP   172.30.168.145   &lt;none&gt;        3306/TCP   31m
service/wordpress   ClusterIP   172.30.199.124   &lt;none&gt;        80/TCP     24m

NAME                        READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/mysql       1/1     1            1           31m
deployment.apps/wordpress   1/1     1            1           24m

NAME                                   DESIRED   CURRENT   READY   AGE
replicaset.apps/mysql-64d9f4d857       0         0         0       31m
replicaset.apps/mysql-77c9c667d5       0         0         0       31m
replicaset.apps/mysql-bc88f5c8         1         1         1       25m
replicaset.apps/mysql-fbf67ff96        0         0         0       30m
replicaset.apps/wordpress-66f777db74   0         0         0       24m
replicaset.apps/wordpress-76b6b4565d   0         0         0       23m
replicaset.apps/wordpress-798f8bb458   1         1         1       14s
replicaset.apps/wordpress-fb6d85d7f    0         0         0       24m

NAME                                       IMAGE REPOSITORY                                                            TAGS                UPDATED
imagestream.image.openshift.io/mysql       image-registry.openshift-image-registry.svc:5000/wordpress-proj/mysql       1-139               31 minutes ago
imagestream.image.openshift.io/wordpress   image-registry.openshift-image-registry.svc:5000/wordpress-proj/wordpress   5.7-php7.4-apache   24 minutes ago
[student@workstation tasks]$ oc get pods
NAME                         READY   STATUS    RESTARTS   AGE
mysql-bc88f5c8-mmxsg         1/1     Running   0          25m
wordpress-798f8bb458-n4629   0/1     Error     1          30s
[student@workstation tasks]$ oc logs wordpress-798f8bb458-n4629 
apache2-foreground
Checking if WordPress is installed
[student@workstation tasks]$ oc logs wordpress-798f8bb458-n4629 
apache2-foreground
Checking if WordPress is installed
Error: Error establishing a database connection. This either means that the username and password information in your `wp-config.php` file is incorrect or we can’t contact the database server at `mysql`. This could mean your host’s database server is down.
Installing WordPress with wpcli
/usr/local/bin/docker-entrypoint.sh: line 111: WORDPRESS_URL: unbound variable
[student@workstation tasks]$ oc set env -h
Update environment variables on a pod template or a build config

 List environment variable definitions in one or more pods, pod templates or build configuration.
Add, update, or remove container environment variable definitions in one or more pod templates
(within replication controllers or deployment configurations) or build configurations. View or
modify the environment variable definitions on all containers in the specified pods or pod
templates, or just those that match a wildcard.

 If &quot;--env -&quot; is passed, environment variables can be read from STDIN using the standard env syntax.

Usage:
  oc set env RESOURCE/NAME KEY_1=VAL_1 ... KEY_N=VAL_N [flags]

Examples:
  # Update deployment config &apos;myapp&apos; with a new environment variable
  oc set env dc/myapp STORAGE_DIR=/local
  
  # List the environment variables defined on a build config &apos;sample-build&apos;
  oc set env bc/sample-build --list
  
  # List the environment variables defined on all pods
  oc set env pods --all --list
  
  # Output modified build config in YAML
  oc set env bc/sample-build STORAGE_DIR=/data -o yaml
  
  # Update all containers in all replication controllers in the project to have ENV=prod
  oc set env rc --all ENV=prod
  
  # Import environment from a secret
  oc set env --from=secret/mysecret dc/myapp
  
  # Import environment from a config map with a prefix
  oc set env --from=configmap/myconfigmap --prefix=MYSQL_ dc/myapp
  
  # Remove the environment variable ENV from container &apos;c1&apos; in all deployment configs
  oc set env dc --all --containers=&quot;c1&quot; ENV-
  
  # Remove the environment variable ENV from a deployment config definition on disk and
  # update the deployment config on the server
  oc set env -f dc.json ENV-
  
  # Set some of the local shell environment into a deployment config on the server
  oc set env | grep RAILS_ | oc env -e - dc/myapp

Options:
      --all=false: If true, select all resources in the namespace of the specified resource types
      --allow-missing-template-keys=true: If true, ignore any errors in templates when a field or
map key is missing in the template. Only applies to golang and jsonpath output formats.
  -c, --containers=&apos;*&apos;: The names of containers in the selected pod templates to change - may use
wildcards
      --dry-run=&apos;none&apos;: Must be &quot;none&quot;, &quot;server&quot;, or &quot;client&quot;. If client strategy, only print the
object that would be sent, without sending it. If server strategy, submit server-side request
without persisting the resource.
  -e, --env=[]: Specify a key-value pair for an environment variable to set into each container.
  -f, --filename=[]: Filename, directory, or URL to files to use to edit the resource
      --from=&apos;&apos;: The name of a resource from which to inject environment variables
  -k, --kustomize=&apos;&apos;: Process the kustomization directory. This flag can&apos;t be used together with -f
or -R.
      --list=false: If true, display the environment and any changes in the standard format
      --local=false: If true, set image will NOT contact api-server but run locally.
  -o, --output=&apos;&apos;: Output format. One of:
json|yaml|name|go-template|go-template-file|template|templatefile|jsonpath|jsonpath-as-json|jsonpath-file.
      --overwrite=true: If true, allow environment to be overwritten, otherwise reject updates that
overwrite existing environment.
      --prefix=&apos;&apos;: Prefix to append to variable names
  -R, --recursive=false: Process the directory used in -f, --filename recursively. Useful when you
want to manage related manifests organized within the same directory.
      --resolve=false: If true, show secret or configmap references when listing variables
      --resource-version=&apos;&apos;: If non-empty, the labels update will only succeed if this is the
current resource-version for the object. Only valid when specifying a single resource.
  -l, --selector=&apos;&apos;: Selector (label query) to filter on
      --template=&apos;&apos;: Template string or path to template file to use when -o=go-template,
-o=go-template-file. The template format is golang templates
[http://golang.org/pkg/text/template/#pkg-overview].

Use &quot;oc options&quot; for a list of global command-line options (applies to all commands).
[student@workstation tasks]$ oc set env deployment/wordpress --from=configmap/wordpress-config
deployment.apps/wordpress updated
[student@workstation tasks]$ oc get pods
NAME                         READY   STATUS              RESTARTS   AGE
mysql-bc88f5c8-mmxsg         1/1     Running             0          29m
wordpress-798f8bb458-n4629   0/1     CrashLoopBackOff    5          4m14s
wordpress-7bb77c5cc8-b7tpq   0/1     ContainerCreating   0          5s
[student@workstation tasks]$ watch oc get pods
[student@workstation tasks]$ oc describe pod wordpress-7bb77c5cc8-b7tpq 
Name:         wordpress-7bb77c5cc8-b7tpq
Namespace:    wordpress-proj
Priority:     0
Node:         master01/192.168.50.10
Start Time:   Sat, 05 Nov 2022 02:23:13 -0400
Labels:       deployment=wordpress
              pod-template-hash=7bb77c5cc8
Annotations:  k8s.v1.cni.cncf.io/network-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.8.0.33&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              k8s.v1.cni.cncf.io/networks-status:
                [{
                    &quot;name&quot;: &quot;&quot;,
                    &quot;interface&quot;: &quot;eth0&quot;,
                    &quot;ips&quot;: [
                        &quot;10.8.0.33&quot;
                    ],
                    &quot;default&quot;: true,
                    &quot;dns&quot;: {}
                }]
              kubernetes.io/limit-ranger: LimitRanger plugin set: cpu request for container wordpress; cpu limit for container wordpress
              openshift.io/generated-by: OpenShiftNewApp
              openshift.io/scc: anyuid
Status:       Running
IP:           10.8.0.33
IPs:
  IP:           10.8.0.33
Controlled By:  ReplicaSet/wordpress-7bb77c5cc8
Containers:
  wordpress:
    Container ID:   cri-o://26e0f545665b89f9592484d11312e2a36d1574125af0d798d1551d0200aede5f
    Image:          quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b
    Image ID:       quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b
    Port:           80/TCP
    Host Port:      0/TCP
    State:          Running
      Started:      Sat, 05 Nov 2022 02:23:21 -0400
    Ready:          True
    Restart Count:  0
    Limits:
      cpu:  50m
    Requests:
      cpu:  50m
    Environment:
      WORDPRESS_DB_PASSWORD:  &lt;set to the key &apos;password&apos; in secret &apos;mysql&apos;&gt;                           Optional: false
      WORDPRESS_TITLE:        &lt;set to the key &apos;WORDPRESS_TITLE&apos; of config map &apos;wordpress-config&apos;&gt;     Optional: false
      WORDPRESS_URL:          &lt;set to the key &apos;WORDPRESS_URL&apos; of config map &apos;wordpress-config&apos;&gt;       Optional: false
      WORDPRESS_USER:         &lt;set to the key &apos;WORDPRESS_USER&apos; of config map &apos;wordpress-config&apos;&gt;      Optional: false
      WORDPRESS_DB_HOST:      &lt;set to the key &apos;WORDPRESS_DB_HOST&apos; of config map &apos;wordpress-config&apos;&gt;   Optional: false
      WORDPRESS_DB_NAME:      &lt;set to the key &apos;WORDPRESS_DB_NAME&apos; of config map &apos;wordpress-config&apos;&gt;   Optional: false
      WORDPRESS_DB_USER:      &lt;set to the key &apos;WORDPRESS_DB_USER&apos; of config map &apos;wordpress-config&apos;&gt;   Optional: false
      WORDPRESS_EMAIL:        &lt;set to the key &apos;WORDPRESS_EMAIL&apos; of config map &apos;wordpress-config&apos;&gt;     Optional: false
      WORDPRESS_PASSWORD:     &lt;set to the key &apos;WORDPRESS_PASSWORD&apos; of config map &apos;wordpress-config&apos;&gt;  Optional: false
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from wordpress-sa-token-8krhp (ro)
      /var/www/html from wordpress-volume-1 (rw)
Conditions:
  Type              Status
  Initialized       True 
  Ready             True 
  ContainersReady   True 
  PodScheduled      True 
Volumes:
  wordpress-volume-1:
    Type:       EmptyDir (a temporary directory that shares a pod&apos;s lifetime)
    Medium:     
    SizeLimit:  &lt;unset&gt;
  wordpress-sa-token-8krhp:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  wordpress-sa-token-8krhp
    Optional:    false
QoS Class:       Burstable
Node-Selectors:  &lt;none&gt;
Tolerations:     node.kubernetes.io/memory-pressure:NoSchedule op=Exists
                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                 node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type    Reason          Age   From               Message
  ----    ------          ----  ----               -------
  Normal  Scheduled       32s   default-scheduler  Successfully assigned wordpress-proj/wordpress-7bb77c5cc8-b7tpq to master01
  Normal  AddedInterface  31s   multus             Add eth0 [10.8.0.33/23]
  Normal  Pulled          26s   kubelet            Container image &quot;quay.io/redhattraining/wordpress@sha256:0cf952b01efd71e94c82c7e4d1c4d4daf9276fb60a9696b2113a9f701c1ecc6b&quot; already present on machine
  Normal  Created         24s   kubelet            Created container wordpress
  Normal  Started         24s   kubelet            Started container wordpress
[student@workstation tasks]$ oc describe configmaps wordpress-config 
Name:         wordpress-config
Namespace:    wordpress-proj
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;

Data
====
WORDPRESS_EMAIL:
----
student@redhat.com
WORDPRESS_PASSWORD:
----
wppass
WORDPRESS_TITLE:
----
Hello wordpress users
WORDPRESS_URL:
----
wordpress.apps.ocp4.example.com
WORDPRESS_USER:
----
wpuser
WORDPRESS_DB_HOST:
----
mysql
WORDPRESS_DB_NAME:
----
wordpress
WORDPRESS_DB_USER:
----
root
Events:  &lt;none&gt;
[student@workstation tasks]$ 
</pre>


