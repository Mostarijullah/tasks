<pre>

[student@workstation ~]$ oc describe clusterrole.rbac | grep ^name
[student@workstation ~]$ oc describe clusterrole.rbac
Name:         admin
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                                  -----------------  --------------  -----
  serviceaccounts                                            []                 []              [create delete deletecollection get list patch update watch impersonate]
  buildconfigs/webhooks                                      []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs                                               []                 []              [create delete deletecollection get list patch update watch]
  buildlogs                                                  []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs/scale                                    []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs                                          []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimages                                          []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings                                        []                 []              [create delete deletecollection get list patch update watch]
  imagestreams/secrets                                       []                 []              [create delete deletecollection get list patch update watch]
  imagestreams                                               []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags                                            []                 []              [create delete deletecollection get list patch update watch]
  imagetags                                                  []                 []              [create delete deletecollection get list patch update watch]
  processedtemplates                                         []                 []              [create delete deletecollection get list patch update watch]
  rolebindings                                               []                 []              [create delete deletecollection get list patch update watch]
  roles                                                      []                 []              [create delete deletecollection get list patch update watch]
  routes                                                     []                 []              [create delete deletecollection get list patch update watch]
  secrets                                                    []                 []              [create delete deletecollection get list patch update watch]
  templateconfigs                                            []                 []              [create delete deletecollection get list patch update watch]
  templateinstances                                          []                 []              [create delete deletecollection get list patch update watch]
  templates                                                  []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs.apps.openshift.io/scale                  []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs.apps.openshift.io                        []                 []              [create delete deletecollection get list patch update watch]
  rolebindings.authorization.openshift.io                    []                 []              [create delete deletecollection get list patch update watch]
  roles.authorization.openshift.io                           []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs.build.openshift.io/webhooks                   []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs.build.openshift.io                            []                 []              [create delete deletecollection get list patch update watch]
  buildlogs.build.openshift.io                               []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimages.image.openshift.io                       []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings.image.openshift.io                     []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io/secrets                    []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io                            []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags.image.openshift.io                         []                 []              [create delete deletecollection get list patch update watch]
  imagetags.image.openshift.io                               []                 []              [create delete deletecollection get list patch update watch]
  rolebindings.rbac.authorization.k8s.io                     []                 []              [create delete deletecollection get list patch update watch]
  roles.rbac.authorization.k8s.io                            []                 []              [create delete deletecollection get list patch update watch]
  routes.route.openshift.io                                  []                 []              [create delete deletecollection get list patch update watch]
  processedtemplates.template.openshift.io                   []                 []              [create delete deletecollection get list patch update watch]
  templateconfigs.template.openshift.io                      []                 []              [create delete deletecollection get list patch update watch]
  templateinstances.template.openshift.io                    []                 []              [create delete deletecollection get list patch update watch]
  templates.template.openshift.io                            []                 []              [create delete deletecollection get list patch update watch]
  configmaps                                                 []                 []              [create delete deletecollection patch update get list watch]
  endpoints                                                  []                 []              [create delete deletecollection patch update get list watch]
  persistentvolumeclaims                                     []                 []              [create delete deletecollection patch update get list watch]
  pods                                                       []                 []              [create delete deletecollection patch update get list watch]
  replicationcontrollers/scale                               []                 []              [create delete deletecollection patch update get list watch]
  replicationcontrollers                                     []                 []              [create delete deletecollection patch update get list watch]
  services                                                   []                 []              [create delete deletecollection patch update get list watch]
  daemonsets.apps                                            []                 []              [create delete deletecollection patch update get list watch]
  deployments.apps/scale                                     []                 []              [create delete deletecollection patch update get list watch]
  deployments.apps                                           []                 []              [create delete deletecollection patch update get list watch]
  replicasets.apps/scale                                     []                 []              [create delete deletecollection patch update get list watch]
  replicasets.apps                                           []                 []              [create delete deletecollection patch update get list watch]
  statefulsets.apps/scale                                    []                 []              [create delete deletecollection patch update get list watch]
  statefulsets.apps                                          []                 []              [create delete deletecollection patch update get list watch]
  horizontalpodautoscalers.autoscaling                       []                 []              [create delete deletecollection patch update get list watch]
  cronjobs.batch                                             []                 []              [create delete deletecollection patch update get list watch]
  jobs.batch                                                 []                 []              [create delete deletecollection patch update get list watch]
  daemonsets.extensions                                      []                 []              [create delete deletecollection patch update get list watch]
  deployments.extensions/scale                               []                 []              [create delete deletecollection patch update get list watch]
  deployments.extensions                                     []                 []              [create delete deletecollection patch update get list watch]
  ingresses.extensions                                       []                 []              [create delete deletecollection patch update get list watch]
  networkpolicies.extensions                                 []                 []              [create delete deletecollection patch update get list watch]
  replicasets.extensions/scale                               []                 []              [create delete deletecollection patch update get list watch]
  replicasets.extensions                                     []                 []              [create delete deletecollection patch update get list watch]
  replicationcontrollers.extensions/scale                    []                 []              [create delete deletecollection patch update get list watch]
  ingresses.networking.k8s.io                                []                 []              [create delete deletecollection patch update get list watch]
  networkpolicies.networking.k8s.io                          []                 []              [create delete deletecollection patch update get list watch]
  poddisruptionbudgets.policy                                []                 []              [create delete deletecollection patch update get list watch]
  deployments.apps/rollback                                  []                 []              [create delete deletecollection patch update]
  deployments.extensions/rollback                            []                 []              [create delete deletecollection patch update]
  subscriptions.operators.coreos.com                         []                 []              [create update patch delete get list watch]
  buildconfigs/instantiate                                   []                 []              [create]
  buildconfigs/instantiatebinary                             []                 []              [create]
  builds/clone                                               []                 []              [create]
  deploymentconfigrollbacks                                  []                 []              [create]
  deploymentconfigs/instantiate                              []                 []              [create]
  deploymentconfigs/rollback                                 []                 []              [create]
  imagestreamimports                                         []                 []              [create]
  localresourceaccessreviews                                 []                 []              [create]
  localsubjectaccessreviews                                  []                 []              [create]
  podsecuritypolicyreviews                                   []                 []              [create]
  podsecuritypolicyselfsubjectreviews                        []                 []              [create]
  podsecuritypolicysubjectreviews                            []                 []              [create]
  resourceaccessreviews                                      []                 []              [create]
  routes/custom-host                                         []                 []              [create]
  subjectaccessreviews                                       []                 []              [create]
  subjectrulesreviews                                        []                 []              [create]
  deploymentconfigrollbacks.apps.openshift.io                []                 []              [create]
  deploymentconfigs.apps.openshift.io/instantiate            []                 []              [create]
  deploymentconfigs.apps.openshift.io/rollback               []                 []              [create]
  localsubjectaccessreviews.authorization.k8s.io             []                 []              [create]
  localresourceaccessreviews.authorization.openshift.io      []                 []              [create]
  localsubjectaccessreviews.authorization.openshift.io       []                 []              [create]
  resourceaccessreviews.authorization.openshift.io           []                 []              [create]
  subjectaccessreviews.authorization.openshift.io            []                 []              [create]
  subjectrulesreviews.authorization.openshift.io             []                 []              [create]
  buildconfigs.build.openshift.io/instantiate                []                 []              [create]
  buildconfigs.build.openshift.io/instantiatebinary          []                 []              [create]
  builds.build.openshift.io/clone                            []                 []              [create]
  imagestreamimports.image.openshift.io                      []                 []              [create]
  routes.route.openshift.io/custom-host                      []                 []              [create]
  podsecuritypolicyreviews.security.openshift.io             []                 []              [create]
  podsecuritypolicyselfsubjectreviews.security.openshift.io  []                 []              [create]
  podsecuritypolicysubjectreviews.security.openshift.io      []                 []              [create]
  catalogsources.operators.coreos.com                        []                 []              [delete get list watch]
  clusterserviceversions.operators.coreos.com                []                 []              [delete get list watch]
  installplans.operators.coreos.com                          []                 []              [delete get list watch]
  jenkins.build.openshift.io                                 []                 []              [edit view admin]
  builds                                                     []                 []              [get create delete deletecollection list patch update watch]
  builds.build.openshift.io                                  []                 []              [get create delete deletecollection list patch update watch]
  projects                                                   []                 []              [get delete patch update]
  projects.project.openshift.io                              []                 []              [get delete patch update]
  pods/attach                                                []                 []              [get list watch create delete deletecollection patch update]
  pods/exec                                                  []                 []              [get list watch create delete deletecollection patch update]
  pods/portforward                                           []                 []              [get list watch create delete deletecollection patch update]
  pods/proxy                                                 []                 []              [get list watch create delete deletecollection patch update]
  services/proxy                                             []                 []              [get list watch create delete deletecollection patch update]
  packagemanifests.packages.operators.coreos.com             []                 []              [get list watch create update patch delete *]
  volumesnapshots.snapshot.storage.k8s.io                    []                 []              [get list watch create update patch delete deletecollection]
  routes/status                                              []                 []              [get list watch update]
  routes.route.openshift.io/status                           []                 []              [get list watch update]
  appliedclusterresourcequotas                               []                 []              [get list watch]
  bindings                                                   []                 []              [get list watch]
  builds/log                                                 []                 []              [get list watch]
  deploymentconfigs/log                                      []                 []              [get list watch]
  deploymentconfigs/status                                   []                 []              [get list watch]
  events                                                     []                 []              [get list watch]
  imagestreams/status                                        []                 []              [get list watch]
  limitranges                                                []                 []              [get list watch]
  namespaces/status                                          []                 []              [get list watch]
  namespaces                                                 []                 []              [get list watch]
  persistentvolumeclaims/status                              []                 []              [get list watch]
  pods/log                                                   []                 []              [get list watch]
  pods/status                                                []                 []              [get list watch]
  replicationcontrollers/status                              []                 []              [get list watch]
  resourcequotas/status                                      []                 []              [get list watch]
  resourcequotas                                             []                 []              [get list watch]
  resourcequotausages                                        []                 []              [get list watch]
  rolebindingrestrictions                                    []                 []              [get list watch]
  services/status                                            []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/log                    []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/status                 []                 []              [get list watch]
  controllerrevisions.apps                                   []                 []              [get list watch]
  daemonsets.apps/status                                     []                 []              [get list watch]
  deployments.apps/status                                    []                 []              [get list watch]
  replicasets.apps/status                                    []                 []              [get list watch]
  statefulsets.apps/status                                   []                 []              [get list watch]
  rolebindingrestrictions.authorization.openshift.io         []                 []              [get list watch]
  horizontalpodautoscalers.autoscaling/status                []                 []              [get list watch]
  cronjobs.batch/status                                      []                 []              [get list watch]
  jobs.batch/status                                          []                 []              [get list watch]
  builds.build.openshift.io/log                              []                 []              [get list watch]
  daemonsets.extensions/status                               []                 []              [get list watch]
  deployments.extensions/status                              []                 []              [get list watch]
  ingresses.extensions/status                                []                 []              [get list watch]
  replicasets.extensions/status                              []                 []              [get list watch]
  imagestreams.image.openshift.io/status                     []                 []              [get list watch]
  nodes.metrics.k8s.io                                       []                 []              [get list watch]
  pods.metrics.k8s.io                                        []                 []              [get list watch]
  ingresses.networking.k8s.io/status                         []                 []              [get list watch]
  operatorgroups.operators.coreos.com                        []                 []              [get list watch]
  packagemanifests.packages.operators.coreos.com/icon        []                 []              [get list watch]
  poddisruptionbudgets.policy/status                         []                 []              [get list watch]
  appliedclusterresourcequotas.quota.openshift.io            []                 []              [get list watch]
  imagestreams/layers                                        []                 []              [get update]
  imagestreams.image.openshift.io/layers                     []                 []              [get update]
  builds/details                                             []                 []              [update]
  builds.build.openshift.io/details                          []                 []              [update]


Name:         aggregate-olm-edit
Labels:       rbac.authorization.k8s.io/aggregate-to-admin=true
              rbac.authorization.k8s.io/aggregate-to-edit=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                    Non-Resource URLs  Resource Names  Verbs
  ---------                                    -----------------  --------------  -----
  subscriptions.operators.coreos.com           []                 []              [create update patch delete]
  catalogsources.operators.coreos.com          []                 []              [delete]
  clusterserviceversions.operators.coreos.com  []                 []              [delete]
  installplans.operators.coreos.com            []                 []              [delete]


Name:         aggregate-olm-view
Labels:       rbac.authorization.k8s.io/aggregate-to-admin=true
              rbac.authorization.k8s.io/aggregate-to-edit=true
              rbac.authorization.k8s.io/aggregate-to-view=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                            Non-Resource URLs  Resource Names  Verbs
  ---------                                            -----------------  --------------  -----
  catalogsources.operators.coreos.com                  []                 []              [get list watch]
  clusterserviceversions.operators.coreos.com          []                 []              [get list watch]
  installplans.operators.coreos.com                    []                 []              [get list watch]
  operatorgroups.operators.coreos.com                  []                 []              [get list watch]
  subscriptions.operators.coreos.com                   []                 []              [get list watch]
  packagemanifests.packages.operators.coreos.com/icon  []                 []              [get list watch]
  packagemanifests.packages.operators.coreos.com       []                 []              [get list watch]


Name:         alertmanager-main
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  tokenreviews.authentication.k8s.io                []                 []              [create]
  subjectaccessreviews.authorization.k8s.io         []                 []              [create]
  securitycontextconstraints.security.openshift.io  []                 [nonroot]       [use]


Name:         basic-user
Labels:       &lt;none&gt;
Annotations:  openshift.io/description: A user that can get basic information about projects.
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                           Non-Resource URLs  Resource Names  Verbs
  ---------                                           -----------------  --------------  -----
  selfsubjectrulesreviews                             []                 []              [create]
  selfsubjectaccessreviews.authorization.k8s.io       []                 []              [create]
  selfsubjectrulesreviews.authorization.openshift.io  []                 []              [create]
  clusterroles.rbac.authorization.k8s.io              []                 []              [get list watch]
  volumesnapshotclasses.snapshot.storage.k8s.io       []                 []              [get list watch]
  clusterroles                                        []                 []              [get list]
  clusterroles.authorization.openshift.io             []                 []              [get list]
  storageclasses.storage.k8s.io                       []                 []              [get list]
  users                                               []                 [~]             [get]
  users.user.openshift.io                             []                 [~]             [get]
  projects                                            []                 []              [list watch]
  projects.project.openshift.io                       []                 []              [list watch]
  projectrequests                                     []                 []              [list]
  projectrequests.project.openshift.io                []                 []              [list]


Name:         cloud-credential-operator-role
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                    Non-Resource URLs  Resource Names  Verbs
  ---------                                                    -----------------  --------------  -----
  mutatingwebhookconfigurations.admissionregistration.k8s.io   []                 []              [*]
  clusterrolebindings.rbac.authorization.k8s.io                []                 []              [*]
  clusterroles.rbac.authorization.k8s.io                       []                 []              [*]
  authentications.config.openshift.io                          []                 []              [create get update list watch]
  clusteroperators.config.openshift.io/status                  []                 []              [create get update list watch]
  clusteroperators.config.openshift.io                         []                 []              [create get update list watch]
  tokenreviews.authentication.k8s.io                           []                 []              [create]
  subjectaccessreviews.authorization.k8s.io                    []                 []              [create]
  configmaps                                                   []                 []              [get list watch create update patch delete]
  events                                                       []                 []              [get list watch create update patch delete]
  secrets                                                      []                 []              [get list watch create update patch delete]
  credentialsrequests.cloudcredential.openshift.io/finalizers  []                 []              [get list watch create update patch delete]
  credentialsrequests.cloudcredential.openshift.io/status      []                 []              [get list watch create update patch delete]
  credentialsrequests.cloudcredential.openshift.io             []                 []              [get list watch create update patch delete]
  namespaces                                                   []                 []              [get list watch]
  clusterversions.config.openshift.io                          []                 []              [get list watch]
  dnses.config.openshift.io                                    []                 []              [get list watch]
  infrastructures.config.openshift.io                          []                 []              [get list watch]
  cloudcredentials.operator.openshift.io                       []                 []              [get list watch]


Name:         cluster-admin
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  *.*        []                 []              [*]
             [*]                []              [*]


Name:         cluster-autoscaler
Labels:       k8s-addon=cluster-autoscaler.addons.k8s.io
              k8s-app=cluster-autoscaler
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                Non-Resource URLs  Resource Names        Verbs
  ---------                                -----------------  --------------        -----
  endpoints                                []                 []                    [create patch]
  events                                   []                 []                    [create patch]
  pods/eviction                            []                 []                    [create]
  leases.coordination.k8s.io               []                 []                    [create]
  endpoints                                []                 [cluster-autoscaler]  [get update]
  leases.coordination.k8s.io               []                 [cluster-autoscaler]  [get update]
  pods/status                              []                 []                    [update]
  nodes                                    []                 []                    [watch list get update]
  machinedeployments.cluster.k8s.io        []                 []                    [watch list get update]
  machines.cluster.k8s.io                  []                 []                    [watch list get update]
  machinesets.cluster.k8s.io               []                 []                    [watch list get update]
  machinedeployments.machine.openshift.io  []                 []                    [watch list get update]
  machines.machine.openshift.io            []                 []                    [watch list get update]
  machinesets.machine.openshift.io         []                 []                    [watch list get update]
  namespaces                               []                 []                    [watch list get]
  persistentvolumeclaims                   []                 []                    [watch list get]
  persistentvolumes                        []                 []                    [watch list get]
  pods                                     []                 []                    [watch list get]
  replicationcontrollers                   []                 []                    [watch list get]
  services                                 []                 []                    [watch list get]
  daemonsets.apps                          []                 []                    [watch list get]
  replicasets.apps                         []                 []                    [watch list get]
  statefulsets.apps                        []                 []                    [watch list get]
  jobs.batch                               []                 []                    [watch list get]
  daemonsets.extensions                    []                 []                    [watch list get]
  replicasets.extensions                   []                 []                    [watch list get]
  csinodes.storage.k8s.io                  []                 []                    [watch list get]
  storageclasses.storage.k8s.io            []                 []                    [watch list get]
  poddisruptionbudgets.policy              []                 []                    [watch list]


Name:         cluster-autoscaler-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                                     -----------------  --------------  -----
  validatingwebhookconfigurations.admissionregistration.k8s.io  []                 []              [*]
  *.autoscaling.openshift.io                                    []                 []              [*]
  clusteroperators.config.openshift.io/status                   []                 []              [create get update]
  clusteroperators.config.openshift.io                          []                 []              [create get update]
  tokenreviews.authentication.k8s.io                            []                 []              [create]
  subjectaccessreviews.authorization.k8s.io                     []                 []              [create]


Name:         cluster-autoscaler-operator:cluster-reader
Labels:       rbac.authorization.k8s.io/aggregate-to-cluster-reader=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                   Non-Resource URLs  Resource Names  Verbs
  ---------                   -----------------  --------------  -----
  *.autoscaling.openshift.io  []                 []              [get list watch]


Name:         cluster-debugger
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
             [/debug/pprof/*]   []              [get]
             [/debug/pprof]     []              [get]
             [/metrics]         []              [get]


Name:         cluster-image-registry-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                Non-Resource URLs  Resource Names  Verbs
  ---------                                                -----------------  --------------  -----
  clusteroperators.config.openshift.io                     []                 []              [* create get update]
  configmaps                                               []                 []              [*]
  endpoints                                                []                 []              [*]
  events                                                   []                 []              [*]
  namespaces                                               []                 []              [*]
  persistentvolumeclaims                                   []                 []              [*]
  pods                                                     []                 []              [*]
  secrets                                                  []                 []              [*]
  serviceaccounts                                          []                 []              [*]
  services                                                 []                 []              [*]
  deploymentconfigs.apps.openshift.io                      []                 []              [*]
  daemonsets.apps                                          []                 []              [*]
  deploymentconfigs.apps                                   []                 []              [*]
  deployments.apps                                         []                 []              [*]
  replicasets.apps                                         []                 []              [*]
  statefulsets.apps                                        []                 []              [*]
  cronjobs.batch                                           []                 []              [*]
  jobs.batch                                               []                 []              [*]
  images.config.openshift.io/status                        []                 []              [*]
  images.config.openshift.io                               []                 []              [*]
  *.image.openshift.io                                     []                 []              [*]
  configs.imageregistry.operator.openshift.io/status       []                 []              [*]
  configs.imageregistry.operator.openshift.io              []                 []              [*]
  imagepruners.imageregistry.operator.openshift.io/status  []                 []              [*]
  imagepruners.imageregistry.operator.openshift.io         []                 []              [*]
  clusterrolebindings.rbac.authorization.k8s.io            []                 []              [*]
  clusterroles.rbac.authorization.k8s.io                   []                 []              [*]
  routes.route.openshift.io/custom-host                    []                 []              [*]
  routes.route.openshift.io                                []                 []              [*]
  clusteroperators.config.openshift.io/status              []                 []              [create get update]
  infrastructures.config.openshift.io                      []                 []              [get list watch]
  proxies.config.openshift.io                              []                 []              [list get watch]
  limitranges                                              []                 []              [list]
  resourcequotas                                           []                 []              [list]


Name:         cluster-monitoring-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                     Non-Resource URLs  Resource Names                           Verbs
  ---------                                                     -----------------  --------------                           -----
  configmaps                                                    []                 []                                       [* create get list watch update delete]
  prometheusrules.monitoring.coreos.com                         []                 []                                       [* get list watch]
  alertmanagers.monitoring.coreos.com                           []                 []                                       [* get]
  secrets                                                       []                 []                                       [* list watch]
  statefulsets.apps                                             []                 []                                       [* list watch]
  configmaps                                                    []                 [user-workload-monitoring-config]        [*]
  *.metrics.k8s.io                                              []                 []                                       [*]
  alertmanagers.monitoring.coreos.com/finalizers                []                 []                                       [*]
  podmonitors.monitoring.coreos.com                             []                 []                                       [*]
  probes.monitoring.coreos.com                                  []                 []                                       [*]
  prometheuses.monitoring.coreos.com/finalizers                 []                 []                                       [*]
  prometheuses.monitoring.coreos.com                            []                 []                                       [*]
  servicemonitors.monitoring.coreos.com                         []                 []                                       [*]
  thanosrulers.monitoring.coreos.com/finalizers                 []                 []                                       [*]
  thanosrulers.monitoring.coreos.com                            []                 []                                       [*]
  serviceaccounts                                               []                 []                                       [create get list watch update delete]
  services                                                      []                 []                                       [create get list watch update delete]
  validatingwebhookconfigurations.admissionregistration.k8s.io  []                 [prometheusrules.openshift.io]           [create get list watch update delete]
  apiservices.apiregistration.k8s.io                            []                 []                                       [create get list watch update delete]
  daemonsets.apps                                               []                 []                                       [create get list watch update delete]
  deployments.apps                                              []                 []                                       [create get list watch update delete]
  clusterrolebindings.rbac.authorization.k8s.io                 []                 []                                       [create get list watch update delete]
  clusterroles.rbac.authorization.k8s.io                        []                 []                                       [create get list watch update delete]
  rolebindings.rbac.authorization.k8s.io                        []                 []                                       [create get list watch update delete]
  roles.rbac.authorization.k8s.io                               []                 []                                       [create get list watch update delete]
  routes.route.openshift.io                                     []                 []                                       [create get list watch update delete]
  securitycontextconstraints.security.openshift.io              []                 []                                       [create get list watch update delete]
  validatingwebhookconfigurations.admissionregistration.k8s.io  []                 []                                       [create get list watch]
  customresourcedefinitions.apiextensions.k8s.io                []                 []                                       [create]
  tokenreviews.authentication.k8s.io                            []                 []                                       [create]
  subjectaccessreviews.authorization.k8s.io                     []                 []                                       [create]
  endpoints                                                     []                 []                                       [get create update delete list watch]
  services/finalizers                                           []                 []                                       [get create update delete]
  pods                                                          []                 []                                       [get list watch delete]
  namespaces                                                    []                 []                                       [get list watch]
  nodes                                                         []                 []                                       [get list watch]
  nodes.metrics.k8s.io                                          []                 []                                       [get list watch]
  pods.metrics.k8s.io                                           []                 []                                       [get list watch]
  clusteroperators.config.openshift.io/status                   []                 []                                       [get update create]
  clusteroperators.config.openshift.io                          []                 []                                       [get update create]
  customresourcedefinitions.apiextensions.k8s.io                []                 [alertmanagers.monitoring.coreos.com]    [get update]
  customresourcedefinitions.apiextensions.k8s.io                []                 [podmonitors.monitoring.coreos.com]      [get update]
  customresourcedefinitions.apiextensions.k8s.io                []                 [prometheuses.monitoring.coreos.com]     [get update]
  customresourcedefinitions.apiextensions.k8s.io                []                 [prometheusrules.monitoring.coreos.com]  [get update]
  customresourcedefinitions.apiextensions.k8s.io                []                 [servicemonitors.monitoring.coreos.com]  [get update]
  customresourcedefinitions.apiextensions.k8s.io                []                 [thanosrulers.monitoring.coreos.com]     [get update]
                                                                [/metrics]         []                                       [get]
  nodes/metrics                                                 []                 []                                       [get]
  clusterversions.config.openshift.io                           []                 []                                       [get]
  infrastructures.config.openshift.io                           []                 []                                       [get]
  proxies.config.openshift.io                                   []                 []                                       [get]
  limitranges                                                   []                 []                                       [list watch]
  persistentvolumeclaims                                        []                 []                                       [list watch]
  persistentvolumes                                             []                 []                                       [list watch]
  replicationcontrollers                                        []                 []                                       [list watch]
  resourcequotas                                                []                 []                                       [list watch]
  mutatingwebhookconfigurations.admissionregistration.k8s.io    []                 []                                       [list watch]
  deploymentconfigs.apps.openshift.io                           []                 []                                       [list watch]
  replicasets.apps                                              []                 []                                       [list watch]
  horizontalpodautoscalers.autoscaling                          []                 []                                       [list watch]
  cronjobs.batch                                                []                 []                                       [list watch]
  jobs.batch                                                    []                 []                                       [list watch]
  buildconfigs.build.openshift.io                               []                 []                                       [list watch]
  builds.build.openshift.io                                     []                 []                                       [list watch]
  certificatesigningrequests.certificates.k8s.io                []                 []                                       [list watch]
  daemonsets.extensions                                         []                 []                                       [list watch]
  deployments.extensions                                        []                 []                                       [list watch]
  ingresses.extensions                                          []                 []                                       [list watch]
  replicasets.extensions                                        []                 []                                       [list watch]
  networkpolicies.networking.k8s.io                             []                 []                                       [list watch]
  poddisruptionbudgets.policy                                   []                 []                                       [list watch]
  clusterresourcequotas.quota.openshift.io                      []                 []                                       [list watch]
  storageclasses.storage.k8s.io                                 []                 []                                       [list watch]
  volumeattachments.storage.k8s.io                              []                 []                                       [list watch]
  groups.user.openshift.io                                      []                 []                                       [list watch]
  securitycontextconstraints.security.openshift.io              []                 [node-exporter]                          [use]
  securitycontextconstraints.security.openshift.io              []                 [nonroot]                                [use]


Name:         cluster-monitoring-view
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources   Non-Resource URLs  Resource Names  Verbs
  ---------   -----------------  --------------  -----
  namespaces  []                 []              [get]


Name:         cluster-node-tuning-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                             Non-Resource URLs  Resource Names  Verbs
  ---------                                             -----------------  --------------  -----
  *.tuned.openshift.io                                  []                 []              [*]
  configmaps                                            []                 []              [create get delete list update watch]
  namespaces                                            []                 []              [create get delete list update watch]
  secrets                                               []                 []              [create get delete list update watch]
  serviceaccounts                                       []                 []              [create get delete list update watch]
  services                                              []                 []              [create get delete list update watch]
  daemonsets.apps                                       []                 []              [create get delete list update watch]
  machineconfigs.machineconfiguration.openshift.io      []                 []              [create get delete list update watch]
  clusterrolebindings.rbac.authorization.k8s.io         []                 []              [create get delete list update watch]
  clusterroles.rbac.authorization.k8s.io                []                 []              [create get delete list update watch]
  clusteroperators.config.openshift.io                  []                 []              [create get list watch]
  events                                                []                 []              [create]
  nodes                                                 []                 []              [get list watch]
  pods                                                  []                 []              [get list watch]
  machineconfigpools.machineconfiguration.openshift.io  []                 []              [get list watch]
  nodes/metrics                                         []                 []              [get]
  nodes/specs                                           []                 []              [get]
  clusteroperators.config.openshift.io/status           []                 []              [update]
  securitycontextconstraints.security.openshift.io      []                 []              [use]


Name:         cluster-node-tuning:tuned
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  *.tuned.openshift.io                              []                 []              [*]
  securitycontextconstraints.security.openshift.io  []                 [privileged]    [use]


Name:         cluster-reader
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                                     -----------------  --------------  -----
  nodes/stats                                                   []                 []              [create get]
  localresourceaccessreviews                                    []                 []              [create]
  localsubjectaccessreviews                                     []                 []              [create]
  podsecuritypolicyreviews                                      []                 []              [create]
  podsecuritypolicyselfsubjectreviews                           []                 []              [create]
  podsecuritypolicysubjectreviews                               []                 []              [create]
  resourceaccessreviews                                         []                 []              [create]
  selfsubjectrulesreviews                                       []                 []              [create]
  subjectaccessreviews                                          []                 []              [create]
  subjectrulesreviews                                           []                 []              [create]
  tokenreviews.authentication.k8s.io                            []                 []              [create]
  localsubjectaccessreviews.authorization.k8s.io                []                 []              [create]
  selfsubjectaccessreviews.authorization.k8s.io                 []                 []              [create]
  selfsubjectrulesreviews.authorization.k8s.io                  []                 []              [create]
  subjectaccessreviews.authorization.k8s.io                     []                 []              [create]
  localresourceaccessreviews.authorization.openshift.io         []                 []              [create]
  localsubjectaccessreviews.authorization.openshift.io          []                 []              [create]
  resourceaccessreviews.authorization.openshift.io              []                 []              [create]
  selfsubjectrulesreviews.authorization.openshift.io            []                 []              [create]
  subjectaccessreviews.authorization.openshift.io               []                 []              [create]
  subjectrulesreviews.authorization.openshift.io                []                 []              [create]
  podsecuritypolicyreviews.security.openshift.io                []                 []              [create]
  podsecuritypolicyselfsubjectreviews.security.openshift.io     []                 []              [create]
  podsecuritypolicysubjectreviews.security.openshift.io         []                 []              [create]
  appliedclusterresourcequotas                                  []                 []              [get list watch]
  bindings                                                      []                 []              [get list watch]
  brokertemplateinstances                                       []                 []              [get list watch]
  buildconfigs/webhooks                                         []                 []              [get list watch]
  buildconfigs                                                  []                 []              [get list watch]
  buildlogs                                                     []                 []              [get list watch]
  builds/details                                                []                 []              [get list watch]
  builds/log                                                    []                 []              [get list watch]
  builds                                                        []                 []              [get list watch]
  clusternetworks                                               []                 []              [get list watch]
  clusterresourcequotas/status                                  []                 []              [get list watch]
  clusterresourcequotas                                         []                 []              [get list watch]
  clusterrolebindings                                           []                 []              [get list watch]
  clusterroles                                                  []                 []              [get list watch]
  componentstatuses                                             []                 []              [get list watch]
  configmaps                                                    []                 []              [get list watch]
  deploymentconfigs/log                                         []                 []              [get list watch]
  deploymentconfigs/scale                                       []                 []              [get list watch]
  deploymentconfigs/status                                      []                 []              [get list watch]
  deploymentconfigs                                             []                 []              [get list watch]
  egressnetworkpolicies                                         []                 []              [get list watch]
  endpoints                                                     []                 []              [get list watch]
  events                                                        []                 []              [get list watch]
  groups                                                        []                 []              [get list watch]
  hostsubnets                                                   []                 []              [get list watch]
  identities                                                    []                 []              [get list watch]
  images                                                        []                 []              [get list watch]
  imagesignatures                                               []                 []              [get list watch]
  imagestreamimages                                             []                 []              [get list watch]
  imagestreammappings                                           []                 []              [get list watch]
  imagestreams/status                                           []                 []              [get list watch]
  imagestreams                                                  []                 []              [get list watch]
  imagestreamtags                                               []                 []              [get list watch]
  imagetags                                                     []                 []              [get list watch]
  limitranges                                                   []                 []              [get list watch]
  namespaces/status                                             []                 []              [get list watch]
  namespaces                                                    []                 []              [get list watch]
  netnamespaces                                                 []                 []              [get list watch]
  nodes/status                                                  []                 []              [get list watch]
  nodes                                                         []                 []              [get list watch]
  oauthclientauthorizations                                     []                 []              [get list watch]
  persistentvolumeclaims/status                                 []                 []              [get list watch]
  persistentvolumeclaims                                        []                 []              [get list watch]
  persistentvolumes/status                                      []                 []              [get list watch]
  persistentvolumes                                             []                 []              [get list watch]
  pods/binding                                                  []                 []              [get list watch]
  pods/eviction                                                 []                 []              [get list watch]
  pods/log                                                      []                 []              [get list watch]
  pods/status                                                   []                 []              [get list watch]
  pods                                                          []                 []              [get list watch]
  podtemplates                                                  []                 []              [get list watch]
  processedtemplates                                            []                 []              [get list watch]
  projectrequests                                               []                 []              [get list watch]
  replicationcontrollers/scale                                  []                 []              [get list watch]
  replicationcontrollers/status                                 []                 []              [get list watch]
  replicationcontrollers                                        []                 []              [get list watch]
  resourcequotas/status                                         []                 []              [get list watch]
  resourcequotas                                                []                 []              [get list watch]
  resourcequotausages                                           []                 []              [get list watch]
  rolebindingrestrictions                                       []                 []              [get list watch]
  rolebindings                                                  []                 []              [get list watch]
  roles                                                         []                 []              [get list watch]
  routes/status                                                 []                 []              [get list watch]
  routes                                                        []                 []              [get list watch]
  securitycontextconstraints                                    []                 []              [get list watch]
  serviceaccounts                                               []                 []              [get list watch]
  services/status                                               []                 []              [get list watch]
  services                                                      []                 []              [get list watch]
  templateconfigs                                               []                 []              [get list watch]
  templateinstances/status                                      []                 []              [get list watch]
  templateinstances                                             []                 []              [get list watch]
  templates                                                     []                 []              [get list watch]
  useridentitymappings                                          []                 []              [get list watch]
  users                                                         []                 []              [get list watch]
  mutatingwebhookconfigurations.admissionregistration.k8s.io    []                 []              [get list watch]
  validatingwebhookconfigurations.admissionregistration.k8s.io  []                 []              [get list watch]
  customresourcedefinitions.apiextensions.k8s.io/status         []                 []              [get list watch]
  customresourcedefinitions.apiextensions.k8s.io                []                 []              [get list watch]
  apiservices.apiregistration.k8s.io/status                     []                 []              [get list watch]
  apiservices.apiregistration.k8s.io                            []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/log                       []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/scale                     []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/status                    []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io                           []                 []              [get list watch]
  controllerrevisions.apps                                      []                 []              [get list watch]
  daemonsets.apps/status                                        []                 []              [get list watch]
  daemonsets.apps                                               []                 []              [get list watch]
  deployments.apps/scale                                        []                 []              [get list watch]
  deployments.apps/status                                       []                 []              [get list watch]
  deployments.apps                                              []                 []              [get list watch]
  replicasets.apps/scale                                        []                 []              [get list watch]
  replicasets.apps/status                                       []                 []              [get list watch]
  replicasets.apps                                              []                 []              [get list watch]
  statefulsets.apps/scale                                       []                 []              [get list watch]
  statefulsets.apps/status                                      []                 []              [get list watch]
  statefulsets.apps                                             []                 []              [get list watch]
  clusterrolebindings.authorization.openshift.io                []                 []              [get list watch]
  clusterroles.authorization.openshift.io                       []                 []              [get list watch]
  rolebindingrestrictions.authorization.openshift.io            []                 []              [get list watch]
  rolebindings.authorization.openshift.io                       []                 []              [get list watch]
  roles.authorization.openshift.io                              []                 []              [get list watch]
  *.autoscaling.openshift.io                                    []                 []              [get list watch]
  horizontalpodautoscalers.autoscaling/status                   []                 []              [get list watch]
  horizontalpodautoscalers.autoscaling                          []                 []              [get list watch]
  cronjobs.batch/status                                         []                 []              [get list watch]
  cronjobs.batch                                                []                 []              [get list watch]
  jobs.batch/status                                             []                 []              [get list watch]
  jobs.batch                                                    []                 []              [get list watch]
  buildconfigs.build.openshift.io/webhooks                      []                 []              [get list watch]
  buildconfigs.build.openshift.io                               []                 []              [get list watch]
  buildlogs.build.openshift.io                                  []                 []              [get list watch]
  builds.build.openshift.io/details                             []                 []              [get list watch]
  builds.build.openshift.io/log                                 []                 []              [get list watch]
  builds.build.openshift.io                                     []                 []              [get list watch]
  certificatesigningrequests.certificates.k8s.io/approval       []                 []              [get list watch]
  certificatesigningrequests.certificates.k8s.io/status         []                 []              [get list watch]
  certificatesigningrequests.certificates.k8s.io                []                 []              [get list watch]
  credentialsrequests.cloudcredential.openshift.io              []                 []              [get list watch]
  apiservers.config.openshift.io                                []                 []              [get list watch]
  authentications.config.openshift.io                           []                 []              [get list watch]
  builds.config.openshift.io                                    []                 []              [get list watch]
  clusteroperators.config.openshift.io                          []                 []              [get list watch]
  clusterversions.config.openshift.io                           []                 []              [get list watch]
  consoles.config.openshift.io                                  []                 []              [get list watch]
  dnses.config.openshift.io                                     []                 []              [get list watch]
  featuregates.config.openshift.io                              []                 []              [get list watch]
  images.config.openshift.io                                    []                 []              [get list watch]
  infrastructures.config.openshift.io                           []                 []              [get list watch]
  ingresses.config.openshift.io                                 []                 []              [get list watch]
  networks.config.openshift.io                                  []                 []              [get list watch]
  oauths.config.openshift.io                                    []                 []              [get list watch]
  operatorhubs.config.openshift.io                              []                 []              [get list watch]
  projects.config.openshift.io                                  []                 []              [get list watch]
  proxies.config.openshift.io                                   []                 []              [get list watch]
  schedulers.config.openshift.io                                []                 []              [get list watch]
  leases.coordination.k8s.io                                    []                 []              [get list watch]
  events.events.k8s.io                                          []                 []              [get list watch]
  daemonsets.extensions/status                                  []                 []              [get list watch]
  daemonsets.extensions                                         []                 []              [get list watch]
  deployments.extensions/scale                                  []                 []              [get list watch]
  deployments.extensions/status                                 []                 []              [get list watch]
  deployments.extensions                                        []                 []              [get list watch]
  horizontalpodautoscalers.extensions/status                    []                 []              [get list watch]
  horizontalpodautoscalers.extensions                           []                 []              [get list watch]
  ingresses.extensions/status                                   []                 []              [get list watch]
  ingresses.extensions                                          []                 []              [get list watch]
  jobs.extensions/status                                        []                 []              [get list watch]
  jobs.extensions                                               []                 []              [get list watch]
  networkpolicies.extensions                                    []                 []              [get list watch]
  podsecuritypolicies.extensions                                []                 []              [get list watch]
  replicasets.extensions/scale                                  []                 []              [get list watch]
  replicasets.extensions/status                                 []                 []              [get list watch]
  replicasets.extensions                                        []                 []              [get list watch]
  replicationcontrollers.extensions/scale                       []                 []              [get list watch]
  replicationcontrollers.extensions                             []                 []              [get list watch]
  storageclasses.extensions                                     []                 []              [get list watch]
  thirdpartyresources.extensions                                []                 []              [get list watch]
  images.image.openshift.io                                     []                 []              [get list watch]
  imagesignatures.image.openshift.io                            []                 []              [get list watch]
  imagestreamimages.image.openshift.io                          []                 []              [get list watch]
  imagestreammappings.image.openshift.io                        []                 []              [get list watch]
  imagestreams.image.openshift.io/status                        []                 []              [get list watch]
  imagestreams.image.openshift.io                               []                 []              [get list watch]
  imagestreamtags.image.openshift.io                            []                 []              [get list watch]
  imagetags.image.openshift.io                                  []                 []              [get list watch]
  machinehealthchecks.machine.openshift.io                      []                 []              [get list watch]
  machines.machine.openshift.io                                 []                 []              [get list watch]
  machinesets.machine.openshift.io                              []                 []              [get list watch]
  containerruntimeconfigs.machineconfiguration.openshift.io     []                 []              [get list watch]
  controllerconfigs.machineconfiguration.openshift.io           []                 []              [get list watch]
  kubeletconfigs.machineconfiguration.openshift.io              []                 []              [get list watch]
  machineconfigpools.machineconfiguration.openshift.io          []                 []              [get list watch]
  nodes.metrics.k8s.io                                          []                 []              [get list watch]
  pods.metrics.k8s.io                                           []                 []              [get list watch]
  clusternetworks.network.openshift.io                          []                 []              [get list watch]
  egressnetworkpolicies.network.openshift.io                    []                 []              [get list watch]
  hostsubnets.network.openshift.io                              []                 []              [get list watch]
  netnamespaces.network.openshift.io                            []                 []              [get list watch]
  ingresses.networking.k8s.io/status                            []                 []              [get list watch]
  ingresses.networking.k8s.io                                   []                 []              [get list watch]
  networkpolicies.networking.k8s.io                             []                 []              [get list watch]
  runtimeclasses.node.k8s.io                                    []                 []              [get list watch]
  oauthclientauthorizations.oauth.openshift.io                  []                 []              [get list watch]
  catalogsources.operators.coreos.com                           []                 []              [get list watch]
  clusterserviceversions.operators.coreos.com                   []                 []              [get list watch]
  installplans.operators.coreos.com                             []                 []              [get list watch]
  operatorgroups.operators.coreos.com                           []                 []              [get list watch]
  subscriptions.operators.coreos.com                            []                 []              [get list watch]
  packagemanifests.packages.operators.coreos.com/icon           []                 []              [get list watch]
  packagemanifests.packages.operators.coreos.com                []                 []              [get list watch]
  poddisruptionbudgets.policy/status                            []                 []              [get list watch]
  poddisruptionbudgets.policy                                   []                 []              [get list watch]
  podsecuritypolicies.policy                                    []                 []              [get list watch]
  projectrequests.project.openshift.io                          []                 []              [get list watch]
  appliedclusterresourcequotas.quota.openshift.io               []                 []              [get list watch]
  clusterresourcequotas.quota.openshift.io/status               []                 []              [get list watch]
  clusterresourcequotas.quota.openshift.io                      []                 []              [get list watch]
  clusterrolebindings.rbac.authorization.k8s.io                 []                 []              [get list watch]
  clusterroles.rbac.authorization.k8s.io                        []                 []              [get list watch]
  rolebindings.rbac.authorization.k8s.io                        []                 []              [get list watch]
  roles.rbac.authorization.k8s.io                               []                 []              [get list watch]
  routes.route.openshift.io/status                              []                 []              [get list watch]
  routes.route.openshift.io                                     []                 []              [get list watch]
  configs.samples.operator.openshift.io/status                  []                 []              [get list watch]
  configs.samples.operator.openshift.io                         []                 []              [get list watch]
  priorityclasses.scheduling.k8s.io                             []                 []              [get list watch]
  rangeallocations.security.openshift.io                        []                 []              [get list watch]
  securitycontextconstraints.security.openshift.io              []                 []              [get list watch]
  podpresets.settings.k8s.io                                    []                 []              [get list watch]
  volumesnapshots.snapshot.storage.k8s.io                       []                 []              [get list watch]
  csidrivers.storage.k8s.io                                     []                 []              [get list watch]
  csinodes.storage.k8s.io                                       []                 []              [get list watch]
  storageclasses.storage.k8s.io                                 []                 []              [get list watch]
  volumeattachments.storage.k8s.io/status                       []                 []              [get list watch]
  volumeattachments.storage.k8s.io                              []                 []              [get list watch]
  brokertemplateinstances.template.openshift.io                 []                 []              [get list watch]
  processedtemplates.template.openshift.io                      []                 []              [get list watch]
  templateconfigs.template.openshift.io                         []                 []              [get list watch]
  templateinstances.template.openshift.io/status                []                 []              [get list watch]
  templateinstances.template.openshift.io                       []                 []              [get list watch]
  templates.template.openshift.io                               []                 []              [get list watch]
  groups.user.openshift.io                                      []                 []              [get list watch]
  identities.user.openshift.io                                  []                 []              [get list watch]
  useridentitymappings.user.openshift.io                        []                 []              [get list watch]
  users.user.openshift.io                                       []                 []              [get list watch]
                                                                [*]                []              [get]
  imagestreams/layers                                           []                 []              [get]
  nodes/metrics                                                 []                 []              [get]
  nodes/spec                                                    []                 []              [get]
  imagestreams.image.openshift.io/layers                        []                 []              [get]
  projects                                                      []                 []              [list watch get]
  projects.project.openshift.io                                 []                 []              [list watch get]
  jenkins.build.openshift.io                                    []                 []              [view]


Name:         cluster-samples-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                     -----------------  --------------  -----
  clusteroperators.config.openshift.io/status   []                 []              [*]
  clusteroperators.config.openshift.io          []                 []              [*]
  configs.samples.operator.openshift.io/status  []                 []              [*]
  configs.samples.operator.openshift.io         []                 []              [*]


Name:         cluster-samples-operator-proxy-reader
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                    Non-Resource URLs  Resource Names  Verbs
  ---------                    -----------------  --------------  -----
  proxies.config.openshift.io  []                 []              [get list watch]


Name:         cluster-status
Labels:       &lt;none&gt;
Annotations:  openshift.io/description: A user that can get basic cluster status information.
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs       Resource Names  Verbs
  ---------  -----------------       --------------  -----
             [/.well-known/*]        []              [get]
             [/.well-known]          []              [get]
             [/]                     []              [get]
             [/api/*]                []              [get]
             [/api]                  []              [get]
             [/apis/*]               []              [get]
             [/apis]                 []              [get]
             [/healthz/]             []              [get]
             [/healthz]              []              [get]
             [/oapi/*]               []              [get]
             [/oapi]                 []              [get]
             [/openapi/v2]           []              [get]
             [/osapi/]               []              [get]
             [/osapi]                []              [get]
             [/swagger-2.0.0.pb-v1]  []              [get]
             [/swagger.json]         []              [get]
             [/swaggerapi/*]         []              [get]
             [/swaggerapi]           []              [get]
             [/version/*]            []              [get]
             [/version]              []              [get]


Name:         console
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                                     -----------------  --------------  -----
  customresourcedefinitions.apiextensions.k8s.io                []                 []              [get list watch]
  mutatingwebhookconfigurations.admissionregistration.k8s.io    []                 []              [get]
  validatingwebhookconfigurations.admissionregistration.k8s.io  []                 []              [get]


Name:         console-extensions-reader
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                     -----------------  --------------  -----
  consoleclidownloads.console.openshift.io      []                 []              [get list watch]
  consoleexternalloglinks.console.openshift.io  []                 []              [get list watch]
  consolelinks.console.openshift.io             []                 []              [get list watch]
  consolenotifications.console.openshift.io     []                 []              [get list watch]
  consoleyamlsamples.console.openshift.io       []                 []              [get list watch]


Name:         console-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                    Non-Resource URLs  Resource Names  Verbs
  ---------                                    -----------------  --------------  -----
  oauthclients.oauth.openshift.io              []                 [console]       [get list update watch]
  clusteroperators.config.openshift.io/status  []                 []              [get list watch create update delete]
  clusteroperators.config.openshift.io         []                 []              [get list watch create update delete]
  consoles.config.openshift.io/status          []                 []              [get list watch create update delete]
  consoles.config.openshift.io                 []                 []              [get list watch create update delete]
  consoleclidownloads.console.openshift.io     []                 []              [get list watch create update delete]
  consoles.operator.openshift.io/status        []                 []              [get list watch create update delete]
  consoles.operator.openshift.io               []                 []              [get list watch create update delete]
  infrastructures.config.openshift.io          []                 []              [get list watch]
  ingresses.config.openshift.io                []                 []              [get list watch]
  oauths.config.openshift.io                   []                 []              [get list watch]
  proxies.config.openshift.io                  []                 []              [get list watch]


Name:         dns-monitoring
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                    Non-Resource URLs  Resource Names  Verbs
  ---------                    -----------------  --------------  -----
  dnses.operator.openshift.io  []                 []              [get]


Name:         edit
Labels:       kubernetes.io/bootstrapping=rbac-defaults
              rbac.authorization.k8s.io/aggregate-to-admin=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                            Non-Resource URLs  Resource Names  Verbs
  ---------                                            -----------------  --------------  -----
  serviceaccounts                                      []                 []              [create delete deletecollection get list patch update watch impersonate]
  buildconfigs/webhooks                                []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs                                         []                 []              [create delete deletecollection get list patch update watch]
  buildlogs                                            []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs/scale                              []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs                                    []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimages                                    []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings                                  []                 []              [create delete deletecollection get list patch update watch]
  imagestreams/secrets                                 []                 []              [create delete deletecollection get list patch update watch]
  imagestreams                                         []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags                                      []                 []              [create delete deletecollection get list patch update watch]
  imagetags                                            []                 []              [create delete deletecollection get list patch update watch]
  processedtemplates                                   []                 []              [create delete deletecollection get list patch update watch]
  routes                                               []                 []              [create delete deletecollection get list patch update watch]
  secrets                                              []                 []              [create delete deletecollection get list patch update watch]
  templateconfigs                                      []                 []              [create delete deletecollection get list patch update watch]
  templateinstances                                    []                 []              [create delete deletecollection get list patch update watch]
  templates                                            []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs.apps.openshift.io/scale            []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs.apps.openshift.io                  []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs.build.openshift.io/webhooks             []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs.build.openshift.io                      []                 []              [create delete deletecollection get list patch update watch]
  buildlogs.build.openshift.io                         []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimages.image.openshift.io                 []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings.image.openshift.io               []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io/secrets              []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io                      []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags.image.openshift.io                   []                 []              [create delete deletecollection get list patch update watch]
  imagetags.image.openshift.io                         []                 []              [create delete deletecollection get list patch update watch]
  routes.route.openshift.io                            []                 []              [create delete deletecollection get list patch update watch]
  processedtemplates.template.openshift.io             []                 []              [create delete deletecollection get list patch update watch]
  templateconfigs.template.openshift.io                []                 []              [create delete deletecollection get list patch update watch]
  templateinstances.template.openshift.io              []                 []              [create delete deletecollection get list patch update watch]
  templates.template.openshift.io                      []                 []              [create delete deletecollection get list patch update watch]
  configmaps                                           []                 []              [create delete deletecollection patch update get list watch]
  endpoints                                            []                 []              [create delete deletecollection patch update get list watch]
  persistentvolumeclaims                               []                 []              [create delete deletecollection patch update get list watch]
  pods                                                 []                 []              [create delete deletecollection patch update get list watch]
  replicationcontrollers/scale                         []                 []              [create delete deletecollection patch update get list watch]
  replicationcontrollers                               []                 []              [create delete deletecollection patch update get list watch]
  services                                             []                 []              [create delete deletecollection patch update get list watch]
  daemonsets.apps                                      []                 []              [create delete deletecollection patch update get list watch]
  deployments.apps/scale                               []                 []              [create delete deletecollection patch update get list watch]
  deployments.apps                                     []                 []              [create delete deletecollection patch update get list watch]
  replicasets.apps/scale                               []                 []              [create delete deletecollection patch update get list watch]
  replicasets.apps                                     []                 []              [create delete deletecollection patch update get list watch]
  statefulsets.apps/scale                              []                 []              [create delete deletecollection patch update get list watch]
  statefulsets.apps                                    []                 []              [create delete deletecollection patch update get list watch]
  horizontalpodautoscalers.autoscaling                 []                 []              [create delete deletecollection patch update get list watch]
  cronjobs.batch                                       []                 []              [create delete deletecollection patch update get list watch]
  jobs.batch                                           []                 []              [create delete deletecollection patch update get list watch]
  daemonsets.extensions                                []                 []              [create delete deletecollection patch update get list watch]
  deployments.extensions/scale                         []                 []              [create delete deletecollection patch update get list watch]
  deployments.extensions                               []                 []              [create delete deletecollection patch update get list watch]
  ingresses.extensions                                 []                 []              [create delete deletecollection patch update get list watch]
  networkpolicies.extensions                           []                 []              [create delete deletecollection patch update get list watch]
  replicasets.extensions/scale                         []                 []              [create delete deletecollection patch update get list watch]
  replicasets.extensions                               []                 []              [create delete deletecollection patch update get list watch]
  replicationcontrollers.extensions/scale              []                 []              [create delete deletecollection patch update get list watch]
  ingresses.networking.k8s.io                          []                 []              [create delete deletecollection patch update get list watch]
  networkpolicies.networking.k8s.io                    []                 []              [create delete deletecollection patch update get list watch]
  poddisruptionbudgets.policy                          []                 []              [create delete deletecollection patch update get list watch]
  deployments.apps/rollback                            []                 []              [create delete deletecollection patch update]
  deployments.extensions/rollback                      []                 []              [create delete deletecollection patch update]
  subscriptions.operators.coreos.com                   []                 []              [create update patch delete get list watch]
  buildconfigs/instantiate                             []                 []              [create]
  buildconfigs/instantiatebinary                       []                 []              [create]
  builds/clone                                         []                 []              [create]
  deploymentconfigrollbacks                            []                 []              [create]
  deploymentconfigs/instantiate                        []                 []              [create]
  deploymentconfigs/rollback                           []                 []              [create]
  imagestreamimports                                   []                 []              [create]
  routes/custom-host                                   []                 []              [create]
  deploymentconfigrollbacks.apps.openshift.io          []                 []              [create]
  deploymentconfigs.apps.openshift.io/instantiate      []                 []              [create]
  deploymentconfigs.apps.openshift.io/rollback         []                 []              [create]
  buildconfigs.build.openshift.io/instantiate          []                 []              [create]
  buildconfigs.build.openshift.io/instantiatebinary    []                 []              [create]
  builds.build.openshift.io/clone                      []                 []              [create]
  imagestreamimports.image.openshift.io                []                 []              [create]
  routes.route.openshift.io/custom-host                []                 []              [create]
  catalogsources.operators.coreos.com                  []                 []              [delete get list watch]
  clusterserviceversions.operators.coreos.com          []                 []              [delete get list watch]
  installplans.operators.coreos.com                    []                 []              [delete get list watch]
  jenkins.build.openshift.io                           []                 []              [edit view]
  builds                                               []                 []              [get create delete deletecollection list patch update watch]
  builds.build.openshift.io                            []                 []              [get create delete deletecollection list patch update watch]
  pods/attach                                          []                 []              [get list watch create delete deletecollection patch update]
  pods/exec                                            []                 []              [get list watch create delete deletecollection patch update]
  pods/portforward                                     []                 []              [get list watch create delete deletecollection patch update]
  pods/proxy                                           []                 []              [get list watch create delete deletecollection patch update]
  services/proxy                                       []                 []              [get list watch create delete deletecollection patch update]
  volumesnapshots.snapshot.storage.k8s.io              []                 []              [get list watch create update patch delete deletecollection]
  packagemanifests.packages.operators.coreos.com       []                 []              [get list watch create update patch delete]
  appliedclusterresourcequotas                         []                 []              [get list watch]
  bindings                                             []                 []              [get list watch]
  builds/log                                           []                 []              [get list watch]
  deploymentconfigs/log                                []                 []              [get list watch]
  deploymentconfigs/status                             []                 []              [get list watch]
  events                                               []                 []              [get list watch]
  imagestreams/status                                  []                 []              [get list watch]
  limitranges                                          []                 []              [get list watch]
  namespaces/status                                    []                 []              [get list watch]
  namespaces                                           []                 []              [get list watch]
  persistentvolumeclaims/status                        []                 []              [get list watch]
  pods/log                                             []                 []              [get list watch]
  pods/status                                          []                 []              [get list watch]
  replicationcontrollers/status                        []                 []              [get list watch]
  resourcequotas/status                                []                 []              [get list watch]
  resourcequotas                                       []                 []              [get list watch]
  resourcequotausages                                  []                 []              [get list watch]
  routes/status                                        []                 []              [get list watch]
  services/status                                      []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/log              []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/status           []                 []              [get list watch]
  controllerrevisions.apps                             []                 []              [get list watch]
  daemonsets.apps/status                               []                 []              [get list watch]
  deployments.apps/status                              []                 []              [get list watch]
  replicasets.apps/status                              []                 []              [get list watch]
  statefulsets.apps/status                             []                 []              [get list watch]
  horizontalpodautoscalers.autoscaling/status          []                 []              [get list watch]
  cronjobs.batch/status                                []                 []              [get list watch]
  jobs.batch/status                                    []                 []              [get list watch]
  builds.build.openshift.io/log                        []                 []              [get list watch]
  daemonsets.extensions/status                         []                 []              [get list watch]
  deployments.extensions/status                        []                 []              [get list watch]
  ingresses.extensions/status                          []                 []              [get list watch]
  replicasets.extensions/status                        []                 []              [get list watch]
  imagestreams.image.openshift.io/status               []                 []              [get list watch]
  nodes.metrics.k8s.io                                 []                 []              [get list watch]
  pods.metrics.k8s.io                                  []                 []              [get list watch]
  ingresses.networking.k8s.io/status                   []                 []              [get list watch]
  operatorgroups.operators.coreos.com                  []                 []              [get list watch]
  packagemanifests.packages.operators.coreos.com/icon  []                 []              [get list watch]
  poddisruptionbudgets.policy/status                   []                 []              [get list watch]
  appliedclusterresourcequotas.quota.openshift.io      []                 []              [get list watch]
  routes.route.openshift.io/status                     []                 []              [get list watch]
  imagestreams/layers                                  []                 []              [get update]
  imagestreams.image.openshift.io/layers               []                 []              [get update]
  projects                                             []                 []              [get]
  projects.project.openshift.io                        []                 []              [get]
  builds/details                                       []                 []              [update]
  builds.build.openshift.io/details                    []                 []              [update]


Name:         global-operators-admin
Labels:       olm.owner=global-operators
              olm.owner.kind=OperatorGroup
              olm.owner.namespace=openshift-operators
Annotations:  &lt;none&gt;
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----


Name:         global-operators-edit
Labels:       olm.owner=global-operators
              olm.owner.kind=OperatorGroup
              olm.owner.namespace=openshift-operators
Annotations:  &lt;none&gt;
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----


Name:         global-operators-view
Labels:       olm.owner=global-operators
              olm.owner.kind=OperatorGroup
              olm.owner.namespace=openshift-operators
Annotations:  &lt;none&gt;
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----


Name:         grafana
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  tokenreviews.authentication.k8s.io         []                 []              [create]
  subjectaccessreviews.authorization.k8s.io  []                 []              [create]


Name:         helm-chartrepos-viewer
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                Non-Resource URLs  Resource Names  Verbs
  ---------                                -----------------  --------------  -----
  helmchartrepositories.helm.openshift.io  []                 []              [get list]


Name:         insights-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                    Non-Resource URLs  Resource Names  Verbs
  ---------                                    -----------------  --------------  -----
  clusteroperators.config.openshift.io         []                 []              [create]
  clusteroperators.config.openshift.io/status  []                 [insights]      [get update patch]
  clusteroperators.config.openshift.io         []                 [insights]      [get watch]
  namespaces                                   []                 []              [get]


Name:         insights-operator-gather
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  nodes                                             []                 []              [get list watch proxy]
  *.config.openshift.io                             []                 []              [get list watch]
  configs.imageregistry.operator.openshift.io       []                 []              [get list watch]
  imagepruners.imageregistry.operator.openshift.io  []                 []              [get list watch]
  *.installers.datahub.sap.com                      []                 []              [get list watch]
  machinesets.machine.openshift.io                  []                 []              [get list watch]
  *.operator.openshift.io                           []                 []              [get list watch]
  *.operators.coreos.com                            []                 []              [get list watch]
  nodes/log                                         []                 []              [get]
  nodes/metrics                                     []                 []              [get]
  nodes/proxy                                       []                 []              [get]
  nodes/stats                                       []                 []              [get]
  poddisruptionbudgets.policy                       []                 []              [list get watch]
  events                                            []                 []              [list]


Name:         kube-apiserver
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources    Non-Resource URLs  Resource Names  Verbs
  ---------    -----------------  --------------  -----
  nodes/proxy  []                 []              [get create]


Name:         kube-state-metrics
Labels:       app.kubernetes.io/name=kube-state-metrics
              app.kubernetes.io/version=v1.9.5
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                                     -----------------  --------------  -----
  tokenreviews.authentication.k8s.io                            []                 []              [create]
  subjectaccessreviews.authorization.k8s.io                     []                 []              [create]
  configmaps                                                    []                 []              [list watch]
  endpoints                                                     []                 []              [list watch]
  limitranges                                                   []                 []              [list watch]
  namespaces                                                    []                 []              [list watch]
  nodes                                                         []                 []              [list watch]
  persistentvolumeclaims                                        []                 []              [list watch]
  persistentvolumes                                             []                 []              [list watch]
  pods                                                          []                 []              [list watch]
  replicationcontrollers                                        []                 []              [list watch]
  resourcequotas                                                []                 []              [list watch]
  secrets                                                       []                 []              [list watch]
  services                                                      []                 []              [list watch]
  mutatingwebhookconfigurations.admissionregistration.k8s.io    []                 []              [list watch]
  validatingwebhookconfigurations.admissionregistration.k8s.io  []                 []              [list watch]
  daemonsets.apps                                               []                 []              [list watch]
  deployments.apps                                              []                 []              [list watch]
  replicasets.apps                                              []                 []              [list watch]
  statefulsets.apps                                             []                 []              [list watch]
  horizontalpodautoscalers.autoscaling                          []                 []              [list watch]
  cronjobs.batch                                                []                 []              [list watch]
  jobs.batch                                                    []                 []              [list watch]
  certificatesigningrequests.certificates.k8s.io                []                 []              [list watch]
  daemonsets.extensions                                         []                 []              [list watch]
  deployments.extensions                                        []                 []              [list watch]
  ingresses.extensions                                          []                 []              [list watch]
  replicasets.extensions                                        []                 []              [list watch]
  networkpolicies.networking.k8s.io                             []                 []              [list watch]
  poddisruptionbudgets.policy                                   []                 []              [list watch]
  storageclasses.storage.k8s.io                                 []                 []              [list watch]
  volumeattachments.storage.k8s.io                              []                 []              [list watch]


Name:         machine-api-controllers
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  pods/eviction                                     []                 []              [create]
  tokenreviews.authentication.k8s.io                []                 []              [create]
  subjectaccessreviews.authorization.k8s.io         []                 []              [create]
  nodes                                             []                 []              [get list watch create update patch delete]
  pods                                              []                 []              [get list watch]
  daemonsets.apps                                   []                 []              [get list watch]
  dnses.config.openshift.io                         []                 []              [get list watch]
  infrastructures.config.openshift.io               []                 []              [get list watch]
  daemonsets.extensions                             []                 []              [get list watch]
  securitycontextconstraints.security.openshift.io  []                 [privileged]    [use]


Name:         machine-api-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                                     -----------------  --------------  -----
  clusteroperators.config.openshift.io/status                   []                 []              [create get update]
  clusteroperators.config.openshift.io                          []                 []              [create get update]
  events                                                        []                 []              [create watch list patch]
  tokenreviews.authentication.k8s.io                            []                 []              [create]
  subjectaccessreviews.authorization.k8s.io                     []                 []              [create]
  mutatingwebhookconfigurations.admissionregistration.k8s.io    []                 []              [get list watch create update]
  validatingwebhookconfigurations.admissionregistration.k8s.io  []                 []              [get list watch create update]
  featuregates.config.openshift.io/status                       []                 []              [get list watch]
  featuregates.config.openshift.io                              []                 []              [get list watch]
  proxies.config.openshift.io                                   []                 []              [get list watch]
  provisionings.metal3.io                                       []                 []              [get list]
  infrastructures.config.openshift.io/status                    []                 []              [get]
  infrastructures.config.openshift.io                           []                 []              [get]


Name:         machine-api-operator:cluster-reader
Labels:       rbac.authorization.k8s.io/aggregate-to-cluster-reader=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                 Non-Resource URLs  Resource Names  Verbs
  ---------                                 -----------------  --------------  -----
  machinehealthchecks.machine.openshift.io  []                 []              [get list watch]
  machines.machine.openshift.io             []                 []              [get list watch]
  machinesets.machine.openshift.io          []                 []              [get list watch]


Name:         machine-config-controller
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  configmaps                                        []                 []              [*]
  secrets                                           []                 []              [*]
  clusterversions.config.openshift.io               []                 []              [*]
  featuregates.config.openshift.io                  []                 []              [*]
  images.config.openshift.io                        []                 []              [*]
  *.machineconfiguration.openshift.io               []                 []              [*]
  nodes                                             []                 []              [get list watch patch]
  schedulers.config.openshift.io                    []                 []              [get list watch]
  etcds.operator.openshift.io                       []                 []              [get list watch]
  imagecontentsourcepolicies.operator.openshift.io  []                 []              [get list watch]


Name:         machine-config-controller-events
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  events     []                 []              [create patch]


Name:         machine-config-daemon
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  pods                                              []                 []              [*]
  machineconfigs.machineconfiguration.openshift.io  []                 []              [*]
  pods/eviction                                     []                 []              [create]
  subjectaccessreviews.authentication.k8s.io        []                 []              [create]
  tokenreviews.authentication.k8s.io                []                 []              [create]
  subjectaccessreviews.authorization.k8s.io         []                 []              [create]
  nodes                                             []                 []              [get list watch patch update]
  daemonsets.apps                                   []                 []              [get]
  daemonsets.extensions                             []                 []              [get]


Name:         machine-config-daemon-events
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  events     []                 []              [create patch]


Name:         machine-config-server
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                             Non-Resource URLs  Resource Names  Verbs
  ---------                                             -----------------  --------------  -----
  machineconfigpools.machineconfiguration.openshift.io  []                 []              [*]
  machineconfigs.machineconfiguration.openshift.io      []                 []              [*]


Name:         marketplace-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  clusteroperators.config.openshift.io/status     []                 []              [create get update]
  clusteroperators.config.openshift.io            []                 []              [create get update]
  catalogsources.operators.coreos.com             []                 []              [get create delete update list watch]
  operatorsources.operators.coreos.com            []                 []              [get create delete update list watch]
  customresourcedefinitions.apiextensions.k8s.io  []                 []              [get delete]
  operatorhubs.config.openshift.io/status         []                 []              [get list watch update]
  operatorhubs.config.openshift.io                []                 []              [get list watch update]
  configmaps                                      []                 []              [get list watch]
  namespaces                                      []                 []              [get list watch]
  subscriptions.operators.coreos.com              []                 []              [get update list]
  secrets                                         []                 []              [list watch]
  serviceaccounts                                 []                 []              [list watch]
  services                                        []                 []              [list watch]
  deployments.apps                                []                 []              [list watch]
  rolebindings.rbac.authorization.k8s.io          []                 []              [list watch]
  roles.rbac.authorization.k8s.io                 []                 []              [list watch]


Name:         metrics-daemon-role
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  tokenreviews.authentication.k8s.io              []                 []              [create]
  subjectaccessreviews.authorization.k8s.io       []                 []              [create]
  pods                                            []                 []              [get watch list]
  network-attachment-definitions.k8s.cni.cncf.io  []                 []              [get watch list]


Name:         monitoring-edit
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                              Non-Resource URLs  Resource Names  Verbs
  ---------                              -----------------  --------------  -----
  podmonitors.monitoring.coreos.com      []                 []              [*]
  prometheusrules.monitoring.coreos.com  []                 []              [*]
  servicemonitors.monitoring.coreos.com  []                 []              [*]


Name:         monitoring-rules-edit
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                              Non-Resource URLs  Resource Names  Verbs
  ---------                              -----------------  --------------  -----
  prometheusrules.monitoring.coreos.com  []                 []              [*]


Name:         monitoring-rules-view
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                              Non-Resource URLs  Resource Names  Verbs
  ---------                              -----------------  --------------  -----
  prometheusrules.monitoring.coreos.com  []                 []              [get list watch]


Name:         multus
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                              Non-Resource URLs  Resource Names  Verbs
  ---------                                              -----------------  --------------  -----
  events                                                 []                 []              [create patch update]
  pods/status                                            []                 []              [get list watch patch update]
  pods                                                   []                 []              [get list watch patch update]
  namespaces                                             []                 []              [get list watch]
  customresourcedefinitions.apiextensions.k8s.io/status  []                 []              [get list watch]
  customresourcedefinitions.apiextensions.k8s.io         []                 []              [get list watch]
  *.k8s.cni.cncf.io                                      []                 []              [get list watch]


Name:         multus-admission-controller-webhook
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                                     -----------------  --------------  -----
  tokenreviews.authentication.k8s.io                            []                 []              [create]
  subjectaccessreviews.authorization.k8s.io                     []                 []              [create]
  namespaces                                                    []                 []              [get patch update]
  validatingwebhookconfigurations.admissionregistration.k8s.io  []                 []              [get patch update]


Name:         nfs-client-provisioner-runner
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                      Non-Resource URLs  Resource Names  Verbs
  ---------                      -----------------  --------------  -----
  events                         []                 []              [create update patch]
  persistentvolumes              []                 []              [get list watch create delete]
  persistentvolumeclaims         []                 []              [get list watch update]
  storageclasses.storage.k8s.io  []                 []              [get list watch]


Name:         node-exporter
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names   Verbs
  ---------                                         -----------------  --------------   -----
  tokenreviews.authentication.k8s.io                []                 []               [create]
  subjectaccessreviews.authorization.k8s.io         []                 []               [create]
  securitycontextconstraints.security.openshift.io  []                 [node-exporter]  [use]


Name:         olm-operators-admin
Labels:       olm.owner=olm-operators
              olm.owner.kind=OperatorGroup
              olm.owner.namespace=openshift-operator-lifecycle-manager
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  packagemanifests.packages.operators.coreos.com  []                 []              [*]


Name:         olm-operators-edit
Labels:       olm.owner=olm-operators
              olm.owner.kind=OperatorGroup
              olm.owner.namespace=openshift-operator-lifecycle-manager
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  packagemanifests.packages.operators.coreos.com  []                 []              [create update patch delete]


Name:         olm-operators-view
Labels:       olm.owner=olm-operators
              olm.owner.kind=OperatorGroup
              olm.owner.namespace=openshift-operator-lifecycle-manager
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  packagemanifests.packages.operators.coreos.com  []                 []              [get list watch]


Name:         openshift-cluster-monitoring-admin
Labels:       olm.owner=openshift-cluster-monitoring
              olm.owner.kind=OperatorGroup
              olm.owner.namespace=openshift-monitoring
Annotations:  &lt;none&gt;
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----


Name:         openshift-cluster-monitoring-edit
Labels:       olm.owner=openshift-cluster-monitoring
              olm.owner.kind=OperatorGroup
              olm.owner.namespace=openshift-monitoring
Annotations:  &lt;none&gt;
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----


Name:         openshift-cluster-monitoring-view
Labels:       olm.owner=openshift-cluster-monitoring
              olm.owner.kind=OperatorGroup
              olm.owner.namespace=openshift-monitoring
Annotations:  &lt;none&gt;
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----


Name:         openshift-csi-snapshot-controller-runner
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  volumesnapshotcontents.snapshot.storage.k8s.io  []                 []              [create get list watch update delete]
  persistentvolumeclaims                          []                 []              [get list watch update]
  volumesnapshots.snapshot.storage.k8s.io         []                 []              [get list watch update]
  persistentvolumes                               []                 []              [get list watch]
  volumesnapshotclasses.snapshot.storage.k8s.io   []                 []              [get list watch]
  storageclasses.storage.k8s.io                   []                 []              [get list watch]
  events                                          []                 []              [list watch create update patch]
  volumesnapshots.snapshot.storage.k8s.io/status  []                 []              [update]


Name:         openshift-dns
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  tokenreviews.authentication.k8s.io         []                 []              [create]
  subjectaccessreviews.authorization.k8s.io  []                 []              [create]
  endpoints                                  []                 []              [list watch]
  namespaces                                 []                 []              [list watch]
  pods                                       []                 []              [list watch]
  services                                   []                 []              [list watch]


Name:         openshift-dns-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                      Non-Resource URLs  Resource Names  Verbs
  ---------                                      -----------------  --------------  -----
  configmaps                                     []                 []              [*]
  endpoints                                      []                 []              [*]
  namespaces                                     []                 []              [*]
  pods                                           []                 []              [*]
  serviceaccounts                                []                 []              [*]
  services                                       []                 []              [*]
  daemonsets.apps                                []                 []              [*]
  daemonsets.extensions                          []                 []              [*]
  dnses.operator.openshift.io                    []                 []              [*]
  clusterroles.rbac.authorization.k8s.io         []                 []              [create get list watch update]
  clusterrolebindings.rbac.authorization.k8s.io  []                 []              [create get list watch]
  rolebindings.rbac.authorization.k8s.io         []                 []              [create get list watch]
  roles.rbac.authorization.k8s.io                []                 []              [create get list watch]
  clusteroperators.config.openshift.io           []                 []              [create get]
  networks.config.openshift.io                   []                 []              [create get]
  servicemonitors.monitoring.coreos.com          []                 []              [create update get]
  tokenreviews.authentication.k8s.io             []                 []              [create]
  subjectaccessreviews.authorization.k8s.io      []                 []              [create]
  clusteroperators.config.openshift.io/status    []                 []              [update]
  dnses.operator.openshift.io/status             []                 []              [update]


Name:         openshift-ingress-operator
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  configmaps                                        []                 []              [*]
  endpoints                                         []                 []              [*]
  events                                            []                 []              [*]
  namespaces                                        []                 []              [*]
  pods                                              []                 []              [*]
  secrets                                           []                 []              [*]
  serviceaccounts                                   []                 []              [*]
  services                                          []                 []              [*]
  deployments.apps                                  []                 []              [*]
  dnsrecords.ingress.operator.openshift.io/status   []                 []              [*]
  dnsrecords.ingress.operator.openshift.io          []                 []              [*]
  ingresscontrollers.operator.openshift.io/status   []                 []              [*]
  ingresscontrollers.operator.openshift.io          []                 []              [*]
  poddisruptionbudgets.policy                       []                 []              [*]
  clusterrolebindings.rbac.authorization.k8s.io     []                 []              [create get list watch update]
  clusterroles.rbac.authorization.k8s.io            []                 []              [create get list watch update]
  rolebindings.rbac.authorization.k8s.io            []                 []              [create get list watch update]
  roles.rbac.authorization.k8s.io                   []                 []              [create get list watch update]
  servicemonitors.monitoring.coreos.com             []                 []              [create get update]
  clusteroperators.config.openshift.io              []                 []              [create get]
  tokenreviews.authentication.k8s.io                []                 []              [create]
  subjectaccessreviews.authorization.k8s.io         []                 []              [create]
  dnses.config.openshift.io                         []                 []              [get list watch]
  infrastructures.config.openshift.io               []                 []              [get list watch]
  ingresses.config.openshift.io                     []                 []              [get list watch]
  apiservers.config.openshift.io                    []                 []              [get]
  networks.config.openshift.io                      []                 []              [get]
  routers.route.openshift.io/metrics                []                 []              [get]
  endpointslices.discovery.k8s.io                   []                 []              [list watch]
  routes.route.openshift.io                         []                 []              [list watch]
  clusteroperators.config.openshift.io/status       []                 []              [update]
  routes.route.openshift.io/status                  []                 []              [update]
  securitycontextconstraints.security.openshift.io  []                 [hostnetwork]   [use]


Name:         openshift-ingress-router
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  tokenreviews.authentication.k8s.io                []                 []              [create]
  subjectaccessreviews.authorization.k8s.io         []                 []              [create]
  endpoints                                         []                 []              [list watch]
  namespaces                                        []                 []              [list watch]
  services                                          []                 []              [list watch]
  endpointslices.discovery.k8s.io                   []                 []              [list watch]
  routes.route.openshift.io                         []                 []              [list watch]
  routes.route.openshift.io/status                  []                 []              [update]
  securitycontextconstraints.security.openshift.io  []                 [hostnetwork]   [use]


Name:         openshift-sdn
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                   Non-Resource URLs  Resource Names  Verbs
  ---------                                   -----------------  --------------  -----
  events                                      []                 []              [create patch update]
  tokenreviews.authentication.k8s.io          []                 []              [create]
  subjectaccessreviews.authorization.k8s.io   []                 []              [create]
  nodes                                       []                 []              [get list watch patch]
  endpoints                                   []                 []              [get list watch]
  namespaces                                  []                 []              [get list watch]
  pods                                        []                 []              [get list watch]
  services                                    []                 []              [get list watch]
  networkpolicies.extensions                  []                 []              [get list watch]
  clusternetworks.network.openshift.io        []                 []              [get list watch]
  egressnetworkpolicies.network.openshift.io  []                 []              [get list watch]
  hostsubnets.network.openshift.io            []                 []              [get list watch]
  netnamespaces.network.openshift.io          []                 []              [get list watch]
  networkpolicies.networking.k8s.io           []                 []              [get list watch]


Name:         openshift-sdn-controller
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                   Non-Resource URLs  Resource Names  Verbs
  ---------                                   -----------------  --------------  -----
  clusternetworks.network.openshift.io        []                 []              [get list watch create update patch delete]
  egressnetworkpolicies.network.openshift.io  []                 []              [get list watch create update patch delete]
  hostsubnets.network.openshift.io            []                 []              [get list watch create update patch delete]
  netnamespaces.network.openshift.io          []                 []              [get list watch create update patch delete]
  namespaces                                  []                 []              [list get watch]
  nodes                                       []                 []              [list get watch]
  nodes/status                                []                 []              [patch update]


Name:         openshift-state-metrics
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  tokenreviews.authentication.k8s.io         []                 []              [create]
  subjectaccessreviews.authorization.k8s.io  []                 []              [create]
  deploymentconfigs.apps.openshift.io        []                 []              [list watch]
  buildconfigs.build.openshift.io            []                 []              [list watch]
  builds.build.openshift.io                  []                 []              [list watch]
  clusterresourcequotas.quota.openshift.io   []                 []              [list watch]
  routes.route.openshift.io                  []                 []              [list watch]
  groups.user.openshift.io                   []                 []              [list watch]


Name:         operatorhub-config-reader
Labels:       rbac.authorization.k8s.io/aggregate-to-cluster-reader=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                         Non-Resource URLs  Resource Names  Verbs
  ---------                         -----------------  --------------  -----
  operatorhubs.config.openshift.io  []                 []              [get list watch]


Name:         packagemanifests-v1-admin
Labels:       olm.opgroup.permissions/aggregate-to-4bca9f23e412d79d-admin=true
              rbac.authorization.k8s.io/aggregate-to-admin=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  packagemanifests.packages.operators.coreos.com  []                 []              [*]


Name:         packagemanifests-v1-edit
Labels:       olm.opgroup.permissions/aggregate-to-4bca9f23e412d79d-edit=true
              rbac.authorization.k8s.io/aggregate-to-edit=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  packagemanifests.packages.operators.coreos.com  []                 []              [create update patch delete]


Name:         packagemanifests-v1-view
Labels:       olm.opgroup.permissions/aggregate-to-4bca9f23e412d79d-view=true
              rbac.authorization.k8s.io/aggregate-to-view=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  packagemanifests.packages.operators.coreos.com  []                 []              [get list watch]


Name:         prometheus-adapter
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources   Non-Resource URLs  Resource Names  Verbs
  ---------   -----------------  --------------  -----
  namespaces  []                 []              [get list watch]
  nodes       []                 []              [get list watch]
  pods        []                 []              [get list watch]
  services    []                 []              [get list watch]


Name:         prometheus-k8s
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  tokenreviews.authentication.k8s.io                []                 []              [create]
  subjectaccessreviews.authorization.k8s.io         []                 []              [create]
                                                    [/metrics]         []              [get]
  namespaces                                        []                 []              [get]
  nodes/metrics                                     []                 []              [get]
  securitycontextconstraints.security.openshift.io  []                 [nonroot]       [use]


Name:         prometheus-operator
Labels:       app.kubernetes.io/component=controller
              app.kubernetes.io/name=prometheus-operator
              app.kubernetes.io/version=v0.42.1
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  configmaps                                      []                 []              [*]
  secrets                                         []                 []              [*]
  statefulsets.apps                               []                 []              [*]
  alertmanagers.monitoring.coreos.com/finalizers  []                 []              [*]
  alertmanagers.monitoring.coreos.com             []                 []              [*]
  podmonitors.monitoring.coreos.com               []                 []              [*]
  probes.monitoring.coreos.com                    []                 []              [*]
  prometheuses.monitoring.coreos.com/finalizers   []                 []              [*]
  prometheuses.monitoring.coreos.com              []                 []              [*]
  prometheusrules.monitoring.coreos.com           []                 []              [*]
  servicemonitors.monitoring.coreos.com           []                 []              [*]
  thanosrulers.monitoring.coreos.com/finalizers   []                 []              [*]
  thanosrulers.monitoring.coreos.com              []                 []              [*]
  tokenreviews.authentication.k8s.io              []                 []              [create]
  subjectaccessreviews.authorization.k8s.io       []                 []              [create]
  endpoints                                       []                 []              [get create update delete]
  services/finalizers                             []                 []              [get create update delete]
  services                                        []                 []              [get create update delete]
  namespaces                                      []                 []              [get list watch]
  pods                                            []                 []              [list delete]
  nodes                                           []                 []              [list watch]


Name:         registry-admin
Labels:       rbac.authorization.k8s.io/aggregate-to-admin=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                              Non-Resource URLs  Resource Names  Verbs
  ---------                                              -----------------  --------------  -----
  imagestreamimages                                      []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings                                    []                 []              [create delete deletecollection get list patch update watch]
  imagestreams/secrets                                   []                 []              [create delete deletecollection get list patch update watch]
  imagestreams                                           []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags                                        []                 []              [create delete deletecollection get list patch update watch]
  imagetags                                              []                 []              [create delete deletecollection get list patch update watch]
  rolebindings                                           []                 []              [create delete deletecollection get list patch update watch]
  roles                                                  []                 []              [create delete deletecollection get list patch update watch]
  secrets                                                []                 []              [create delete deletecollection get list patch update watch]
  serviceaccounts                                        []                 []              [create delete deletecollection get list patch update watch]
  rolebindings.authorization.openshift.io                []                 []              [create delete deletecollection get list patch update watch]
  roles.authorization.openshift.io                       []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimages.image.openshift.io                   []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings.image.openshift.io                 []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io/secrets                []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io                        []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags.image.openshift.io                     []                 []              [create delete deletecollection get list patch update watch]
  imagetags.image.openshift.io                           []                 []              [create delete deletecollection get list patch update watch]
  rolebindings.rbac.authorization.k8s.io                 []                 []              [create delete deletecollection get list patch update watch]
  roles.rbac.authorization.k8s.io                        []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimports                                     []                 []              [create]
  localresourceaccessreviews                             []                 []              [create]
  localsubjectaccessreviews                              []                 []              [create]
  resourceaccessreviews                                  []                 []              [create]
  subjectaccessreviews                                   []                 []              [create]
  subjectrulesreviews                                    []                 []              [create]
  localsubjectaccessreviews.authorization.k8s.io         []                 []              [create]
  localresourceaccessreviews.authorization.openshift.io  []                 []              [create]
  localsubjectaccessreviews.authorization.openshift.io   []                 []              [create]
  resourceaccessreviews.authorization.openshift.io       []                 []              [create]
  subjectaccessreviews.authorization.openshift.io        []                 []              [create]
  subjectrulesreviews.authorization.openshift.io         []                 []              [create]
  imagestreamimports.image.openshift.io                  []                 []              [create]
  projects                                               []                 []              [delete get]
  projects.project.openshift.io                          []                 []              [delete get]
  imagestreams/layers                                    []                 []              [get update]
  imagestreams.image.openshift.io/layers                 []                 []              [get update]
  namespaces                                             []                 []              [get]


Name:         registry-editor
Labels:       rbac.authorization.k8s.io/aggregate-to-edit=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                Non-Resource URLs  Resource Names  Verbs
  ---------                                -----------------  --------------  -----
  imagestreamimages                        []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings                      []                 []              [create delete deletecollection get list patch update watch]
  imagestreams/secrets                     []                 []              [create delete deletecollection get list patch update watch]
  imagestreams                             []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags                          []                 []              [create delete deletecollection get list patch update watch]
  imagetags                                []                 []              [create delete deletecollection get list patch update watch]
  secrets                                  []                 []              [create delete deletecollection get list patch update watch]
  serviceaccounts                          []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimages.image.openshift.io     []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings.image.openshift.io   []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io/secrets  []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io          []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags.image.openshift.io       []                 []              [create delete deletecollection get list patch update watch]
  imagetags.image.openshift.io             []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimports                       []                 []              [create]
  imagestreamimports.image.openshift.io    []                 []              [create]
  imagestreams/layers                      []                 []              [get update]
  imagestreams.image.openshift.io/layers   []                 []              [get update]
  namespaces                               []                 []              [get]
  projects                                 []                 []              [get]
  projects.project.openshift.io            []                 []              [get]


Name:         registry-monitoring
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                            Non-Resource URLs  Resource Names  Verbs
  ---------                            -----------------  --------------  -----
  registry.image.openshift.io/metrics  []                 []              [get]


Name:         registry-viewer
Labels:       rbac.authorization.k8s.io/aggregate-to-view=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                               Non-Resource URLs  Resource Names  Verbs
  ---------                               -----------------  --------------  -----
  imagestreamimages                       []                 []              [get list watch]
  imagestreammappings                     []                 []              [get list watch]
  imagestreams                            []                 []              [get list watch]
  imagestreamtags                         []                 []              [get list watch]
  imagetags                               []                 []              [get list watch]
  imagestreamimages.image.openshift.io    []                 []              [get list watch]
  imagestreammappings.image.openshift.io  []                 []              [get list watch]
  imagestreams.image.openshift.io         []                 []              [get list watch]
  imagestreamtags.image.openshift.io      []                 []              [get list watch]
  imagetags.image.openshift.io            []                 []              [get list watch]
  imagestreams/layers                     []                 []              [get]
  namespaces                              []                 []              [get]
  projects                                []                 []              [get]
  imagestreams.image.openshift.io/layers  []                 []              [get]
  projects.project.openshift.io           []                 []              [get]


Name:         resource-metrics-server-resources
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources         Non-Resource URLs  Resource Names  Verbs
  ---------         -----------------  --------------  -----
  *.metrics.k8s.io  []                 []              [*]


Name:         router-monitoring
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                           Non-Resource URLs  Resource Names  Verbs
  ---------                           -----------------  --------------  -----
  routers.route.openshift.io/metrics  []                 []              [get]


Name:         self-access-reviewer
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                           Non-Resource URLs  Resource Names  Verbs
  ---------                                           -----------------  --------------  -----
  selfsubjectrulesreviews                             []                 []              [create]
  selfsubjectaccessreviews.authorization.k8s.io       []                 []              [create]
  selfsubjectrulesreviews.authorization.openshift.io  []                 []              [create]


Name:         self-provisioner
Labels:       &lt;none&gt;
Annotations:  openshift.io/description: A user that can request projects.
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                             Non-Resource URLs  Resource Names  Verbs
  ---------                             -----------------  --------------  -----
  projectrequests                       []                 []              [create]
  projectrequests.project.openshift.io  []                 []              [create]


Name:         storage-admin
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  persistentvolumes                               []                 []              [create delete deletecollection get list patch update watch]
  storageclasses.storage.k8s.io                   []                 []              [create delete deletecollection get list patch update watch]
  volumesnapshotclasses.snapshot.storage.k8s.io   []                 []              [get list watch create update patch delete deletecollection]
  volumesnapshotcontents.snapshot.storage.k8s.io  []                 []              [get list watch create update patch delete deletecollection]
  events                                          []                 []              [get list watch]
  persistentvolumeclaims                          []                 []              [get list watch]
  pods                                            []                 []              [get list watch]
  volumesnapshots.snapshot.storage.k8s.io         []                 []              [get list watch]


Name:         sudoer
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                       Non-Resource URLs  Resource Names    Verbs
  ---------                       -----------------  --------------    -----
  groups                          []                 [system:masters]  [impersonate]
  systemgroups                    []                 [system:masters]  [impersonate]
  systemusers                     []                 [system:admin]    [impersonate]
  users                           []                 [system:admin]    [impersonate]
  groups.user.openshift.io        []                 [system:masters]  [impersonate]
  systemgroups.user.openshift.io  []                 [system:masters]  [impersonate]
  systemusers.user.openshift.io   []                 [system:admin]    [impersonate]
  users.user.openshift.io         []                 [system:admin]    [impersonate]


Name:         system:aggregate-to-admin
Labels:       kubernetes.io/bootstrapping=rbac-defaults
              rbac.authorization.k8s.io/aggregate-to-admin=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  rolebindings.rbac.authorization.k8s.io          []                 []              [create delete deletecollection get list patch update watch]
  roles.rbac.authorization.k8s.io                 []                 []              [create delete deletecollection get list patch update watch]
  localsubjectaccessreviews.authorization.k8s.io  []                 []              [create]


Name:         system:aggregate-to-edit
Labels:       kubernetes.io/bootstrapping=rbac-defaults
              rbac.authorization.k8s.io/aggregate-to-edit=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                Non-Resource URLs  Resource Names  Verbs
  ---------                                -----------------  --------------  -----
  configmaps                               []                 []              [create delete deletecollection patch update]
  endpoints                                []                 []              [create delete deletecollection patch update]
  persistentvolumeclaims                   []                 []              [create delete deletecollection patch update]
  pods                                     []                 []              [create delete deletecollection patch update]
  replicationcontrollers/scale             []                 []              [create delete deletecollection patch update]
  replicationcontrollers                   []                 []              [create delete deletecollection patch update]
  services                                 []                 []              [create delete deletecollection patch update]
  daemonsets.apps                          []                 []              [create delete deletecollection patch update]
  deployments.apps/rollback                []                 []              [create delete deletecollection patch update]
  deployments.apps/scale                   []                 []              [create delete deletecollection patch update]
  deployments.apps                         []                 []              [create delete deletecollection patch update]
  replicasets.apps/scale                   []                 []              [create delete deletecollection patch update]
  replicasets.apps                         []                 []              [create delete deletecollection patch update]
  statefulsets.apps/scale                  []                 []              [create delete deletecollection patch update]
  statefulsets.apps                        []                 []              [create delete deletecollection patch update]
  horizontalpodautoscalers.autoscaling     []                 []              [create delete deletecollection patch update]
  cronjobs.batch                           []                 []              [create delete deletecollection patch update]
  jobs.batch                               []                 []              [create delete deletecollection patch update]
  daemonsets.extensions                    []                 []              [create delete deletecollection patch update]
  deployments.extensions/rollback          []                 []              [create delete deletecollection patch update]
  deployments.extensions/scale             []                 []              [create delete deletecollection patch update]
  deployments.extensions                   []                 []              [create delete deletecollection patch update]
  ingresses.extensions                     []                 []              [create delete deletecollection patch update]
  networkpolicies.extensions               []                 []              [create delete deletecollection patch update]
  replicasets.extensions/scale             []                 []              [create delete deletecollection patch update]
  replicasets.extensions                   []                 []              [create delete deletecollection patch update]
  replicationcontrollers.extensions/scale  []                 []              [create delete deletecollection patch update]
  ingresses.networking.k8s.io              []                 []              [create delete deletecollection patch update]
  networkpolicies.networking.k8s.io        []                 []              [create delete deletecollection patch update]
  poddisruptionbudgets.policy              []                 []              [create delete deletecollection patch update]
  pods/attach                              []                 []              [get list watch create delete deletecollection patch update]
  pods/exec                                []                 []              [get list watch create delete deletecollection patch update]
  pods/portforward                         []                 []              [get list watch create delete deletecollection patch update]
  pods/proxy                               []                 []              [get list watch create delete deletecollection patch update]
  secrets                                  []                 []              [get list watch create delete deletecollection patch update]
  services/proxy                           []                 []              [get list watch create delete deletecollection patch update]
  serviceaccounts                          []                 []              [impersonate create delete deletecollection patch update]


Name:         system:aggregate-to-view
Labels:       kubernetes.io/bootstrapping=rbac-defaults
              rbac.authorization.k8s.io/aggregate-to-view=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                    Non-Resource URLs  Resource Names  Verbs
  ---------                                    -----------------  --------------  -----
  bindings                                     []                 []              [get list watch]
  configmaps                                   []                 []              [get list watch]
  endpoints                                    []                 []              [get list watch]
  events                                       []                 []              [get list watch]
  limitranges                                  []                 []              [get list watch]
  namespaces/status                            []                 []              [get list watch]
  namespaces                                   []                 []              [get list watch]
  persistentvolumeclaims/status                []                 []              [get list watch]
  persistentvolumeclaims                       []                 []              [get list watch]
  pods/log                                     []                 []              [get list watch]
  pods/status                                  []                 []              [get list watch]
  pods                                         []                 []              [get list watch]
  replicationcontrollers/scale                 []                 []              [get list watch]
  replicationcontrollers/status                []                 []              [get list watch]
  replicationcontrollers                       []                 []              [get list watch]
  resourcequotas/status                        []                 []              [get list watch]
  resourcequotas                               []                 []              [get list watch]
  serviceaccounts                              []                 []              [get list watch]
  services/status                              []                 []              [get list watch]
  services                                     []                 []              [get list watch]
  controllerrevisions.apps                     []                 []              [get list watch]
  daemonsets.apps/status                       []                 []              [get list watch]
  daemonsets.apps                              []                 []              [get list watch]
  deployments.apps/scale                       []                 []              [get list watch]
  deployments.apps/status                      []                 []              [get list watch]
  deployments.apps                             []                 []              [get list watch]
  replicasets.apps/scale                       []                 []              [get list watch]
  replicasets.apps/status                      []                 []              [get list watch]
  replicasets.apps                             []                 []              [get list watch]
  statefulsets.apps/scale                      []                 []              [get list watch]
  statefulsets.apps/status                     []                 []              [get list watch]
  statefulsets.apps                            []                 []              [get list watch]
  horizontalpodautoscalers.autoscaling/status  []                 []              [get list watch]
  horizontalpodautoscalers.autoscaling         []                 []              [get list watch]
  cronjobs.batch/status                        []                 []              [get list watch]
  cronjobs.batch                               []                 []              [get list watch]
  jobs.batch/status                            []                 []              [get list watch]
  jobs.batch                                   []                 []              [get list watch]
  daemonsets.extensions/status                 []                 []              [get list watch]
  daemonsets.extensions                        []                 []              [get list watch]
  deployments.extensions/scale                 []                 []              [get list watch]
  deployments.extensions/status                []                 []              [get list watch]
  deployments.extensions                       []                 []              [get list watch]
  ingresses.extensions/status                  []                 []              [get list watch]
  ingresses.extensions                         []                 []              [get list watch]
  networkpolicies.extensions                   []                 []              [get list watch]
  replicasets.extensions/scale                 []                 []              [get list watch]
  replicasets.extensions/status                []                 []              [get list watch]
  replicasets.extensions                       []                 []              [get list watch]
  replicationcontrollers.extensions/scale      []                 []              [get list watch]
  ingresses.networking.k8s.io/status           []                 []              [get list watch]
  ingresses.networking.k8s.io                  []                 []              [get list watch]
  networkpolicies.networking.k8s.io            []                 []              [get list watch]
  poddisruptionbudgets.policy/status           []                 []              [get list watch]
  poddisruptionbudgets.policy                  []                 []              [get list watch]


Name:         system:aggregated-metrics-reader
Labels:       rbac.authorization.k8s.io/aggregate-to-admin=true
              rbac.authorization.k8s.io/aggregate-to-cluster-reader=true
              rbac.authorization.k8s.io/aggregate-to-edit=true
              rbac.authorization.k8s.io/aggregate-to-view=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  nodes.metrics.k8s.io  []                 []              [get list watch]
  pods.metrics.k8s.io   []                 []              [get list watch]


Name:         system:auth-delegator
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  tokenreviews.authentication.k8s.io         []                 []              [create]
  subjectaccessreviews.authorization.k8s.io  []                 []              [create]


Name:         system:basic-user
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                      Non-Resource URLs  Resource Names  Verbs
  ---------                                      -----------------  --------------  -----
  selfsubjectaccessreviews.authorization.k8s.io  []                 []              [create]
  selfsubjectrulesreviews.authorization.k8s.io   []                 []              [create]


Name:         system:build-strategy-custom
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                         Non-Resource URLs  Resource Names  Verbs
  ---------                         -----------------  --------------  -----
  builds/custom                     []                 []              [create]
  builds.build.openshift.io/custom  []                 []              [create]


Name:         system:build-strategy-docker
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  builds/docker                              []                 []              [create]
  builds/optimizeddocker                     []                 []              [create]
  builds.build.openshift.io/docker           []                 []              [create]
  builds.build.openshift.io/optimizeddocker  []                 []              [create]


Name:         system:build-strategy-jenkinspipeline
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  builds/jenkinspipeline                     []                 []              [create]
  builds.build.openshift.io/jenkinspipeline  []                 []              [create]


Name:         system:build-strategy-source
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                         Non-Resource URLs  Resource Names  Verbs
  ---------                         -----------------  --------------  -----
  builds/source                     []                 []              [create]
  builds.build.openshift.io/source  []                 []              [create]


Name:         system:certificates.k8s.io:certificatesigningrequests:nodeclient
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                                  -----------------  --------------  -----
  certificatesigningrequests.certificates.k8s.io/nodeclient  []                 []              [create]


Name:         system:certificates.k8s.io:certificatesigningrequests:selfnodeclient
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                                      Non-Resource URLs  Resource Names  Verbs
  ---------                                                      -----------------  --------------  -----
  certificatesigningrequests.certificates.k8s.io/selfnodeclient  []                 []              [create]


Name:         system:certificates.k8s.io:kube-apiserver-client-approver
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                    Non-Resource URLs  Resource Names                         Verbs
  ---------                    -----------------  --------------                         -----
  signers.certificates.k8s.io  []                 [kubernetes.io/kube-apiserver-client]  [approve]


Name:         system:certificates.k8s.io:kube-apiserver-client-kubelet-approver
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                    Non-Resource URLs  Resource Names                                 Verbs
  ---------                    -----------------  --------------                                 -----
  signers.certificates.k8s.io  []                 [kubernetes.io/kube-apiserver-client-kubelet]  [approve]


Name:         system:certificates.k8s.io:kubelet-serving-approver
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                    Non-Resource URLs  Resource Names                   Verbs
  ---------                    -----------------  --------------                   -----
  signers.certificates.k8s.io  []                 [kubernetes.io/kubelet-serving]  [approve]


Name:         system:certificates.k8s.io:legacy-unknown-approver
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                    Non-Resource URLs  Resource Names                  Verbs
  ---------                    -----------------  --------------                  -----
  signers.certificates.k8s.io  []                 [kubernetes.io/legacy-unknown]  [approve]


Name:         system:controller:attachdetach-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                         Non-Resource URLs  Resource Names  Verbs
  ---------                         -----------------  --------------  -----
  volumeattachments.storage.k8s.io  []                 []              [create delete get list watch]
  events                            []                 []              [create patch update]
  events.events.k8s.io              []                 []              [create patch update]
  nodes                             []                 []              [get list watch]
  csidrivers.storage.k8s.io         []                 []              [get list watch]
  csinodes.storage.k8s.io           []                 []              [get list watch]
  persistentvolumeclaims            []                 []              [list watch]
  persistentvolumes                 []                 []              [list watch]
  pods                              []                 []              [list watch]
  nodes/status                      []                 []              [patch update]


Name:         system:controller:certificate-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                                Non-Resource URLs  Resource Names                                 Verbs
  ---------                                                -----------------  --------------                                 -----
  signers.certificates.k8s.io                              []                 [kubernetes.io/kube-apiserver-client-kubelet]  [approve sign]
  events                                                   []                 []                                             [create patch update]
  events.events.k8s.io                                     []                 []                                             [create patch update]
  subjectaccessreviews.authorization.k8s.io                []                 []                                             [create]
  certificatesigningrequests.certificates.k8s.io           []                 []                                             [delete get list watch]
  signers.certificates.k8s.io                              []                 [kubernetes.io/kube-apiserver-client]          [sign]
  signers.certificates.k8s.io                              []                 [kubernetes.io/kubelet-serving]                [sign]
  signers.certificates.k8s.io                              []                 [kubernetes.io/legacy-unknown]                 [sign]
  certificatesigningrequests.certificates.k8s.io/approval  []                 []                                             [update]
  certificatesigningrequests.certificates.k8s.io/status    []                 []                                             [update]


Name:         system:controller:clusterrole-aggregation-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                               Non-Resource URLs  Resource Names  Verbs
  ---------                               -----------------  --------------  -----
  clusterroles.rbac.authorization.k8s.io  []                 []              [escalate get list patch update watch]


Name:         system:controller:cronjob-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                  Non-Resource URLs  Resource Names  Verbs
  ---------                  -----------------  --------------  -----
  jobs.batch                 []                 []              [create delete get list patch update watch]
  events                     []                 []              [create patch update]
  events.events.k8s.io       []                 []              [create patch update]
  pods                       []                 []              [delete list]
  cronjobs.batch             []                 []              [get list update watch]
  cronjobs.batch/finalizers  []                 []              [update]
  cronjobs.batch/status      []                 []              [update]


Name:         system:controller:daemon-set-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                         Non-Resource URLs  Resource Names  Verbs
  ---------                         -----------------  --------------  -----
  controllerrevisions.apps          []                 []              [create delete get list patch update watch]
  pods                              []                 []              [create delete list patch watch]
  events                            []                 []              [create patch update]
  events.events.k8s.io              []                 []              [create patch update]
  pods/binding                      []                 []              [create]
  daemonsets.apps                   []                 []              [get list watch]
  daemonsets.extensions             []                 []              [get list watch]
  nodes                             []                 []              [list watch]
  daemonsets.apps/finalizers        []                 []              [update]
  daemonsets.apps/status            []                 []              [update]
  daemonsets.extensions/finalizers  []                 []              [update]
  daemonsets.extensions/status      []                 []              [update]


Name:         system:controller:deployment-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                          Non-Resource URLs  Resource Names  Verbs
  ---------                          -----------------  --------------  -----
  replicasets.apps                   []                 []              [create delete get list patch update watch]
  replicasets.extensions             []                 []              [create delete get list patch update watch]
  events                             []                 []              [create patch update]
  events.events.k8s.io               []                 []              [create patch update]
  pods                               []                 []              [get list update watch]
  deployments.apps                   []                 []              [get list update watch]
  deployments.extensions             []                 []              [get list update watch]
  deployments.apps/finalizers        []                 []              [update]
  deployments.apps/status            []                 []              [update]
  deployments.extensions/finalizers  []                 []              [update]
  deployments.extensions/status      []                 []              [update]


Name:         system:controller:disruption-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                           Non-Resource URLs  Resource Names  Verbs
  ---------                           -----------------  --------------  -----
  events                              []                 []              [create patch update]
  events.events.k8s.io                []                 []              [create patch update]
  replicationcontrollers              []                 []              [get list watch]
  deployments.apps                    []                 []              [get list watch]
  replicasets.apps                    []                 []              [get list watch]
  statefulsets.apps                   []                 []              [get list watch]
  deployments.extensions              []                 []              [get list watch]
  replicasets.extensions              []                 []              [get list watch]
  poddisruptionbudgets.policy         []                 []              [get list watch]
  *.*/scale                           []                 []              [get]
  poddisruptionbudgets.policy/status  []                 []              [update]


Name:         system:controller:endpoint-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  endpoints             []                 []              [create delete get list update]
  events                []                 []              [create patch update]
  events.events.k8s.io  []                 []              [create patch update]
  endpoints/restricted  []                 []              [create]
  pods                  []                 []              [get list watch]
  services              []                 []              [get list watch]


Name:         system:controller:endpointslice-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                        Non-Resource URLs  Resource Names  Verbs
  ---------                        -----------------  --------------  -----
  endpointslices.discovery.k8s.io  []                 []              [create delete get list update]
  events                           []                 []              [create patch update]
  events.events.k8s.io             []                 []              [create patch update]
  nodes                            []                 []              [get list watch]
  pods                             []                 []              [get list watch]
  services                         []                 []              [get list watch]
  services/finalizers              []                 []              [update]


Name:         system:controller:endpointslicemirroring-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                        Non-Resource URLs  Resource Names  Verbs
  ---------                        -----------------  --------------  -----
  endpointslices.discovery.k8s.io  []                 []              [create delete get list update]
  events                           []                 []              [create patch update]
  events.events.k8s.io             []                 []              [create patch update]
  endpoints                        []                 []              [get list watch]
  services                         []                 []              [get list watch]
  endpoints/finalizers             []                 []              [update]
  services/finalizers              []                 []              [update]


Name:         system:controller:expand-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                      Non-Resource URLs  Resource Names  Verbs
  ---------                      -----------------  --------------  -----
  events                         []                 []              [create patch update]
  events.events.k8s.io           []                 []              [create patch update]
  persistentvolumes              []                 []              [get list patch update watch]
  persistentvolumeclaims         []                 []              [get list watch]
  storageclasses.storage.k8s.io  []                 []              [get list watch]
  endpoints                      []                 []              [get]
  secrets                        []                 []              [get]
  services                       []                 []              [get]
  persistentvolumeclaims/status  []                 []              [patch update]


Name:         system:controller:generic-garbage-collector
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  events                []                 []              [create patch update]
  events.events.k8s.io  []                 []              [create patch update]
  *.*                   []                 []              [delete get list patch update watch]


Name:         system:controller:horizontal-pod-autoscaler
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                    Non-Resource URLs  Resource Names     Verbs
  ---------                                    -----------------  --------------     -----
  events                                       []                 []                 [create patch update]
  events.events.k8s.io                         []                 []                 [create patch update]
  horizontalpodautoscalers.autoscaling         []                 []                 [get list watch]
  *.custom.metrics.k8s.io                      []                 []                 [get list]
  *.*/scale                                    []                 []                 [get update]
  services/proxy                               []                 [http:heapster:]   [get]
  services/proxy                               []                 [https:heapster:]  [get]
  pods                                         []                 []                 [list]
  pods.metrics.k8s.io                          []                 []                 [list]
  horizontalpodautoscalers.autoscaling/status  []                 []                 [update]


Name:         system:controller:job-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources              Non-Resource URLs  Resource Names  Verbs
  ---------              -----------------  --------------  -----
  pods                   []                 []              [create delete list patch watch]
  events                 []                 []              [create patch update]
  events.events.k8s.io   []                 []              [create patch update]
  jobs.batch             []                 []              [get list update watch]
  jobs.batch/finalizers  []                 []              [update]
  jobs.batch/status      []                 []              [update]


Name:         system:controller:namespace-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources            Non-Resource URLs  Resource Names  Verbs
  ---------            -----------------  --------------  -----
  *.*                  []                 []              [delete deletecollection get list]
  namespaces           []                 []              [delete get list watch]
  namespaces/finalize  []                 []              [update]
  namespaces/status    []                 []              [update]


Name:         system:controller:node-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  events                []                 []              [create patch update]
  events.events.k8s.io  []                 []              [create patch update]
  nodes                 []                 []              [delete get list patch update]
  pods                  []                 []              [delete list]
  nodes/status          []                 []              [patch update]
  pods/status           []                 []              [update]


Name:         system:controller:operator-lifecycle-manager
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  *.*        []                 []              [*]
             [*]                []              [*]


Name:         system:controller:persistent-volume-binder
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                      Non-Resource URLs  Resource Names  Verbs
  ---------                      -----------------  --------------  -----
  persistentvolumes              []                 []              [create delete get list update watch]
  pods                           []                 []              [create delete get list watch]
  endpoints                      []                 []              [create delete get update]
  services                       []                 []              [create delete get]
  events.events.k8s.io           []                 []              [create patch update]
  persistentvolumeclaims         []                 []              [get list update watch]
  storageclasses.storage.k8s.io  []                 []              [get list watch]
  nodes                          []                 []              [get list]
  secrets                        []                 []              [get]
  persistentvolumeclaims/status  []                 []              [update]
  persistentvolumes/status       []                 []              [update]
  events                         []                 []              [watch create patch update]


Name:         system:controller:pod-garbage-collector
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  pods       []                 []              [delete list watch]
  nodes      []                 []              [get list]


Name:         system:controller:pv-protection-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  events                []                 []              [create patch update]
  events.events.k8s.io  []                 []              [create patch update]
  persistentvolumes     []                 []              [get list update watch]


Name:         system:controller:pvc-protection-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources               Non-Resource URLs  Resource Names  Verbs
  ---------               -----------------  --------------  -----
  events                  []                 []              [create patch update]
  events.events.k8s.io    []                 []              [create patch update]
  persistentvolumeclaims  []                 []              [get list update watch]
  pods                    []                 []              [get list watch]


Name:         system:controller:replicaset-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                          Non-Resource URLs  Resource Names  Verbs
  ---------                          -----------------  --------------  -----
  pods                               []                 []              [create delete list patch watch]
  events                             []                 []              [create patch update]
  events.events.k8s.io               []                 []              [create patch update]
  replicasets.apps                   []                 []              [get list update watch]
  replicasets.extensions             []                 []              [get list update watch]
  replicasets.apps/finalizers        []                 []              [update]
  replicasets.apps/status            []                 []              [update]
  replicasets.extensions/finalizers  []                 []              [update]
  replicasets.extensions/status      []                 []              [update]


Name:         system:controller:replication-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                          Non-Resource URLs  Resource Names  Verbs
  ---------                          -----------------  --------------  -----
  pods                               []                 []              [create delete list patch watch]
  events                             []                 []              [create patch update]
  events.events.k8s.io               []                 []              [create patch update]
  replicationcontrollers             []                 []              [get list update watch]
  replicationcontrollers/finalizers  []                 []              [update]
  replicationcontrollers/status      []                 []              [update]


Name:         system:controller:resourcequota-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources              Non-Resource URLs  Resource Names  Verbs
  ---------              -----------------  --------------  -----
  events                 []                 []              [create patch update]
  events.events.k8s.io   []                 []              [create patch update]
  *.*                    []                 []              [list watch]
  resourcequotas/status  []                 []              [update]


Name:         system:controller:route-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  events                []                 []              [create patch update]
  events.events.k8s.io  []                 []              [create patch update]
  nodes                 []                 []              [list watch]
  nodes/status          []                 []              [patch]


Name:         system:controller:service-account-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  events                []                 []              [create patch update]
  events.events.k8s.io  []                 []              [create patch update]
  serviceaccounts       []                 []              [create]


Name:         system:controller:service-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  events                []                 []              [create patch update]
  events.events.k8s.io  []                 []              [create patch update]
  services              []                 []              [get list watch]
  nodes                 []                 []              [list watch]
  services/status       []                 []              [patch update]


Name:         system:controller:statefulset-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                     Non-Resource URLs  Resource Names  Verbs
  ---------                     -----------------  --------------  -----
  controllerrevisions.apps      []                 []              [create delete get list patch update watch]
  persistentvolumeclaims        []                 []              [create get]
  events                        []                 []              [create patch update]
  events.events.k8s.io          []                 []              [create patch update]
  statefulsets.apps             []                 []              [get list watch]
  pods                          []                 []              [list watch create delete get patch update]
  statefulsets.apps/finalizers  []                 []              [update]
  statefulsets.apps/status      []                 []              [update]


Name:         system:controller:ttl-controller
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  events                []                 []              [create patch update]
  events.events.k8s.io  []                 []              [create patch update]
  nodes                 []                 []              [list patch update watch]


Name:         system:deployer
Labels:       &lt;none&gt;
Annotations:  openshift.io/description: Grants the right to deploy within a project.  Used primarily with service accounts for automated deployments.
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                           Non-Resource URLs  Resource Names  Verbs
  ---------                           -----------------  --------------  -----
  pods                                []                 []              [create get list watch]
  events                              []                 []              [create list]
  imagestreamtags                     []                 []              [create update]
  imagetags                           []                 []              [create update]
  imagestreamtags.image.openshift.io  []                 []              [create update]
  imagetags.image.openshift.io        []                 []              [create update]
  replicationcontrollers              []                 []              [delete get list update watch]
  replicationcontrollers/scale        []                 []              [get update]
  pods/log                            []                 []              [get]


Name:         system:discovery
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
             [/api/*]           []              [get]
             [/api]             []              [get]
             [/apis/*]          []              [get]
             [/apis]            []              [get]
             [/healthz]         []              [get]
             [/livez]           []              [get]
             [/openapi/*]       []              [get]
             [/openapi]         []              [get]
             [/readyz]          []              [get]
             [/version/]        []              [get]
             [/version]         []              [get]


Name:         system:heapster
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources               Non-Resource URLs  Resource Names  Verbs
  ---------               -----------------  --------------  -----
  events                  []                 []              [get list watch]
  namespaces              []                 []              [get list watch]
  nodes                   []                 []              [get list watch]
  pods                    []                 []              [get list watch]
  deployments.extensions  []                 []              [get list watch]


Name:         system:image-auditor
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                  Non-Resource URLs  Resource Names  Verbs
  ---------                  -----------------  --------------  -----
  images                     []                 []              [get list patch update watch]
  images.image.openshift.io  []                 []              [get list patch update watch]


Name:         system:image-builder
Labels:       rbac.authorization.k8s.io/aggregate-to-admin=true
              rbac.authorization.k8s.io/aggregate-to-edit=true
Annotations:  openshift.io/description:
                Grants the right to build, push and pull images from within a project.  Used primarily with service accounts for builds.
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                               Non-Resource URLs  Resource Names  Verbs
  ---------                               -----------------  --------------  -----
  imagestreams                            []                 []              [create]
  imagestreams.image.openshift.io         []                 []              [create]
  imagestreams/layers                     []                 []              [get update]
  imagestreams.image.openshift.io/layers  []                 []              [get update]
  builds                                  []                 []              [get]
  builds.build.openshift.io               []                 []              [get]
  builds/details                          []                 []              [update]
  builds.build.openshift.io/details       []                 []              [update]


Name:         system:image-pruner
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                               Non-Resource URLs  Resource Names  Verbs
  ---------                               -----------------  --------------  -----
  images                                  []                 []              [delete get list watch]
  images.image.openshift.io               []                 []              [delete get list watch]
  imagestreams                            []                 []              [get list watch]
  imagestreams.image.openshift.io         []                 []              [get list watch]
  buildconfigs                            []                 []              [get list]
  builds                                  []                 []              [get list]
  deploymentconfigs                       []                 []              [get list]
  pods                                    []                 []              [get list]
  replicationcontrollers                  []                 []              [get list]
  deploymentconfigs.apps.openshift.io     []                 []              [get list]
  daemonsets.apps                         []                 []              [get list]
  deployments.apps                        []                 []              [get list]
  replicasets.apps                        []                 []              [get list]
  buildconfigs.build.openshift.io         []                 []              [get list]
  builds.build.openshift.io               []                 []              [get list]
  daemonsets.extensions                   []                 []              [get list]
  deployments.extensions                  []                 []              [get list]
  replicasets.extensions                  []                 []              [get list]
  limitranges                             []                 []              [list]
  imagestreams/status                     []                 []              [update]
  imagestreams.image.openshift.io/status  []                 []              [update]


Name:         system:image-puller
Labels:       &lt;none&gt;
Annotations:  openshift.io/description: Grants the right to pull images from within a project.
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                               Non-Resource URLs  Resource Names  Verbs
  ---------                               -----------------  --------------  -----
  imagestreams/layers                     []                 []              [get]
  imagestreams.image.openshift.io/layers  []                 []              [get]


Name:         system:image-pusher
Labels:       &lt;none&gt;
Annotations:  openshift.io/description: Grants the right to push and pull images from within a project.
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                               Non-Resource URLs  Resource Names  Verbs
  ---------                               -----------------  --------------  -----
  imagestreams/layers                     []                 []              [get update]
  imagestreams.image.openshift.io/layers  []                 []              [get update]


Name:         system:image-signer
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                               Non-Resource URLs  Resource Names  Verbs
  ---------                               -----------------  --------------  -----
  imagesignatures                         []                 []              [create delete]
  imagesignatures.image.openshift.io      []                 []              [create delete]
  images                                  []                 []              [get]
  imagestreams/layers                     []                 []              [get]
  images.image.openshift.io               []                 []              [get]
  imagestreams.image.openshift.io/layers  []                 []              [get]


Name:         system:kube-aggregator
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  endpoints  []                 []              [get list watch]
  services   []                 []              [get list watch]


Name:         system:kube-controller-manager
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names             Verbs
  ---------                                  -----------------  --------------             -----
  secrets                                    []                 []                         [create delete get update]
  serviceaccounts                            []                 []                         [create get update]
  events                                     []                 []                         [create patch update]
  events.events.k8s.io                       []                 []                         [create patch update]
  endpoints                                  []                 []                         [create]
  serviceaccounts/token                      []                 []                         [create]
  tokenreviews.authentication.k8s.io         []                 []                         [create]
  subjectaccessreviews.authorization.k8s.io  []                 []                         [create]
  leases.coordination.k8s.io                 []                 []                         [create]
  endpoints                                  []                 [kube-controller-manager]  [get update]
  leases.coordination.k8s.io                 []                 [kube-controller-manager]  [get update]
  configmaps                                 []                 []                         [get]
  namespaces                                 []                 []                         [get]
  *.*                                        []                 []                         [list watch]


Name:         system:kube-dns
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  endpoints  []                 []              [list watch]
  services   []                 []              [list watch]


Name:         system:kube-scheduler
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names    Verbs
  ---------                                  -----------------  --------------    -----
  events                                     []                 []                [create patch update]
  events.events.k8s.io                       []                 []                [create patch update]
  bindings                                   []                 []                [create]
  endpoints                                  []                 []                [create]
  pods/binding                               []                 []                [create]
  tokenreviews.authentication.k8s.io         []                 []                [create]
  subjectaccessreviews.authorization.k8s.io  []                 []                [create]
  leases.coordination.k8s.io                 []                 []                [create]
  pods                                       []                 []                [delete get list watch]
  nodes                                      []                 []                [get list watch]
  persistentvolumeclaims                     []                 []                [get list watch]
  persistentvolumes                          []                 []                [get list watch]
  replicationcontrollers                     []                 []                [get list watch]
  services                                   []                 []                [get list watch]
  replicasets.apps                           []                 []                [get list watch]
  statefulsets.apps                          []                 []                [get list watch]
  replicasets.extensions                     []                 []                [get list watch]
  poddisruptionbudgets.policy                []                 []                [get list watch]
  csinodes.storage.k8s.io                    []                 []                [get list watch]
  endpoints                                  []                 [kube-scheduler]  [get update]
  leases.coordination.k8s.io                 []                 [kube-scheduler]  [get update]
  pods/status                                []                 []                [patch update]


Name:         system:kubelet-api-admin
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources      Non-Resource URLs  Resource Names  Verbs
  ---------      -----------------  --------------  -----
  nodes/log      []                 []              [*]
  nodes/metrics  []                 []              [*]
  nodes/proxy    []                 []              [*]
  nodes/spec     []                 []              [*]
  nodes/stats    []                 []              [*]
  nodes          []                 []              [get list watch proxy]


Name:         system:master
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  *.*        []                 []              [*]
             [*]                []              [*]


Name:         system:node
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  leases.coordination.k8s.io                      []                 []              [create delete get patch update]
  csinodes.storage.k8s.io                         []                 []              [create delete get patch update]
  nodes                                           []                 []              [create get list watch patch update]
  certificatesigningrequests.certificates.k8s.io  []                 []              [create get list watch]
  events                                          []                 []              [create patch update]
  pods/eviction                                   []                 []              [create]
  serviceaccounts/token                           []                 []              [create]
  tokenreviews.authentication.k8s.io              []                 []              [create]
  localsubjectaccessreviews.authorization.k8s.io  []                 []              [create]
  subjectaccessreviews.authorization.k8s.io       []                 []              [create]
  pods                                            []                 []              [get list watch create delete]
  configmaps                                      []                 []              [get list watch]
  secrets                                         []                 []              [get list watch]
  services                                        []                 []              [get list watch]
  runtimeclasses.node.k8s.io                      []                 []              [get list watch]
  csidrivers.storage.k8s.io                       []                 []              [get list watch]
  persistentvolumeclaims/status                   []                 []              [get patch update]
  endpoints                                       []                 []              [get]
  persistentvolumeclaims                          []                 []              [get]
  persistentvolumes                               []                 []              [get]
  volumeattachments.storage.k8s.io                []                 []              [get]
  nodes/status                                    []                 []              [patch update]
  pods/status                                     []                 []              [patch update]


Name:         system:node-admin
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources      Non-Resource URLs  Resource Names  Verbs
  ---------      -----------------  --------------  -----
  nodes/log      []                 []              [*]
  nodes/metrics  []                 []              [*]
  nodes/proxy    []                 []              [*]
  nodes/spec     []                 []              [*]
  nodes/stats    []                 []              [*]
  nodes          []                 []              [get list watch proxy]


Name:         system:node-bootstrapper
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  certificatesigningrequests.certificates.k8s.io  []                 []              [create get list watch]


Name:         system:node-problem-detector
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  events                []                 []              [create patch update]
  events.events.k8s.io  []                 []              [create patch update]
  nodes                 []                 []              [get]
  nodes/status          []                 []              [patch]


Name:         system:node-proxier
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                        Non-Resource URLs  Resource Names  Verbs
  ---------                        -----------------  --------------  -----
  events                           []                 []              [create patch update]
  events.events.k8s.io             []                 []              [create patch update]
  nodes                            []                 []              [get list watch]
  endpoints                        []                 []              [list watch]
  services                         []                 []              [list watch]
  endpointslices.discovery.k8s.io  []                 []              [list watch]


Name:         system:node-reader
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources      Non-Resource URLs  Resource Names  Verbs
  ---------      -----------------  --------------  -----
  nodes/stats    []                 []              [create get]
  nodes          []                 []              [get list watch]
  nodes/metrics  []                 []              [get]
  nodes/spec     []                 []              [get]


Name:         system:oauth-token-deleter
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                Non-Resource URLs  Resource Names  Verbs
  ---------                                -----------------  --------------  -----
  oauthaccesstokens                        []                 []              [delete]
  oauthauthorizetokens                     []                 []              [delete]
  oauthaccesstokens.oauth.openshift.io     []                 []              [delete]
  oauthauthorizetokens.oauth.openshift.io  []                 []              [delete]


Name:         system:openshift:aggregate-snapshots-to-admin
Labels:       addonmanager.kubernetes.io/mode=Reconcile
              kubernetes.io/cluster-service=true
              rbac.authorization.k8s.io/aggregate-to-admin=true
              rbac.authorization.k8s.io/aggregate-to-edit=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                Non-Resource URLs  Resource Names  Verbs
  ---------                                -----------------  --------------  -----
  volumesnapshots.snapshot.storage.k8s.io  []                 []              [get list watch create update patch delete deletecollection]


Name:         system:openshift:aggregate-snapshots-to-basic-user
Labels:       addonmanager.kubernetes.io/mode=Reconcile
              authorization.openshift.io/aggregate-to-basic-user=true
              kubernetes.io/cluster-service=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                      Non-Resource URLs  Resource Names  Verbs
  ---------                                      -----------------  --------------  -----
  volumesnapshotclasses.snapshot.storage.k8s.io  []                 []              [get list watch]


Name:         system:openshift:aggregate-snapshots-to-storage-admin
Labels:       addonmanager.kubernetes.io/mode=Reconcile
              kubernetes.io/cluster-service=true
              storage.openshift.io/aggregate-to-storage-admin=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  volumesnapshotclasses.snapshot.storage.k8s.io   []                 []              [get list watch create update patch delete deletecollection]
  volumesnapshotcontents.snapshot.storage.k8s.io  []                 []              [get list watch create update patch delete deletecollection]
  volumesnapshots.snapshot.storage.k8s.io         []                 []              [get list watch]


Name:         system:openshift:aggregate-snapshots-to-view
Labels:       addonmanager.kubernetes.io/mode=Reconcile
              kubernetes.io/cluster-service=true
              rbac.authorization.k8s.io/aggregate-to-view=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                Non-Resource URLs  Resource Names  Verbs
  ---------                                -----------------  --------------  -----
  volumesnapshots.snapshot.storage.k8s.io  []                 []              [get list watch]


Name:         system:openshift:aggregate-to-admin
Labels:       rbac.authorization.k8s.io/aggregate-to-admin=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                                  -----------------  --------------  -----
  jenkins.build.openshift.io                                 []                 []              [admin edit view]
  buildconfigs/webhooks                                      []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs                                               []                 []              [create delete deletecollection get list patch update watch]
  buildlogs                                                  []                 []              [create delete deletecollection get list patch update watch]
  builds                                                     []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs/scale                                    []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs                                          []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimages                                          []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings                                        []                 []              [create delete deletecollection get list patch update watch]
  imagestreams/secrets                                       []                 []              [create delete deletecollection get list patch update watch]
  imagestreams                                               []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags                                            []                 []              [create delete deletecollection get list patch update watch]
  imagetags                                                  []                 []              [create delete deletecollection get list patch update watch]
  processedtemplates                                         []                 []              [create delete deletecollection get list patch update watch]
  rolebindings                                               []                 []              [create delete deletecollection get list patch update watch]
  roles                                                      []                 []              [create delete deletecollection get list patch update watch]
  routes                                                     []                 []              [create delete deletecollection get list patch update watch]
  templateconfigs                                            []                 []              [create delete deletecollection get list patch update watch]
  templateinstances                                          []                 []              [create delete deletecollection get list patch update watch]
  templates                                                  []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs.apps.openshift.io/scale                  []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs.apps.openshift.io                        []                 []              [create delete deletecollection get list patch update watch]
  rolebindings.authorization.openshift.io                    []                 []              [create delete deletecollection get list patch update watch]
  roles.authorization.openshift.io                           []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs.build.openshift.io/webhooks                   []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs.build.openshift.io                            []                 []              [create delete deletecollection get list patch update watch]
  buildlogs.build.openshift.io                               []                 []              [create delete deletecollection get list patch update watch]
  builds.build.openshift.io                                  []                 []              [create delete deletecollection get list patch update watch]
  networkpolicies.extensions                                 []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimages.image.openshift.io                       []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings.image.openshift.io                     []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io/secrets                    []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io                            []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags.image.openshift.io                         []                 []              [create delete deletecollection get list patch update watch]
  imagetags.image.openshift.io                               []                 []              [create delete deletecollection get list patch update watch]
  networkpolicies.networking.k8s.io                          []                 []              [create delete deletecollection get list patch update watch]
  routes.route.openshift.io                                  []                 []              [create delete deletecollection get list patch update watch]
  processedtemplates.template.openshift.io                   []                 []              [create delete deletecollection get list patch update watch]
  templateconfigs.template.openshift.io                      []                 []              [create delete deletecollection get list patch update watch]
  templateinstances.template.openshift.io                    []                 []              [create delete deletecollection get list patch update watch]
  templates.template.openshift.io                            []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs/instantiate                                   []                 []              [create]
  buildconfigs/instantiatebinary                             []                 []              [create]
  builds/clone                                               []                 []              [create]
  deploymentconfigrollbacks                                  []                 []              [create]
  deploymentconfigs/instantiate                              []                 []              [create]
  deploymentconfigs/rollback                                 []                 []              [create]
  imagestreamimports                                         []                 []              [create]
  localresourceaccessreviews                                 []                 []              [create]
  localsubjectaccessreviews                                  []                 []              [create]
  podsecuritypolicyreviews                                   []                 []              [create]
  podsecuritypolicyselfsubjectreviews                        []                 []              [create]
  podsecuritypolicysubjectreviews                            []                 []              [create]
  resourceaccessreviews                                      []                 []              [create]
  routes/custom-host                                         []                 []              [create]
  subjectaccessreviews                                       []                 []              [create]
  subjectrulesreviews                                        []                 []              [create]
  deploymentconfigrollbacks.apps.openshift.io                []                 []              [create]
  deploymentconfigs.apps.openshift.io/instantiate            []                 []              [create]
  deploymentconfigs.apps.openshift.io/rollback               []                 []              [create]
  localresourceaccessreviews.authorization.openshift.io      []                 []              [create]
  localsubjectaccessreviews.authorization.openshift.io       []                 []              [create]
  resourceaccessreviews.authorization.openshift.io           []                 []              [create]
  subjectaccessreviews.authorization.openshift.io            []                 []              [create]
  subjectrulesreviews.authorization.openshift.io             []                 []              [create]
  buildconfigs.build.openshift.io/instantiate                []                 []              [create]
  buildconfigs.build.openshift.io/instantiatebinary          []                 []              [create]
  builds.build.openshift.io/clone                            []                 []              [create]
  imagestreamimports.image.openshift.io                      []                 []              [create]
  routes.route.openshift.io/custom-host                      []                 []              [create]
  podsecuritypolicyreviews.security.openshift.io             []                 []              [create]
  podsecuritypolicyselfsubjectreviews.security.openshift.io  []                 []              [create]
  podsecuritypolicysubjectreviews.security.openshift.io      []                 []              [create]
  projects                                                   []                 []              [delete get patch update]
  projects.project.openshift.io                              []                 []              [delete get patch update]
  routes/status                                              []                 []              [get list watch update]
  routes.route.openshift.io/status                           []                 []              [get list watch update]
  appliedclusterresourcequotas                               []                 []              [get list watch]
  builds/log                                                 []                 []              [get list watch]
  deploymentconfigs/log                                      []                 []              [get list watch]
  deploymentconfigs/status                                   []                 []              [get list watch]
  imagestreams/status                                        []                 []              [get list watch]
  resourcequotausages                                        []                 []              [get list watch]
  rolebindingrestrictions                                    []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/log                    []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/status                 []                 []              [get list watch]
  rolebindingrestrictions.authorization.openshift.io         []                 []              [get list watch]
  builds.build.openshift.io/log                              []                 []              [get list watch]
  imagestreams.image.openshift.io/status                     []                 []              [get list watch]
  appliedclusterresourcequotas.quota.openshift.io            []                 []              [get list watch]
  imagestreams/layers                                        []                 []              [get update]
  imagestreams.image.openshift.io/layers                     []                 []              [get update]
  builds/details                                             []                 []              [update]
  builds.build.openshift.io/details                          []                 []              [update]


Name:         system:openshift:aggregate-to-basic-user
Labels:       authorization.openshift.io/aggregate-to-basic-user=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                           Non-Resource URLs  Resource Names  Verbs
  ---------                                           -----------------  --------------  -----
  selfsubjectrulesreviews                             []                 []              [create]
  selfsubjectaccessreviews.authorization.k8s.io       []                 []              [create]
  selfsubjectrulesreviews.authorization.openshift.io  []                 []              [create]
  clusterroles.rbac.authorization.k8s.io              []                 []              [get list watch]
  clusterroles                                        []                 []              [get list]
  clusterroles.authorization.openshift.io             []                 []              [get list]
  storageclasses.storage.k8s.io                       []                 []              [get list]
  users                                               []                 [~]             [get]
  users.user.openshift.io                             []                 [~]             [get]
  projects                                            []                 []              [list watch]
  projects.project.openshift.io                       []                 []              [list watch]
  projectrequests                                     []                 []              [list]
  projectrequests.project.openshift.io                []                 []              [list]


Name:         system:openshift:aggregate-to-cluster-reader
Labels:       rbac.authorization.k8s.io/aggregate-to-cluster-reader=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                                     -----------------  --------------  -----
  nodes/stats                                                   []                 []              [create get]
  localresourceaccessreviews                                    []                 []              [create]
  localsubjectaccessreviews                                     []                 []              [create]
  podsecuritypolicyreviews                                      []                 []              [create]
  podsecuritypolicyselfsubjectreviews                           []                 []              [create]
  podsecuritypolicysubjectreviews                               []                 []              [create]
  resourceaccessreviews                                         []                 []              [create]
  selfsubjectrulesreviews                                       []                 []              [create]
  subjectaccessreviews                                          []                 []              [create]
  subjectrulesreviews                                           []                 []              [create]
  tokenreviews.authentication.k8s.io                            []                 []              [create]
  localsubjectaccessreviews.authorization.k8s.io                []                 []              [create]
  selfsubjectaccessreviews.authorization.k8s.io                 []                 []              [create]
  selfsubjectrulesreviews.authorization.k8s.io                  []                 []              [create]
  subjectaccessreviews.authorization.k8s.io                     []                 []              [create]
  localresourceaccessreviews.authorization.openshift.io         []                 []              [create]
  localsubjectaccessreviews.authorization.openshift.io          []                 []              [create]
  resourceaccessreviews.authorization.openshift.io              []                 []              [create]
  selfsubjectrulesreviews.authorization.openshift.io            []                 []              [create]
  subjectaccessreviews.authorization.openshift.io               []                 []              [create]
  subjectrulesreviews.authorization.openshift.io                []                 []              [create]
  podsecuritypolicyreviews.security.openshift.io                []                 []              [create]
  podsecuritypolicyselfsubjectreviews.security.openshift.io     []                 []              [create]
  podsecuritypolicysubjectreviews.security.openshift.io         []                 []              [create]
  brokertemplateinstances                                       []                 []              [get list watch]
  builds/details                                                []                 []              [get list watch]
  clusternetworks                                               []                 []              [get list watch]
  clusterresourcequotas/status                                  []                 []              [get list watch]
  clusterresourcequotas                                         []                 []              [get list watch]
  clusterrolebindings                                           []                 []              [get list watch]
  clusterroles                                                  []                 []              [get list watch]
  componentstatuses                                             []                 []              [get list watch]
  egressnetworkpolicies                                         []                 []              [get list watch]
  groups                                                        []                 []              [get list watch]
  hostsubnets                                                   []                 []              [get list watch]
  identities                                                    []                 []              [get list watch]
  images                                                        []                 []              [get list watch]
  imagesignatures                                               []                 []              [get list watch]
  netnamespaces                                                 []                 []              [get list watch]
  nodes/status                                                  []                 []              [get list watch]
  nodes                                                         []                 []              [get list watch]
  oauthclientauthorizations                                     []                 []              [get list watch]
  persistentvolumeclaims/status                                 []                 []              [get list watch]
  persistentvolumes/status                                      []                 []              [get list watch]
  persistentvolumes                                             []                 []              [get list watch]
  pods/binding                                                  []                 []              [get list watch]
  pods/eviction                                                 []                 []              [get list watch]
  podtemplates                                                  []                 []              [get list watch]
  projectrequests                                               []                 []              [get list watch]
  rolebindingrestrictions                                       []                 []              [get list watch]
  rolebindings                                                  []                 []              [get list watch]
  roles                                                         []                 []              [get list watch]
  securitycontextconstraints                                    []                 []              [get list watch]
  services/status                                               []                 []              [get list watch]
  templateinstances/status                                      []                 []              [get list watch]
  useridentitymappings                                          []                 []              [get list watch]
  users                                                         []                 []              [get list watch]
  mutatingwebhookconfigurations.admissionregistration.k8s.io    []                 []              [get list watch]
  validatingwebhookconfigurations.admissionregistration.k8s.io  []                 []              [get list watch]
  customresourcedefinitions.apiextensions.k8s.io/status         []                 []              [get list watch]
  customresourcedefinitions.apiextensions.k8s.io                []                 []              [get list watch]
  apiservices.apiregistration.k8s.io/status                     []                 []              [get list watch]
  apiservices.apiregistration.k8s.io                            []                 []              [get list watch]
  controllerrevisions.apps                                      []                 []              [get list watch]
  daemonsets.apps/status                                        []                 []              [get list watch]
  deployments.apps/status                                       []                 []              [get list watch]
  replicasets.apps/status                                       []                 []              [get list watch]
  statefulsets.apps/status                                      []                 []              [get list watch]
  clusterrolebindings.authorization.openshift.io                []                 []              [get list watch]
  clusterroles.authorization.openshift.io                       []                 []              [get list watch]
  rolebindingrestrictions.authorization.openshift.io            []                 []              [get list watch]
  rolebindings.authorization.openshift.io                       []                 []              [get list watch]
  roles.authorization.openshift.io                              []                 []              [get list watch]
  horizontalpodautoscalers.autoscaling/status                   []                 []              [get list watch]
  cronjobs.batch/status                                         []                 []              [get list watch]
  jobs.batch/status                                             []                 []              [get list watch]
  builds.build.openshift.io/details                             []                 []              [get list watch]
  certificatesigningrequests.certificates.k8s.io/approval       []                 []              [get list watch]
  certificatesigningrequests.certificates.k8s.io/status         []                 []              [get list watch]
  certificatesigningrequests.certificates.k8s.io                []                 []              [get list watch]
  leases.coordination.k8s.io                                    []                 []              [get list watch]
  events.events.k8s.io                                          []                 []              [get list watch]
  daemonsets.extensions/status                                  []                 []              [get list watch]
  deployments.extensions/status                                 []                 []              [get list watch]
  horizontalpodautoscalers.extensions/status                    []                 []              [get list watch]
  horizontalpodautoscalers.extensions                           []                 []              [get list watch]
  ingresses.extensions/status                                   []                 []              [get list watch]
  jobs.extensions/status                                        []                 []              [get list watch]
  jobs.extensions                                               []                 []              [get list watch]
  podsecuritypolicies.extensions                                []                 []              [get list watch]
  replicasets.extensions/status                                 []                 []              [get list watch]
  replicationcontrollers.extensions                             []                 []              [get list watch]
  storageclasses.extensions                                     []                 []              [get list watch]
  thirdpartyresources.extensions                                []                 []              [get list watch]
  images.image.openshift.io                                     []                 []              [get list watch]
  imagesignatures.image.openshift.io                            []                 []              [get list watch]
  clusternetworks.network.openshift.io                          []                 []              [get list watch]
  egressnetworkpolicies.network.openshift.io                    []                 []              [get list watch]
  hostsubnets.network.openshift.io                              []                 []              [get list watch]
  netnamespaces.network.openshift.io                            []                 []              [get list watch]
  ingresses.networking.k8s.io/status                            []                 []              [get list watch]
  runtimeclasses.node.k8s.io                                    []                 []              [get list watch]
  oauthclientauthorizations.oauth.openshift.io                  []                 []              [get list watch]
  poddisruptionbudgets.policy/status                            []                 []              [get list watch]
  podsecuritypolicies.policy                                    []                 []              [get list watch]
  projectrequests.project.openshift.io                          []                 []              [get list watch]
  clusterresourcequotas.quota.openshift.io/status               []                 []              [get list watch]
  clusterresourcequotas.quota.openshift.io                      []                 []              [get list watch]
  clusterrolebindings.rbac.authorization.k8s.io                 []                 []              [get list watch]
  clusterroles.rbac.authorization.k8s.io                        []                 []              [get list watch]
  rolebindings.rbac.authorization.k8s.io                        []                 []              [get list watch]
  roles.rbac.authorization.k8s.io                               []                 []              [get list watch]
  priorityclasses.scheduling.k8s.io                             []                 []              [get list watch]
  rangeallocations.security.openshift.io                        []                 []              [get list watch]
  securitycontextconstraints.security.openshift.io              []                 []              [get list watch]
  podpresets.settings.k8s.io                                    []                 []              [get list watch]
  csidrivers.storage.k8s.io                                     []                 []              [get list watch]
  csinodes.storage.k8s.io                                       []                 []              [get list watch]
  storageclasses.storage.k8s.io                                 []                 []              [get list watch]
  volumeattachments.storage.k8s.io/status                       []                 []              [get list watch]
  volumeattachments.storage.k8s.io                              []                 []              [get list watch]
  brokertemplateinstances.template.openshift.io                 []                 []              [get list watch]
  templateinstances.template.openshift.io/status                []                 []              [get list watch]
  groups.user.openshift.io                                      []                 []              [get list watch]
  identities.user.openshift.io                                  []                 []              [get list watch]
  useridentitymappings.user.openshift.io                        []                 []              [get list watch]
  users.user.openshift.io                                       []                 []              [get list watch]
                                                                [*]                []              [get]
  imagestreams/layers                                           []                 []              [get]
  nodes/metrics                                                 []                 []              [get]
  nodes/spec                                                    []                 []              [get]
  imagestreams.image.openshift.io/layers                        []                 []              [get]
  projects                                                      []                 []              [list watch]
  projects.project.openshift.io                                 []                 []              [list watch]


Name:         system:openshift:aggregate-to-edit
Labels:       rbac.authorization.k8s.io/aggregate-to-edit=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                          Non-Resource URLs  Resource Names  Verbs
  ---------                                          -----------------  --------------  -----
  buildconfigs/webhooks                              []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs                                       []                 []              [create delete deletecollection get list patch update watch]
  buildlogs                                          []                 []              [create delete deletecollection get list patch update watch]
  builds                                             []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs/scale                            []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs                                  []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimages                                  []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings                                []                 []              [create delete deletecollection get list patch update watch]
  imagestreams/secrets                               []                 []              [create delete deletecollection get list patch update watch]
  imagestreams                                       []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags                                    []                 []              [create delete deletecollection get list patch update watch]
  imagetags                                          []                 []              [create delete deletecollection get list patch update watch]
  processedtemplates                                 []                 []              [create delete deletecollection get list patch update watch]
  routes                                             []                 []              [create delete deletecollection get list patch update watch]
  templateconfigs                                    []                 []              [create delete deletecollection get list patch update watch]
  templateinstances                                  []                 []              [create delete deletecollection get list patch update watch]
  templates                                          []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs.apps.openshift.io/scale          []                 []              [create delete deletecollection get list patch update watch]
  deploymentconfigs.apps.openshift.io                []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs.build.openshift.io/webhooks           []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs.build.openshift.io                    []                 []              [create delete deletecollection get list patch update watch]
  buildlogs.build.openshift.io                       []                 []              [create delete deletecollection get list patch update watch]
  builds.build.openshift.io                          []                 []              [create delete deletecollection get list patch update watch]
  networkpolicies.extensions                         []                 []              [create delete deletecollection get list patch update watch]
  imagestreamimages.image.openshift.io               []                 []              [create delete deletecollection get list patch update watch]
  imagestreammappings.image.openshift.io             []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io/secrets            []                 []              [create delete deletecollection get list patch update watch]
  imagestreams.image.openshift.io                    []                 []              [create delete deletecollection get list patch update watch]
  imagestreamtags.image.openshift.io                 []                 []              [create delete deletecollection get list patch update watch]
  imagetags.image.openshift.io                       []                 []              [create delete deletecollection get list patch update watch]
  networkpolicies.networking.k8s.io                  []                 []              [create delete deletecollection get list patch update watch]
  routes.route.openshift.io                          []                 []              [create delete deletecollection get list patch update watch]
  processedtemplates.template.openshift.io           []                 []              [create delete deletecollection get list patch update watch]
  templateconfigs.template.openshift.io              []                 []              [create delete deletecollection get list patch update watch]
  templateinstances.template.openshift.io            []                 []              [create delete deletecollection get list patch update watch]
  templates.template.openshift.io                    []                 []              [create delete deletecollection get list patch update watch]
  buildconfigs/instantiate                           []                 []              [create]
  buildconfigs/instantiatebinary                     []                 []              [create]
  builds/clone                                       []                 []              [create]
  deploymentconfigrollbacks                          []                 []              [create]
  deploymentconfigs/instantiate                      []                 []              [create]
  deploymentconfigs/rollback                         []                 []              [create]
  imagestreamimports                                 []                 []              [create]
  routes/custom-host                                 []                 []              [create]
  deploymentconfigrollbacks.apps.openshift.io        []                 []              [create]
  deploymentconfigs.apps.openshift.io/instantiate    []                 []              [create]
  deploymentconfigs.apps.openshift.io/rollback       []                 []              [create]
  buildconfigs.build.openshift.io/instantiate        []                 []              [create]
  buildconfigs.build.openshift.io/instantiatebinary  []                 []              [create]
  builds.build.openshift.io/clone                    []                 []              [create]
  imagestreamimports.image.openshift.io              []                 []              [create]
  routes.route.openshift.io/custom-host              []                 []              [create]
  jenkins.build.openshift.io                         []                 []              [edit view]
  appliedclusterresourcequotas                       []                 []              [get list watch]
  builds/log                                         []                 []              [get list watch]
  deploymentconfigs/log                              []                 []              [get list watch]
  deploymentconfigs/status                           []                 []              [get list watch]
  imagestreams/status                                []                 []              [get list watch]
  resourcequotausages                                []                 []              [get list watch]
  routes/status                                      []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/log            []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/status         []                 []              [get list watch]
  builds.build.openshift.io/log                      []                 []              [get list watch]
  imagestreams.image.openshift.io/status             []                 []              [get list watch]
  appliedclusterresourcequotas.quota.openshift.io    []                 []              [get list watch]
  routes.route.openshift.io/status                   []                 []              [get list watch]
  imagestreams/layers                                []                 []              [get update]
  imagestreams.image.openshift.io/layers             []                 []              [get update]
  projects                                           []                 []              [get]
  projects.project.openshift.io                      []                 []              [get]
  builds/details                                     []                 []              [update]
  builds.build.openshift.io/details                  []                 []              [update]


Name:         system:openshift:aggregate-to-storage-admin
Labels:       storage.openshift.io/aggregate-to-storage-admin=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                      Non-Resource URLs  Resource Names  Verbs
  ---------                      -----------------  --------------  -----
  persistentvolumes              []                 []              [create delete deletecollection get list patch update watch]
  storageclasses.storage.k8s.io  []                 []              [create delete deletecollection get list patch update watch]
  events                         []                 []              [get list watch]
  persistentvolumeclaims         []                 []              [get list watch]
  pods                           []                 []              [get list watch]


Name:         system:openshift:aggregate-to-view
Labels:       rbac.authorization.k8s.io/aggregate-to-view=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                        Non-Resource URLs  Resource Names  Verbs
  ---------                                        -----------------  --------------  -----
  appliedclusterresourcequotas                     []                 []              [get list watch]
  buildconfigs/webhooks                            []                 []              [get list watch]
  buildconfigs                                     []                 []              [get list watch]
  buildlogs                                        []                 []              [get list watch]
  builds/log                                       []                 []              [get list watch]
  builds                                           []                 []              [get list watch]
  deploymentconfigs/log                            []                 []              [get list watch]
  deploymentconfigs/scale                          []                 []              [get list watch]
  deploymentconfigs/status                         []                 []              [get list watch]
  deploymentconfigs                                []                 []              [get list watch]
  imagestreamimages                                []                 []              [get list watch]
  imagestreammappings                              []                 []              [get list watch]
  imagestreams/status                              []                 []              [get list watch]
  imagestreams                                     []                 []              [get list watch]
  imagestreamtags                                  []                 []              [get list watch]
  imagetags                                        []                 []              [get list watch]
  processedtemplates                               []                 []              [get list watch]
  resourcequotausages                              []                 []              [get list watch]
  routes/status                                    []                 []              [get list watch]
  routes                                           []                 []              [get list watch]
  templateconfigs                                  []                 []              [get list watch]
  templateinstances                                []                 []              [get list watch]
  templates                                        []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/log          []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/scale        []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/status       []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io              []                 []              [get list watch]
  buildconfigs.build.openshift.io/webhooks         []                 []              [get list watch]
  buildconfigs.build.openshift.io                  []                 []              [get list watch]
  buildlogs.build.openshift.io                     []                 []              [get list watch]
  builds.build.openshift.io/log                    []                 []              [get list watch]
  builds.build.openshift.io                        []                 []              [get list watch]
  imagestreamimages.image.openshift.io             []                 []              [get list watch]
  imagestreammappings.image.openshift.io           []                 []              [get list watch]
  imagestreams.image.openshift.io/status           []                 []              [get list watch]
  imagestreams.image.openshift.io                  []                 []              [get list watch]
  imagestreamtags.image.openshift.io               []                 []              [get list watch]
  imagetags.image.openshift.io                     []                 []              [get list watch]
  appliedclusterresourcequotas.quota.openshift.io  []                 []              [get list watch]
  routes.route.openshift.io/status                 []                 []              [get list watch]
  routes.route.openshift.io                        []                 []              [get list watch]
  processedtemplates.template.openshift.io         []                 []              [get list watch]
  templateconfigs.template.openshift.io            []                 []              [get list watch]
  templateinstances.template.openshift.io          []                 []              [get list watch]
  templates.template.openshift.io                  []                 []              [get list watch]
  projects                                         []                 []              [get]
  projects.project.openshift.io                    []                 []              [get]
  jenkins.build.openshift.io                       []                 []              [view]


Name:         system:openshift:cloud-credential-operator:cluster-reader
Labels:       rbac.authorization.k8s.io/aggregate-to-cluster-reader=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  credentialsrequests.cloudcredential.openshift.io  []                 []              [get list watch]


Name:         system:openshift:cluster-config-operator:cluster-reader
Labels:       rbac.authorization.k8s.io/aggregate-to-cluster-reader=true
Annotations:  include.release.openshift.io/self-managed-high-availability: true
PolicyRule:
  Resources                             Non-Resource URLs  Resource Names  Verbs
  ---------                             -----------------  --------------  -----
  apiservers.config.openshift.io        []                 []              [get list watch]
  authentications.config.openshift.io   []                 []              [get list watch]
  builds.config.openshift.io            []                 []              [get list watch]
  clusteroperators.config.openshift.io  []                 []              [get list watch]
  clusterversions.config.openshift.io   []                 []              [get list watch]
  consoles.config.openshift.io          []                 []              [get list watch]
  dnses.config.openshift.io             []                 []              [get list watch]
  featuregates.config.openshift.io      []                 []              [get list watch]
  images.config.openshift.io            []                 []              [get list watch]
  infrastructures.config.openshift.io   []                 []              [get list watch]
  ingresses.config.openshift.io         []                 []              [get list watch]
  networks.config.openshift.io          []                 []              [get list watch]
  oauths.config.openshift.io            []                 []              [get list watch]
  projects.config.openshift.io          []                 []              [get list watch]
  proxies.config.openshift.io           []                 []              [get list watch]
  schedulers.config.openshift.io        []                 []              [get list watch]


Name:         system:openshift:cluster-samples-operator:cluster-reader
Labels:       rbac.authorization.k8s.io/aggregate-to-cluster-reader=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                     -----------------  --------------  -----
  configs.samples.operator.openshift.io/status  []                 []              [get list watch]
  configs.samples.operator.openshift.io         []                 []              [get list watch]


Name:         system:openshift:controller:build-config-change-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                    Non-Resource URLs  Resource Names  Verbs
  ---------                                    -----------------  --------------  -----
  events                                       []                 []              [create patch update]
  buildconfigs/instantiate                     []                 []              [create]
  buildconfigs.build.openshift.io/instantiate  []                 []              [create]
  builds                                       []                 []              [delete]
  builds.build.openshift.io                    []                 []              [delete]
  buildconfigs                                 []                 []              [get list watch]
  buildconfigs.build.openshift.io              []                 []              [get list watch]


Name:         system:openshift:controller:build-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                              Non-Resource URLs  Resource Names  Verbs
  ---------                                              -----------------  --------------  -----
  pods                                                   []                 []              [create delete get list]
  configmaps                                             []                 []              [create get list]
  events                                                 []                 []              [create patch update]
  builds/custom                                          []                 []              [create]
  builds/docker                                          []                 []              [create]
  builds/jenkinspipeline                                 []                 []              [create]
  builds/optimizeddocker                                 []                 []              [create]
  builds/source                                          []                 []              [create]
  podsecuritypolicysubjectreviews                        []                 []              [create]
  builds.build.openshift.io/custom                       []                 []              [create]
  builds.build.openshift.io/docker                       []                 []              [create]
  builds.build.openshift.io/jenkinspipeline              []                 []              [create]
  builds.build.openshift.io/optimizeddocker              []                 []              [create]
  builds.build.openshift.io/source                       []                 []              [create]
  podsecuritypolicysubjectreviews.security.openshift.io  []                 []              [create]
  builds                                                 []                 []              [delete get list patch update watch]
  builds.build.openshift.io                              []                 []              [delete get list patch update watch]
  imagestreams                                           []                 []              [get list]
  secrets                                                []                 []              [get list]
  serviceaccounts                                        []                 []              [get list]
  builds.config.openshift.io                             []                 []              [get list]
  imagestreams.image.openshift.io                        []                 []              [get list]
  buildconfigs                                           []                 []              [get]
  namespaces                                             []                 []              [get]
  buildconfigs.build.openshift.io                        []                 []              [get]
  builds/finalizers                                      []                 []              [update]
  builds.build.openshift.io/finalizers                   []                 []              [update]


Name:         system:openshift:controller:check-endpoints
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                               Non-Resource URLs  Resource Names  Verbs
  ---------                                                               -----------------  --------------  -----
  podnetworkconnectivitychecks.controlplane.operator.openshift.io/status  []                 []              [get list patch update watch]
  events                                                                  []                 []              [get list watch create update patch]
  pods                                                                    []                 []              [get list watch]
  secrets                                                                 []                 []              [get list watch]
  podnetworkconnectivitychecks.controlplane.operator.openshift.io         []                 []              [get list watch]


Name:         system:openshift:controller:check-endpoints-crd-reader
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  customresourcedefinitions.apiextensions.k8s.io  []                 []              [get list watch]


Name:         system:openshift:controller:check-endpoints-node-reader
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  nodes      []                 []              [get list watch]


Name:         system:openshift:controller:cluster-quota-reconciliation-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                        Non-Resource URLs  Resource Names  Verbs
  ---------                                        -----------------  --------------  -----
  events                                           []                 []              [create patch update]
  configmaps                                       []                 []              [get list]
  secrets                                          []                 []              [get list]
  clusterresourcequotas/status                     []                 []              [update]
  clusterresourcequotas.quota.openshift.io/status  []                 []              [update]


Name:         system:openshift:controller:default-rolebindings-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                               Non-Resource URLs  Resource Names  Verbs
  ---------                               -----------------  --------------  -----
  rolebindings.rbac.authorization.k8s.io  []                 []              [create get list watch]
  events                                  []                 []              [create patch update]
  namespaces                              []                 []              [get list watch]


Name:         system:openshift:controller:deployer-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                     Non-Resource URLs  Resource Names  Verbs
  ---------                     -----------------  --------------  -----
  pods                          []                 []              [create delete get list patch watch]
  events                        []                 []              [create patch update]
  replicationcontrollers        []                 []              [delete get list update watch]
  replicationcontrollers/scale  []                 []              [get update]


Name:         system:openshift:controller:deploymentconfig-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  replicationcontrollers                          []                 []              [create delete get list patch update watch]
  events                                          []                 []              [create patch update]
  deploymentconfigs                               []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io             []                 []              [get list watch]
  replicationcontrollers/scale                    []                 []              [get update]
  deploymentconfigs/finalizers                    []                 []              [update]
  deploymentconfigs/status                        []                 []              [update]
  deploymentconfigs.apps.openshift.io/finalizers  []                 []              [update]
  deploymentconfigs.apps.openshift.io/status      []                 []              [update]


Name:         system:openshift:controller:horizontal-pod-autoscaler
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  deploymentconfigs/scale                    []                 []              [get update]
  deploymentconfigs.apps.openshift.io/scale  []                 []              [get update]


Name:         system:openshift:controller:image-import-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                              Non-Resource URLs  Resource Names  Verbs
  ---------                              -----------------  --------------  -----
  images                                 []                 []              [create delete get list patch update watch]
  images.image.openshift.io              []                 []              [create delete get list patch update watch]
  imagestreams                           []                 []              [create get list update watch]
  imagestreams.image.openshift.io        []                 []              [create get list update watch]
  events                                 []                 []              [create patch update]
  imagestreamimports                     []                 []              [create]
  imagestreamimports.image.openshift.io  []                 []              [create]


Name:         system:openshift:controller:image-trigger-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                    Non-Resource URLs  Resource Names  Verbs
  ---------                                    -----------------  --------------  -----
  events                                       []                 []              [create patch update]
  buildconfigs/instantiate                     []                 []              [create]
  builds/custom                                []                 []              [create]
  builds/docker                                []                 []              [create]
  builds/jenkinspipeline                       []                 []              [create]
  builds/optimizeddocker                       []                 []              [create]
  builds/source                                []                 []              [create]
  buildconfigs.build.openshift.io/instantiate  []                 []              [create]
  builds.build.openshift.io/custom             []                 []              [create]
  builds.build.openshift.io/docker             []                 []              [create]
  builds.build.openshift.io/jenkinspipeline    []                 []              [create]
  builds.build.openshift.io/optimizeddocker    []                 []              [create]
  builds.build.openshift.io/source             []                 []              [create]
  deploymentconfigs                            []                 []              [get update]
  deploymentconfigs.apps.openshift.io          []                 []              [get update]
  deployments.apps                             []                 []              [get update]
  statefulsets.apps                            []                 []              [get update]
  cronjobs.batch                               []                 []              [get update]
  daemonsets.extensions                        []                 []              [get update]
  deployments.extensions                       []                 []              [get update]
  imagestreams                                 []                 []              [list watch]
  imagestreams.image.openshift.io              []                 []              [list watch]


Name:         system:openshift:controller:machine-approver
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                Non-Resource URLs  Resource Names                                 Verbs
  ---------                                                -----------------  --------------                                 -----
  signers.certificates.k8s.io                              []                 [kubernetes.io/kube-apiserver-client-kubelet]  [approve]
  signers.certificates.k8s.io                              []                 [kubernetes.io/kubelet-serving]                [approve]
  tokenreviews.authentication.k8s.io                       []                 []                                             [create]
  subjectaccessreviews.authorization.k8s.io                []                 []                                             [create]
  clusteroperators.config.openshift.io                     []                 []                                             [get create list watch]
  certificatesigningrequests.certificates.k8s.io           []                 []                                             [get list watch]
  machines.machine.openshift.io                            []                 []                                             [get list watch]
  nodes                                                    []                 []                                             [get]
  certificatesigningrequests.certificates.k8s.io/approval  []                 []                                             [update]
  clusteroperators.config.openshift.io/status              []                 [machine-approver]                             [update]


Name:         system:openshift:controller:namespace-security-allocation-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                        Non-Resource URLs  Resource Names  Verbs
  ---------                                        -----------------  --------------  -----
  rangeallocations.security.internal.openshift.io  []                 []              [create get update]
  rangeallocations.security.openshift.io           []                 []              [create get update]
  events                                           []                 []              [create patch update]
  namespaces                                       []                 []              [get list update watch patch]


Name:         system:openshift:controller:origin-namespace-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources            Non-Resource URLs  Resource Names  Verbs
  ---------            -----------------  --------------  -----
  events               []                 []              [create patch update]
  namespaces           []                 []              [get list watch]
  namespaces/finalize  []                 []              [update]
  namespaces/status    []                 []              [update]


Name:         system:openshift:controller:pv-recycler-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                      Non-Resource URLs  Resource Names  Verbs
  ---------                      -----------------  --------------  -----
  persistentvolumes              []                 []              [create delete get list update watch]
  pods                           []                 []              [create delete get list watch]
  events                         []                 []              [create patch update]
  persistentvolumeclaims         []                 []              [get list update watch]
  persistentvolumeclaims/status  []                 []              [update]
  persistentvolumes/status       []                 []              [update]


Name:         system:openshift:controller:resourcequota-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources               Non-Resource URLs  Resource Names  Verbs
  ---------               -----------------  --------------  -----
  events                  []                 []              [create patch update]
  configmaps              []                 []              [list]
  replicationcontrollers  []                 []              [list]
  resourcequotas          []                 []              [list]
  secrets                 []                 []              [list]
  services                []                 []              [list]
  resourcequotas/status   []                 []              [update]


Name:         system:openshift:controller:service-ca
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                     Non-Resource URLs  Resource Names  Verbs
  ---------                                                     -----------------  --------------  -----
  secrets                                                       []                 []              [get list watch create update patch]
  services                                                      []                 []              [get list watch update patch]
  apiservices.apiregistration.k8s.io                            []                 []              [get list watch update patch]
  configmaps                                                    []                 []              [get list watch update]
  mutatingwebhookconfigurations.admissionregistration.k8s.io    []                 []              [get list watch update]
  validatingwebhookconfigurations.admissionregistration.k8s.io  []                 []              [get list watch update]
  customresourcedefinitions.apiextensions.k8s.io                []                 []              [get list watch update]


Name:         system:openshift:controller:service-ingress-ip-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources        Non-Resource URLs  Resource Names  Verbs
  ---------        -----------------  --------------  -----
  events           []                 []              [create patch update]
  services         []                 []              [list update watch]
  services/status  []                 []              [update]


Name:         system:openshift:controller:service-serving-cert-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  secrets    []                 []              [create delete get list update watch]
  events     []                 []              [create patch update]
  services   []                 []              [list update watch]


Name:         system:openshift:controller:serviceaccount-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources        Non-Resource URLs  Resource Names  Verbs
  ---------        -----------------  --------------  -----
  serviceaccounts  []                 []              [create delete get list patch update watch]
  events           []                 []              [create patch update]


Name:         system:openshift:controller:serviceaccount-pull-secrets-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources        Non-Resource URLs  Resource Names  Verbs
  ---------        -----------------  --------------  -----
  secrets          []                 []              [create delete get list patch update watch]
  serviceaccounts  []                 []              [create get list update watch]
  events           []                 []              [create patch update]
  services         []                 []              [get list watch]


Name:         system:openshift:controller:template-instance-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  subjectaccessreviews.authorization.k8s.io       []                 []              [create]
  templateinstances.template.openshift.io/status  []                 []              [update]


Name:         system:openshift:controller:template-instance-finalizer-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                       Non-Resource URLs  Resource Names  Verbs
  ---------                                       -----------------  --------------  -----
  templateinstances.template.openshift.io/status  []                 []              [update]


Name:         system:openshift:controller:template-service-broker
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                                 Non-Resource URLs  Resource Names  Verbs
  ---------                                                 -----------------  --------------  -----
  templateinstances.template.openshift.io                   []                 []              [assign create delete get]
  brokertemplateinstances.template.openshift.io             []                 []              [create delete get update]
  secrets                                                   []                 []              [create delete get]
  events                                                    []                 []              [create patch update]
  subjectaccessreviews.authorization.k8s.io                 []                 []              [create]
  subjectaccessreviews.authorization.openshift.io           []                 []              [create]
  templates.template.openshift.io                           []                 []              [get list watch]
  configmaps                                                []                 []              [get]
  routes                                                    []                 []              [get]
  services                                                  []                 []              [get]
  routes.route.openshift.io                                 []                 []              [get]
  brokertemplateinstances.template.openshift.io/finalizers  []                 []              [update]


Name:         system:openshift:controller:unidling-controller
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  deploymentconfigs                          []                 []              [get patch update]
  replicationcontrollers                     []                 []              [get patch update]
  deploymentconfigs.apps.openshift.io        []                 []              [get patch update]
  deploymentconfigs/scale                    []                 []              [get update]
  endpoints                                  []                 []              [get update]
  replicationcontrollers/scale               []                 []              [get update]
  services                                   []                 []              [get update]
  deploymentconfigs.apps.openshift.io/scale  []                 []              [get update]
  deployments.apps/scale                     []                 []              [get update]
  replicasets.apps/scale                     []                 []              [get update]
  deployments.extensions/scale               []                 []              [get update]
  replicasets.extensions/scale               []                 []              [get update]
  events                                     []                 []              [list watch create patch update]


Name:         system:openshift:discovery
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs       Resource Names  Verbs
  ---------  -----------------       --------------  -----
             [/.well-known/*]        []              [get]
             [/.well-known]          []              [get]
             [/]                     []              [get]
             [/api/*]                []              [get]
             [/api]                  []              [get]
             [/apis/*]               []              [get]
             [/apis]                 []              [get]
             [/oapi/*]               []              [get]
             [/oapi]                 []              [get]
             [/openapi/v2]           []              [get]
             [/osapi/]               []              [get]
             [/osapi]                []              [get]
             [/swagger-2.0.0.pb-v1]  []              [get]
             [/swagger.json]         []              [get]
             [/swaggerapi/*]         []              [get]
             [/swaggerapi]           []              [get]
             [/version/*]            []              [get]
             [/version]              []              [get]


Name:         system:openshift:kube-controller-manager:gce-cloud-provider
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources        Non-Resource URLs  Resource Names  Verbs
  ---------        -----------------  --------------  -----
  events           []                 []              [create patch update]
  services/status  []                 []              [patch update]


Name:         system:openshift:machine-config-operator:cluster-reader
Labels:       rbac.authorization.k8s.io/aggregate-to-cluster-reader=true
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                                  -----------------  --------------  -----
  containerruntimeconfigs.machineconfiguration.openshift.io  []                 []              [get list watch]
  controllerconfigs.machineconfiguration.openshift.io        []                 []              [get list watch]
  kubeletconfigs.machineconfiguration.openshift.io           []                 []              [get list watch]
  machineconfigpools.machineconfiguration.openshift.io       []                 []              [get list watch]


Name:         system:openshift:openshift-controller-manager
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources             Non-Resource URLs  Resource Names  Verbs
  ---------             -----------------  --------------  -----
  events                []                 []              [create patch update]
  events.events.k8s.io  []                 []              [create patch update]
  *.*                   []                 []              [get list watch]


Name:         system:openshift:openshift-controller-manager:ingress-to-route-controller
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                              Non-Resource URLs  Resource Names  Verbs
  ---------                              -----------------  --------------  -----
  routes.route.openshift.io              []                 []              [create delete get list patch update watch]
  events                                 []                 []              [create patch update]
  routes.route.openshift.io/custom-host  []                 []              [create update]
  secrets                                []                 []              [get list watch]
  services                               []                 []              [get list watch]
  ingress.networking.k8s.io              []                 []              [get list watch]
  ingresses.networking.k8s.io/status     []                 []              [update]


Name:         system:openshift:public-info-viewer
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
             [/.well-known/*]   []              [get]
             [/.well-known]     []              [get]


Name:         system:openshift:scc:anyuid
Labels:       &lt;none&gt;
Annotations:  include.release.openshift.io/self-managed-high-availability: true
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  securitycontextconstraints.security.openshift.io  []                 [anyuid]        [use]


Name:         system:openshift:scc:hostaccess
Labels:       &lt;none&gt;
Annotations:  include.release.openshift.io/self-managed-high-availability: true
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  securitycontextconstraints.security.openshift.io  []                 [hostaccess]    [use]


Name:         system:openshift:scc:hostmount
Labels:       &lt;none&gt;
Annotations:  include.release.openshift.io/self-managed-high-availability: true
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  securitycontextconstraints.security.openshift.io  []                 [hostmount]     [use]


Name:         system:openshift:scc:hostmount-anyuid
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names      Verbs
  ---------                                         -----------------  --------------      -----
  securitycontextconstraints.security.openshift.io  []                 [hostmount-anyuid]  [use]


Name:         system:openshift:scc:hostnetwork
Labels:       &lt;none&gt;
Annotations:  include.release.openshift.io/self-managed-high-availability: true
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  securitycontextconstraints.security.openshift.io  []                 [hostnetwork]   [use]


Name:         system:openshift:scc:nonroot
Labels:       &lt;none&gt;
Annotations:  include.release.openshift.io/self-managed-high-availability: true
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  securitycontextconstraints.security.openshift.io  []                 [nonroot]       [use]


Name:         system:openshift:scc:privileged
Labels:       &lt;none&gt;
Annotations:  include.release.openshift.io/self-managed-high-availability: true
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  securitycontextconstraints.security.openshift.io  []                 [privileged]    [use]


Name:         system:openshift:scc:restricted
Labels:       &lt;none&gt;
Annotations:  include.release.openshift.io/self-managed-high-availability: true
              rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                         Non-Resource URLs  Resource Names  Verbs
  ---------                                         -----------------  --------------  -----
  securitycontextconstraints.security.openshift.io  []                 [restricted]    [use]


Name:         system:openshift:templateservicebroker-client
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs                   Resource Names  Verbs
  ---------  -----------------                   --------------  -----
             [/brokers/template.openshift.io/*]  []              [delete]
             [/brokers/template.openshift.io/*]  []              [get]
             [/brokers/template.openshift.io/*]  []              [put]
             [/brokers/template.openshift.io/*]  []              [update]


Name:         system:openshift:tokenreview-openshift-controller-manager
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  tokenreviews.authentication.k8s.io         []                 []              [create]
  subjectaccessreviews.authorization.k8s.io  []                 []              [create]


Name:         system:persistent-volume-provisioner
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                      Non-Resource URLs  Resource Names  Verbs
  ---------                      -----------------  --------------  -----
  persistentvolumes              []                 []              [create delete get list watch]
  events.events.k8s.io           []                 []              [create patch update]
  persistentvolumeclaims         []                 []              [get list update watch]
  storageclasses.storage.k8s.io  []                 []              [get list watch]
  events                         []                 []              [watch create patch update]


Name:         system:public-info-viewer
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
             [/healthz]         []              [get]
             [/livez]           []              [get]
             [/readyz]          []              [get]
             [/version/]        []              [get]
             [/version]         []              [get]


Name:         system:registry
Labels:       &lt;none&gt;
Annotations:  imageregistry.operator.openshift.io/checksum: sha256:4f5c458a9529be990802411d939d2126b77fa47083541be8946d4ca262db41d0
PolicyRule:
  Resources                                Non-Resource URLs  Resource Names  Verbs
  ---------                                -----------------  --------------  -----
  imagestreammappings.image.openshift.io   []                 []              [create]
  imagestreamtags.image.openshift.io       []                 []              [delete]
  images.image.openshift.io                []                 []              [get update]
  imagestreams.image.openshift.io          []                 []              [get update]
  imagestreamimages.image.openshift.io     []                 []              [get]
  imagestreams.image.openshift.io/layers   []                 []              [get]
  imagestreams.image.openshift.io/secrets  []                 []              [get]
  limitranges                              []                 []              [list]
  resourcequotas                           []                 []              [list]


Name:         system:router
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  tokenreviews.authentication.k8s.io         []                 []              [create]
  subjectaccessreviews.authorization.k8s.io  []                 []              [create]
  endpoints                                  []                 []              [list watch]
  routes                                     []                 []              [list watch]
  services                                   []                 []              [list watch]
  endpointslices.discovery.k8s.io            []                 []              [list watch]
  routes.route.openshift.io                  []                 []              [list watch]
  routes/status                              []                 []              [update]
  routes.route.openshift.io/status           []                 []              [update]


Name:         system:scope-impersonation
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                                           Non-Resource URLs  Resource Names  Verbs
  ---------                                                           -----------------  --------------  -----
  userextras.authentication.k8s.io/scopes.authorization.openshift.io  []                 []              [impersonate]


Name:         system:sdn-manager
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                             Non-Resource URLs  Resource Names  Verbs
  ---------                             -----------------  --------------  -----
  hostsubnets                           []                 []              [create delete get list watch]
  netnamespaces                         []                 []              [create delete get list watch]
  hostsubnets.network.openshift.io      []                 []              [create delete get list watch]
  netnamespaces.network.openshift.io    []                 []              [create delete get list watch]
  clusternetworks                       []                 []              [create get]
  clusternetworks.network.openshift.io  []                 []              [create get]
  nodes                                 []                 []              [get list watch]


Name:         system:sdn-reader
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                   Non-Resource URLs  Resource Names  Verbs
  ---------                                   -----------------  --------------  -----
  events                                      []                 []              [create patch update]
  egressnetworkpolicies                       []                 []              [get list watch]
  hostsubnets                                 []                 []              [get list watch]
  namespaces                                  []                 []              [get list watch]
  netnamespaces                               []                 []              [get list watch]
  nodes                                       []                 []              [get list watch]
  networkpolicies.extensions                  []                 []              [get list watch]
  egressnetworkpolicies.network.openshift.io  []                 []              [get list watch]
  hostsubnets.network.openshift.io            []                 []              [get list watch]
  netnamespaces.network.openshift.io          []                 []              [get list watch]
  networkpolicies.networking.k8s.io           []                 []              [get list watch]
  clusternetworks                             []                 []              [get]
  clusternetworks.network.openshift.io        []                 []              [get]


Name:         system:volume-scheduler
Labels:       kubernetes.io/bootstrapping=rbac-defaults
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                      Non-Resource URLs  Resource Names  Verbs
  ---------                      -----------------  --------------  -----
  persistentvolumeclaims         []                 []              [get list patch update watch]
  persistentvolumes              []                 []              [get list patch update watch]
  storageclasses.storage.k8s.io  []                 []              [get list watch]


Name:         system:webhook
Labels:       &lt;none&gt;
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                 Non-Resource URLs  Resource Names  Verbs
  ---------                                 -----------------  --------------  -----
  buildconfigs/webhooks                     []                 []              [create get]
  buildconfigs.build.openshift.io/webhooks  []                 []              [create get]


Name:         thanos-querier
Labels:       app.kubernetes.io/component=query-layer
              app.kubernetes.io/instance=thanos-querier
              app.kubernetes.io/name=thanos-query
              app.kubernetes.io/version=0.12.0
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                  Non-Resource URLs  Resource Names  Verbs
  ---------                                  -----------------  --------------  -----
  tokenreviews.authentication.k8s.io         []                 []              [create]
  subjectaccessreviews.authorization.k8s.io  []                 []              [create]


Name:         view
Labels:       kubernetes.io/bootstrapping=rbac-defaults
              rbac.authorization.k8s.io/aggregate-to-edit=true
Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
PolicyRule:
  Resources                                            Non-Resource URLs  Resource Names  Verbs
  ---------                                            -----------------  --------------  -----
  appliedclusterresourcequotas                         []                 []              [get list watch]
  bindings                                             []                 []              [get list watch]
  buildconfigs/webhooks                                []                 []              [get list watch]
  buildconfigs                                         []                 []              [get list watch]
  buildlogs                                            []                 []              [get list watch]
  builds/log                                           []                 []              [get list watch]
  builds                                               []                 []              [get list watch]
  configmaps                                           []                 []              [get list watch]
  deploymentconfigs/log                                []                 []              [get list watch]
  deploymentconfigs/scale                              []                 []              [get list watch]
  deploymentconfigs/status                             []                 []              [get list watch]
  deploymentconfigs                                    []                 []              [get list watch]
  endpoints                                            []                 []              [get list watch]
  events                                               []                 []              [get list watch]
  imagestreamimages                                    []                 []              [get list watch]
  imagestreammappings                                  []                 []              [get list watch]
  imagestreams/status                                  []                 []              [get list watch]
  imagestreams                                         []                 []              [get list watch]
  imagestreamtags                                      []                 []              [get list watch]
  imagetags                                            []                 []              [get list watch]
  limitranges                                          []                 []              [get list watch]
  namespaces/status                                    []                 []              [get list watch]
  namespaces                                           []                 []              [get list watch]
  persistentvolumeclaims/status                        []                 []              [get list watch]
  persistentvolumeclaims                               []                 []              [get list watch]
  pods/log                                             []                 []              [get list watch]
  pods/status                                          []                 []              [get list watch]
  pods                                                 []                 []              [get list watch]
  processedtemplates                                   []                 []              [get list watch]
  replicationcontrollers/scale                         []                 []              [get list watch]
  replicationcontrollers/status                        []                 []              [get list watch]
  replicationcontrollers                               []                 []              [get list watch]
  resourcequotas/status                                []                 []              [get list watch]
  resourcequotas                                       []                 []              [get list watch]
  resourcequotausages                                  []                 []              [get list watch]
  routes/status                                        []                 []              [get list watch]
  routes                                               []                 []              [get list watch]
  serviceaccounts                                      []                 []              [get list watch]
  services/status                                      []                 []              [get list watch]
  services                                             []                 []              [get list watch]
  templateconfigs                                      []                 []              [get list watch]
  templateinstances                                    []                 []              [get list watch]
  templates                                            []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/log              []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/scale            []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io/status           []                 []              [get list watch]
  deploymentconfigs.apps.openshift.io                  []                 []              [get list watch]
  controllerrevisions.apps                             []                 []              [get list watch]
  daemonsets.apps/status                               []                 []              [get list watch]
  daemonsets.apps                                      []                 []              [get list watch]
  deployments.apps/scale                               []                 []              [get list watch]
  deployments.apps/status                              []                 []              [get list watch]
  deployments.apps                                     []                 []              [get list watch]
  replicasets.apps/scale                               []                 []              [get list watch]
  replicasets.apps/status                              []                 []              [get list watch]
  replicasets.apps                                     []                 []              [get list watch]
  statefulsets.apps/scale                              []                 []              [get list watch]
  statefulsets.apps/status                             []                 []              [get list watch]
  statefulsets.apps                                    []                 []              [get list watch]
  horizontalpodautoscalers.autoscaling/status          []                 []              [get list watch]
  horizontalpodautoscalers.autoscaling                 []                 []              [get list watch]
  cronjobs.batch/status                                []                 []              [get list watch]
  cronjobs.batch                                       []                 []              [get list watch]
  jobs.batch/status                                    []                 []              [get list watch]
  jobs.batch                                           []                 []              [get list watch]
  buildconfigs.build.openshift.io/webhooks             []                 []              [get list watch]
  buildconfigs.build.openshift.io                      []                 []              [get list watch]
  buildlogs.build.openshift.io                         []                 []              [get list watch]
  builds.build.openshift.io/log                        []                 []              [get list watch]
  builds.build.openshift.io                            []                 []              [get list watch]
  daemonsets.extensions/status                         []                 []              [get list watch]
  daemonsets.extensions                                []                 []              [get list watch]
  deployments.extensions/scale                         []                 []              [get list watch]
  deployments.extensions/status                        []                 []              [get list watch]
  deployments.extensions                               []                 []              [get list watch]
  ingresses.extensions/status                          []                 []              [get list watch]
  ingresses.extensions                                 []                 []              [get list watch]
  networkpolicies.extensions                           []                 []              [get list watch]
  replicasets.extensions/scale                         []                 []              [get list watch]
  replicasets.extensions/status                        []                 []              [get list watch]
  replicasets.extensions                               []                 []              [get list watch]
  replicationcontrollers.extensions/scale              []                 []              [get list watch]
  imagestreamimages.image.openshift.io                 []                 []              [get list watch]
  imagestreammappings.image.openshift.io               []                 []              [get list watch]
  imagestreams.image.openshift.io/status               []                 []              [get list watch]
  imagestreams.image.openshift.io                      []                 []              [get list watch]
  imagestreamtags.image.openshift.io                   []                 []              [get list watch]
  imagetags.image.openshift.io                         []                 []              [get list watch]
  nodes.metrics.k8s.io                                 []                 []              [get list watch]
  pods.metrics.k8s.io                                  []                 []              [get list watch]
  ingresses.networking.k8s.io/status                   []                 []              [get list watch]
  ingresses.networking.k8s.io                          []                 []              [get list watch]
  networkpolicies.networking.k8s.io                    []                 []              [get list watch]
  catalogsources.operators.coreos.com                  []                 []              [get list watch]
  clusterserviceversions.operators.coreos.com          []                 []              [get list watch]
  installplans.operators.coreos.com                    []                 []              [get list watch]
  operatorgroups.operators.coreos.com                  []                 []              [get list watch]
  subscriptions.operators.coreos.com                   []                 []              [get list watch]
  packagemanifests.packages.operators.coreos.com/icon  []                 []              [get list watch]
  packagemanifests.packages.operators.coreos.com       []                 []              [get list watch]
  poddisruptionbudgets.policy/status                   []                 []              [get list watch]
  poddisruptionbudgets.policy                          []                 []              [get list watch]
  appliedclusterresourcequotas.quota.openshift.io      []                 []              [get list watch]
  routes.route.openshift.io/status                     []                 []              [get list watch]
  routes.route.openshift.io                            []                 []              [get list watch]
  volumesnapshots.snapshot.storage.k8s.io              []                 []              [get list watch]
  processedtemplates.template.openshift.io             []                 []              [get list watch]
  templateconfigs.template.openshift.io                []                 []              [get list watch]
  templateinstances.template.openshift.io              []                 []              [get list watch]
  templates.template.openshift.io                      []                 []              [get list watch]
  imagestreams/layers                                  []                 []              [get]
  projects                                             []                 []              [get]
  imagestreams.image.openshift.io/layers               []                 []              [get]
  projects.project.openshift.io                        []                 []              [get]
  jenkins.build.openshift.io                           []                 []              [view]


Name:         whereabouts-cni
Labels:       &lt;none&gt;
Annotations:  &lt;none&gt;
PolicyRule:
  Resources                                               Non-Resource URLs  Resource Names  Verbs
  ---------                                               -----------------  --------------  -----
  ippools.whereabouts.cni.cncf.io                         []                 []              [get list watch create update patch delete]
  overlappingrangeipreservations.whereabouts.cni.cncf.io  []                 []              [get list watch create update patch delete]
[student@workstation ~]$ oc describe clusterrole.rbac | grep ^Name | grep -v &apos;system:&apos;
Name:         admin
Name:         aggregate-olm-edit
Name:         aggregate-olm-view
Name:         alertmanager-main
Name:         basic-user
Name:         cloud-credential-operator-role
Name:         cluster-admin
Name:         cluster-autoscaler
Name:         cluster-autoscaler-operator
Name:         cluster-autoscaler-operator:cluster-reader
Name:         cluster-debugger
Name:         cluster-image-registry-operator
Name:         cluster-monitoring-operator
Name:         cluster-monitoring-view
Name:         cluster-node-tuning-operator
Name:         cluster-node-tuning:tuned
Name:         cluster-reader
Name:         cluster-samples-operator
Name:         cluster-samples-operator-proxy-reader
Name:         cluster-status
Name:         console
Name:         console-extensions-reader
Name:         console-operator
Name:         dns-monitoring
Name:         edit
Name:         global-operators-admin
Name:         global-operators-edit
Name:         global-operators-view
Name:         grafana
Name:         helm-chartrepos-viewer
Name:         insights-operator
Name:         insights-operator-gather
Name:         kube-apiserver
Name:         kube-state-metrics
Name:         machine-api-controllers
Name:         machine-api-operator
Name:         machine-api-operator:cluster-reader
Name:         machine-config-controller
Name:         machine-config-controller-events
Name:         machine-config-daemon
Name:         machine-config-daemon-events
Name:         machine-config-server
Name:         marketplace-operator
Name:         metrics-daemon-role
Name:         monitoring-edit
Name:         monitoring-rules-edit
Name:         monitoring-rules-view
Name:         multus
Name:         multus-admission-controller-webhook
Name:         nfs-client-provisioner-runner
Name:         node-exporter
Name:         olm-operators-admin
Name:         olm-operators-edit
Name:         olm-operators-view
Name:         openshift-cluster-monitoring-admin
Name:         openshift-cluster-monitoring-edit
Name:         openshift-cluster-monitoring-view
Name:         openshift-csi-snapshot-controller-runner
Name:         openshift-dns
Name:         openshift-dns-operator
Name:         openshift-ingress-operator
Name:         openshift-ingress-router
Name:         openshift-sdn
Name:         openshift-sdn-controller
Name:         openshift-state-metrics
Name:         operatorhub-config-reader
Name:         packagemanifests-v1-admin
Name:         packagemanifests-v1-edit
Name:         packagemanifests-v1-view
Name:         prometheus-adapter
Name:         prometheus-k8s
Name:         prometheus-operator
Name:         registry-admin
Name:         registry-editor
Name:         registry-monitoring
Name:         registry-viewer
Name:         resource-metrics-server-resources
Name:         router-monitoring
Name:         self-access-reviewer
Name:         self-provisioner
Name:         storage-admin
Name:         sudoer
Name:         thanos-querier
Name:         view
Name:         whereabouts-cni
[student@workstation ~]$ oc whoami
admin
[student@workstation ~]$ oc adm policy add-cluster-role-to-group cluster-admin admins
clusterrole.rbac.authorization.k8s.io/cluster-admin added: &quot;admins&quot;
[student@workstation ~]$ oc adm policy add-cluster-role-to-group edit developers
clusterrole.rbac.authorization.k8s.io/edit added: &quot;developers&quot;
[student@workstation ~]$ oc adm policy add-cluster-role-to-group view developers
clusterrole.rbac.authorization.k8s.io/view added: &quot;developers&quot;
[student@workstation ~]$ oc adm policy add-cluster-role-to-group view viewers
clusterrole.rbac.authorization.k8s.io/view added: &quot;viewers&quot;
[student@workstation ~]$ oc get ns
NAME                                               STATUS   AGE
default                                            Active   468d
kube-node-lease                                    Active   468d
kube-public                                        Active   468d
kube-system                                        Active   468d
nfs-client-provisioner                             Active   468d
openshift                                          Active   468d
openshift-apiserver                                Active   468d
openshift-apiserver-operator                       Active   468d
openshift-authentication                           Active   468d
openshift-authentication-operator                  Active   468d
openshift-cloud-credential-operator                Active   468d
openshift-cluster-csi-drivers                      Active   468d
openshift-cluster-machine-approver                 Active   468d
openshift-cluster-node-tuning-operator             Active   468d
openshift-cluster-samples-operator                 Active   468d
openshift-cluster-storage-operator                 Active   468d
openshift-cluster-version                          Active   468d
openshift-config                                   Active   468d
openshift-config-managed                           Active   468d
openshift-config-operator                          Active   468d
openshift-console                                  Active   468d
openshift-console-operator                         Active   468d
openshift-controller-manager                       Active   468d
openshift-controller-manager-operator              Active   468d
openshift-dns                                      Active   468d
openshift-dns-operator                             Active   468d
openshift-etcd                                     Active   468d
openshift-etcd-operator                            Active   468d
openshift-image-registry                           Active   468d
openshift-infra                                    Active   468d
openshift-ingress                                  Active   468d
openshift-ingress-operator                         Active   468d
openshift-insights                                 Active   468d
openshift-kni-infra                                Active   468d
openshift-kube-apiserver                           Active   468d
openshift-kube-apiserver-operator                  Active   468d
openshift-kube-controller-manager                  Active   468d
openshift-kube-controller-manager-operator         Active   468d
openshift-kube-scheduler                           Active   468d
openshift-kube-scheduler-operator                  Active   468d
openshift-kube-storage-version-migrator            Active   468d
openshift-kube-storage-version-migrator-operator   Active   468d
openshift-machine-api                              Active   468d
openshift-machine-config-operator                  Active   468d
openshift-marketplace                              Active   468d
openshift-monitoring                               Active   468d
openshift-multus                                   Active   468d
openshift-network-operator                         Active   468d
openshift-node                                     Active   468d
openshift-oauth-apiserver                          Active   468d
openshift-openstack-infra                          Active   468d
openshift-operator-lifecycle-manager               Active   468d
openshift-operators                                Active   468d
openshift-ovirt-infra                              Active   468d
openshift-sdn                                      Active   468d
openshift-service-ca                               Active   468d
openshift-service-ca-operator                      Active   468d
openshift-user-workload-monitoring                 Active   468d
openshift-vsphere-infra                            Active   468d
[student@workstation ~]$ oc get ns | grep test
[student@workstation ~]$ oc create ns test-namespace
namespace/test-namespace created
[student@workstation ~]$ oc adm policy add-role-to-user edit anouk -n test-namespace 
Warning: User &apos;anouk&apos; not found
clusterrole.rbac.authorization.k8s.io/edit added: &quot;anouk&quot;
[student@workstation ~]$ oc adm policy add-role-to-user view anouk -n test-namespace 
Warning: User &apos;anouk&apos; not found
clusterrole.rbac.authorization.k8s.io/view added: &quot;anouk&quot;
[student@workstation ~]$ oc get users
NAME    UID                                    FULL NAME   IDENTITIES
admin   0fd6231d-a13c-4e7a-9589-d0775028d4ed               htpasswd_provider:admin
linda   a6636eae-9e06-4a1e-8260-88e6d9aeadc5               htpasswd_provider:linda
[student@workstation ~]$ 
</pre>
