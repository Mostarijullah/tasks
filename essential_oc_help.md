
<pre>[student@workstation ~]$ cd tasks/
[student@workstation tasks]$ ls
config.env                                    project_template.md    task2.md  template-by-sidd.yaml
imp_documentation.md                          README.md              task3.md  tolerate_app.yaml
Manage_users__policies_groups_permissions.md  taints_tolerations.md  task4.md  wordpress_example.md
<font color="#0087FF">openssl</font>                                       task1.md               task5.md
[student@workstation tasks]$ oc login -u admin -p redhat
Unable to connect to the server: EOF
[student@workstation tasks]$ cat /usr/local/etc/ocp4.config 
RHT_OCP4_MASTER_API=https://api.ocp4.example.com:6443
RHT_OCP4_WILDCARD_DOMAIN=apps.ocp4.example.com
RHT_OCP4_KUBEADM_PASSWD=waoWn-5S9VM-6cSsy-kMAyk
RHT_OCP4_USER_PASSWD=redhat
[student@workstation tasks]$ oc login -u admin -p redhat https://api.ocp4.example.com:6443
Login successful.

You have access to 65 projects, the list has been suppressed. You can list all projects with &apos; projects&apos;

Using project &quot;wordpress-proj&quot;.
[student@workstation tasks]$ oc 
adm              config           explain          logs             project          secrets
annotate         convert          expose           new-app          projects         serviceaccounts
api-resources    cp               extract          new-build        proxy            set
api-versions     create           get              new-project      registry         start-build
apply            debug            idle             observe          replace          status
attach           delete           image            options          rollback         tag
auth             describe         import-image     patch            rollout          version
autoscale        diff             kustomize        plugin           rsh              wait
cancel-build     edit             label            policy           rsync            whoami
cluster-info     ex               login            port-forward     run              
completion       exec             logout           process          scale            
[student@workstation tasks]$ oc set volumes -h
Update volumes on a pod template

 This command can add, update or remove volumes from containers for any object that has a pod
template (deployment configs, replication controllers, or pods). You can list volumes in pod or any
object that has a pod template. You can specify a single object or multiple, and alter volumes on
all containers or just those that match a given name.

 If you alter a volume setting on a deployment config, a deployment will be triggered. Changing a
replication controller will not affect running pods, and you cannot change a pod&apos;s volumes once it
has been created.

 Volume types include:

  *  emptydir (empty directory) default : A directory allocated when the pod is created on a local
host, is removed when the pod is deleted and is not copied across servers
  *  hostdir (host directory): A directory with specific path on any host (requires elevated
privileges)
  *  persistentvolumeclaim or pvc (persistent volume claim): Link the volume directory in the
container to a persistent volume claim you have allocated by name - a persistent volume claim is a
request to allocate storage. Note that if your claim hasn&apos;t been bound, your pods will not start.
  *  secret (mounted secret): Secret volumes mount a named secret to the provided directory.

 For descriptions on other volume types, see https://docs.openshift.com

Aliases:
volumes, volume

Usage:
  oc set volumes RESOURCE/NAME --add|--remove [flags]

Examples:
  # List volumes defined on all deployment configs in the current project
  oc set volume dc --all
  
  # Add a new empty dir volume to deployment config (dc) &apos;myapp&apos; mounted under
  # /var/lib/myapp
  oc set volume dc/myapp --add --mount-path=/var/lib/myapp
  
  # Use an existing persistent volume claim (pvc) to overwrite an existing volume &apos;v1&apos;
  oc set volume dc/myapp --add --name=v1 -t pvc --claim-name=pvc1 --overwrite
  
  # Remove volume &apos;v1&apos; from deployment config &apos;myapp&apos;
  oc set volume dc/myapp --remove --name=v1
  
  # Create a new persistent volume claim that overwrites an existing volume &apos;v1&apos;
  oc set volume dc/myapp --add --name=v1 -t pvc --claim-size=1G --overwrite
  
  # Change the mount point for volume &apos;v1&apos; to /data
  oc set volume dc/myapp --add --name=v1 -m /data --overwrite
  
  # Modify the deployment config by removing volume mount &quot;v1&quot; from container &quot;c1&quot;
  # (and by removing the volume &quot;v1&quot; if no other containers have volume mounts that reference it)
  oc set volume dc/myapp --remove --name=v1 --containers=c1
  
  # Add new volume based on a more complex volume source (AWS EBS, GCE PD,
  # Ceph, Gluster, NFS, ISCSI, ...)
  oc set volume dc/myapp --add -m /data --source=&lt;json-string&gt;

Options:
      --add=false: If true, add volume and/or volume mounts for containers
      --all=false: If true, select all resources in the namespace of the specified resource types
      --allow-missing-template-keys=true: If true, ignore any errors in templates when a field or
map key is missing in the template. Only applies to golang and jsonpath output formats.
      --claim-class=&apos;&apos;: StorageClass to use for the persistent volume claim
      --claim-mode=&apos;ReadWriteOnce&apos;: Set the access mode of the claim to be created. Valid values are
ReadWriteOnce (rwo), ReadWriteMany (rwm), or ReadOnlyMany (rom)
      --claim-name=&apos;&apos;: Persistent volume claim name. Must be provided for persistentVolumeClaim
volume type
      --claim-size=&apos;&apos;: If specified along with a persistent volume type, create a new claim with the
given size in bytes. Accepts SI notation: 10, 10G, 10Gi
      --configmap-name=&apos;&apos;: Name of the persisted config map. Must be provided for configmap volume
type
      --confirm=false: If true, confirm that you really want to remove multiple volumes
  -c, --containers=&apos;*&apos;: The names of containers in the selected pod templates to change - may use
wildcards
      --default-mode=&apos;&apos;: The default mode bits to create files with. Can be between 0000 and 0777.
Defaults to 0644.
      --dry-run=&apos;none&apos;: Must be &quot;none&quot;, &quot;server&quot;, or &quot;client&quot;. If client strategy, only print the
object that would be sent, without sending it. If server strategy, submit server-side request
without persisting the resource.
  -f, --filename=[]: Filename, directory, or URL to files to use to edit the resource
  -k, --kustomize=&apos;&apos;: Process the kustomization directory. This flag can&apos;t be used together with -f
or -R.
      --local=false: If true, set image will NOT contact api-server but run locally.
  -m, --mount-path=&apos;&apos;: Mount path inside the container. Optional param for --add or --remove
      --name=&apos;&apos;: Name of the volume. If empty, auto generated for add operation
  -o, --output=&apos;&apos;: Output format. One of:
json|yaml|name|go-template|go-template-file|template|templatefile|jsonpath|jsonpath-as-json|jsonpath-file.
      --overwrite=false: If true, replace existing volume source with the provided name and/or
volume mount for the given resource
      --path=&apos;&apos;: Host path. Must be provided for hostPath volume type
      --read-only=false: Mount volume as ReadOnly. Optional param for --add or --remove
  -R, --recursive=false: Process the directory used in -f, --filename recursively. Useful when you
want to manage related manifests organized within the same directory.
      --remove=false: If true, remove volume and/or volume mounts for containers
      --secret-name=&apos;&apos;: Name of the persisted secret. Must be provided for secret volume type
  -l, --selector=&apos;&apos;: Selector (label query) to filter on
      --source=&apos;&apos;: Details of volume source as json string. This can be used if the required volume
type is not supported by --type option. (e.g.: &apos;{&quot;nfs&quot;: {&quot;path&quot;: &quot;/tmp&quot;,&quot;server&quot;:&quot;172.17.0.2&quot;}}&apos;)
      --sub-path=&apos;&apos;: Path within the local volume from which the container&apos;s volume should be
mounted. Optional param for --add or --remove
      --template=&apos;&apos;: Template string or path to template file to use when -o=go-template,
-o=go-template-file. The template format is golang templates
[http://golang.org/pkg/text/template/#pkg-overview].
  -t, --type=&apos;&apos;: Type of the volume source for add operation. Supported options: emptyDir, hostPath,
secret, configmap, persistentVolumeClaim

Use &quot;oc options&quot; for a list of global command-line options (applies to all commands).
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
[student@workstation tasks]$ oc set resources -h
Specify compute resource requirements (cpu, memory) for any resource that defines a pod template. If
a pod is successfully schedualed it is guaranteed the amount of resource requested, but may burst up
to its specified limits.

 For each compute resource, if a limit is specified and a request is omitted, the request will
default to the limit.

 Possible resources include (case insensitive): &quot;ReplicationController&quot;, &quot;Deployment&quot;, &quot;DaemonSet&quot;,
&quot;Job&quot;, &quot;ReplicaSet&quot;, &quot;DeploymentConfigs&quot;

Usage:
  oc set resources (-f FILENAME | TYPE NAME)  ([--limits=LIMITS &amp; --requests=REQUESTS] [flags]

Examples:
  # Set a deployments nginx container cpu limits to &quot;200m and memory to 512Mi&quot;
  
  oc set resources deployment nginx -c=nginx --limits=cpu=200m,memory=512Mi
  
  
  # Set the resource request and limits for all containers in nginx
  
  oc set resources deployment nginx --limits=cpu=200m,memory=512Mi --requests=cpu=100m,memory=256Mi
  
  # Remove the resource requests for resources on containers in nginx
  
  oc set resources deployment nginx --limits=cpu=0,memory=0 --requests=cpu=0,memory=0
  
  # Print the result (in yaml format) of updating nginx container limits from a local, without
hitting the server
  
  oc set resources -f path/to/file.yaml --limits=cpu=200m,memory=512Mi --local -o yaml

Options:
      --all=false: Select all resources, including uninitialized ones, in the namespace of the
specified resource types
      --allow-missing-template-keys=true: If true, ignore any errors in templates when a field or
map key is missing in the template. Only applies to golang and jsonpath output formats.
  -c, --containers=&apos;*&apos;: The names of containers in the selected pod templates to change, all
containers are selected by default - may use wildcards
      --dry-run=&apos;none&apos;: Must be &quot;none&quot;, &quot;server&quot;, or &quot;client&quot;. If client strategy, only print the
object that would be sent, without sending it. If server strategy, submit server-side request
without persisting the resource.
      --field-manager=&apos;kubectl-set&apos;: Name of the manager used to track field ownership.
  -f, --filename=[]: Filename, directory, or URL to files identifying the resource to get from a
server.
  -k, --kustomize=&apos;&apos;: Process the kustomization directory. This flag can&apos;t be used together with -f
or -R.
      --limits=&apos;&apos;: The resource requirement requests for this container.  For example,
&apos;cpu=100m,memory=256Mi&apos;.  Note that server side components may assign requests depending on the
server configuration, such as limit ranges.
      --local=false: If true, set resources will NOT contact api-server but run locally.
  -o, --output=&apos;&apos;: Output format. One of:
json|yaml|name|go-template|go-template-file|template|templatefile|jsonpath|jsonpath-as-json|jsonpath-file.
      --record=false: Record current kubectl command in the resource annotation. If set to false, do
not record the command. If set to true, record the command. If not set, default to updating the
existing annotation value only if one already exists.
  -R, --recursive=false: Process the directory used in -f, --filename recursively. Useful when you
want to manage related manifests organized within the same directory.
      --requests=&apos;&apos;: The resource requirement requests for this container.  For example,
&apos;cpu=100m,memory=256Mi&apos;.  Note that server side components may assign requests depending on the
server configuration, such as limit ranges.
  -l, --selector=&apos;&apos;: Selector (label query) to filter on, not including uninitialized ones,supports
&apos;=&apos;, &apos;==&apos;, and &apos;!=&apos;.(e.g. -l key1=value1,key2=value2)
      --template=&apos;&apos;: Template string or path to template file to use when -o=go-template,
-o=go-template-file. The template format is golang templates
[http://golang.org/pkg/text/template/#pkg-overview].

Use &quot;oc options&quot; for a list of global command-line options (applies to all commands).
[student@workstation tasks]$ oc adm 
build-chain                         create-provider-selection-template  pod-network
catalog                             drain                               policy
certificate                         groups                              prune
completion                          inspect                             release
config                              migrate                             taint
cordon                              must-gather                         top
create-bootstrap-project-template   new-project                         uncordon
create-error-template               node-logs                           upgrade
create-login-template               options                             verify-image-signature
[student@workstation tasks]$ oc adm create-bootstrap-project-template -h
Create a bootstrap project template

Usage:
  oc adm create-bootstrap-project-template [flags]

Options:
      --allow-missing-template-keys=true: If true, ignore any errors in templates when a field or
map key is missing in the template. Only applies to golang and jsonpath output formats.
      --name=&apos;project-request&apos;: The name of the template to output.
  -o, --output=&apos;json&apos;: Output format. One of:
json|yaml|name|go-template|go-template-file|template|templatefile|jsonpath|jsonpath-as-json|jsonpath-file.
      --template=&apos;&apos;: Template string or path to template file to use when -o=go-template,
-o=go-template-file. The template format is golang templates
[http://golang.org/pkg/text/template/#pkg-overview].

Use &quot;oc adm options&quot; for a list of global command-line options (applies to all commands).
[student@workstation tasks]$ oc adm policy -h
Manage policy on the cluster

 These commands allow you to assign and manage the roles and policies that apply to users. The
reconcile commands allow you to reset and upgrade your system policies to the latest default
policies.

 To see more information on roles and policies, use the &apos;get&apos; and &apos;describe&apos; commands on the
following resources: &apos;clusterroles&apos;, &apos;clusterpolicy&apos;, &apos;clusterrolebindings&apos;, &apos;roles&apos;, &apos;policy&apos;,
&apos;rolebindings&apos;, and &apos;scc&apos;.

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
[student@workstation tasks]$ oc create quota -h
Create a resourcequota with the specified name, hard limits and optional scopes

Aliases:
quota, resourcequota

Usage:
  oc create quota NAME [--hard=key1=value1,key2=value2] [--scopes=Scope1,Scope2]
[--dry-run=server|client|none] [flags]

Examples:
  # Create a new resourcequota named my-quota
  oc create quota my-quota
--hard=cpu=1,memory=1G,pods=2,services=3,replicationcontrollers=2,resourcequotas=1,secrets=5,persistentvolumeclaims=10
  
  # Create a new resourcequota named best-effort
  oc create quota best-effort --hard=pods=100 --scopes=BestEffort

Options:
      --allow-missing-template-keys=true: If true, ignore any errors in templates when a field or
map key is missing in the template. Only applies to golang and jsonpath output formats.
      --dry-run=&apos;none&apos;: Must be &quot;none&quot;, &quot;server&quot;, or &quot;client&quot;. If client strategy, only print the
object that would be sent, without sending it. If server strategy, submit server-side request
without persisting the resource.
      --field-manager=&apos;kubectl-create&apos;: Name of the manager used to track field ownership.
      --hard=&apos;&apos;: A comma-delimited set of resource=quantity pairs that define a hard limit.
  -o, --output=&apos;&apos;: Output format. One of:
json|yaml|name|go-template|go-template-file|template|templatefile|jsonpath|jsonpath-as-json|jsonpath-file.
      --save-config=false: If true, the configuration of current object will be saved in its
annotation. Otherwise, the annotation will be unchanged. This flag is useful when you want to
perform kubectl apply on this object in the future.
      --scopes=&apos;&apos;: A comma-delimited set of quota scopes that must all match each object tracked by
the quota.
      --template=&apos;&apos;: Template string or path to template file to use when -o=go-template,
-o=go-template-file. The template format is golang templates
[http://golang.org/pkg/text/template/#pkg-overview].
      --validate=false: If true, use a schema to validate the input before sending it

Use &quot;oc options&quot; for a list of global command-line options (applies to all commands).
[student@workstation tasks]$ oc create secret tls -h
Create a TLS secret from the given public/private key pair.

 The public/private key pair must exist before hand. The public key certificate must be .PEM encoded
and match the given private key.

Usage:
  oc create secret tls NAME --cert=path/to/cert/file --key=path/to/key/file
[--dry-run=server|client|none] [flags]

Examples:
  # Create a new TLS secret named tls-secret with the given key pair:
  oc create secret tls tls-secret --cert=path/to/tls.cert --key=path/to/tls.key

Options:
      --allow-missing-template-keys=true: If true, ignore any errors in templates when a field or
map key is missing in the template. Only applies to golang and jsonpath output formats.
      --append-hash=false: Append a hash of the secret to its name.
      --cert=&apos;&apos;: Path to PEM encoded public key certificate.
      --dry-run=&apos;none&apos;: Must be &quot;none&quot;, &quot;server&quot;, or &quot;client&quot;. If client strategy, only print the
object that would be sent, without sending it. If server strategy, submit server-side request
without persisting the resource.
      --field-manager=&apos;kubectl-create&apos;: Name of the manager used to track field ownership.
      --key=&apos;&apos;: Path to private key associated with given certificate.
  -o, --output=&apos;&apos;: Output format. One of:
json|yaml|name|go-template|go-template-file|template|templatefile|jsonpath|jsonpath-as-json|jsonpath-file.
      --save-config=false: If true, the configuration of current object will be saved in its
annotation. Otherwise, the annotation will be unchanged. This flag is useful when you want to
perform kubectl apply on this object in the future.
      --template=&apos;&apos;: Template string or path to template file to use when -o=go-template,
-o=go-template-file. The template format is golang templates
[http://golang.org/pkg/text/template/#pkg-overview].
      --validate=false: If true, use a schema to validate the input before sending it

Use &quot;oc options&quot; for a list of global command-line options (applies to all commands).
[student@workstation tasks]$ oc create route -h
Expose containers externally via secured routes

 Three types of secured routes are supported: edge, passthrough, and reencrypt. If you wish to
create unsecured routes, see &quot;oc expose -h&quot;

Usage:
  oc create route [flags]

Available Commands:
  edge        Create a route that uses edge TLS termination
  passthrough Create a route that uses passthrough TLS termination
  reencrypt   Create a route that uses reencrypt TLS termination

Use &quot;oc &lt;command&gt; --help&quot; for more information about a given command.
Use &quot;oc options&quot; for a list of global command-line options (applies to all commands).
[student@workstation tasks]$ oc create route passthrough -h
Create a route that uses passthrough TLS termination

 Specify the service (either just its name or using type/name syntax) that the generated route
should expose via the --service flag.

Usage:
  oc create route passthrough [NAME] --service=SERVICE [flags]

Examples:
  # Create a passthrough route named &quot;my-route&quot; that exposes the frontend service.
  oc create route passthrough my-route --service=frontend
  
  # Create a passthrough route that exposes the frontend service and specify
  # a hostname. If the route name is omitted, the service name will be re-used.
  oc create route passthrough --service=frontend --hostname=www.example.com

Options:
      --allow-missing-template-keys=true: If true, ignore any errors in templates when a field or
map key is missing in the template. Only applies to golang and jsonpath output formats.
      --dry-run=&apos;none&apos;: Must be &quot;none&quot;, &quot;server&quot;, or &quot;client&quot;. If client strategy, only print the
object that would be sent, without sending it. If server strategy, submit server-side request
without persisting the resource.
      --hostname=&apos;&apos;: Set a hostname for the new route
      --insecure-policy=&apos;&apos;: Set an insecure policy for the new route
  -o, --output=&apos;&apos;: Output format. One of:
json|yaml|name|go-template|go-template-file|template|templatefile|jsonpath|jsonpath-as-json|jsonpath-file.
      --port=&apos;&apos;: Name of the service port or number of the container port the route will route
traffic to
      --save-config=false: If true, the configuration of current object will be saved in its
annotation. Otherwise, the annotation will be unchanged. This flag is useful when you want to
perform kubectl apply on this object in the future.
      --service=&apos;&apos;: Name of the service that the new route is exposing
      --template=&apos;&apos;: Template string or path to template file to use when -o=go-template,
-o=go-template-file. The template format is golang templates
[http://golang.org/pkg/text/template/#pkg-overview].
      --validate=false: If true, use a schema to validate the input before sending it
      --wildcard-policy=&apos;&apos;: Sets the WilcardPolicy for the hostname, the default is &quot;None&quot;. valid
values are &quot;None&quot; and &quot;Subdomain&quot;

Use &quot;oc options&quot; for a list of global command-line options (applies to all commands).
[student@workstation tasks]$ oc create route edge -h
Create a route that uses edge TLS termination

 Specify the service (either just its name or using type/name syntax) that the generated route
should expose via the --service flag.

Usage:
  oc create route edge [NAME] --service=SERVICE [flags]

Examples:
  # Create an edge route named &quot;my-route&quot; that exposes frontend service.
  oc create route edge my-route --service=frontend
  
  # Create an edge route that exposes the frontend service and specify a path.
  # If the route name is omitted, the service name will be re-used.
  oc create route edge --service=frontend --path /assets

Options:
      --allow-missing-template-keys=true: If true, ignore any errors in templates when a field or
map key is missing in the template. Only applies to golang and jsonpath output formats.
      --ca-cert=&apos;&apos;: Path to a CA certificate file.
      --cert=&apos;&apos;: Path to a certificate file.
      --dry-run=&apos;none&apos;: Must be &quot;none&quot;, &quot;server&quot;, or &quot;client&quot;. If client strategy, only print the
object that would be sent, without sending it. If server strategy, submit server-side request
without persisting the resource.
      --hostname=&apos;&apos;: Set a hostname for the new route
      --insecure-policy=&apos;&apos;: Set an insecure policy for the new route
      --key=&apos;&apos;: Path to a key file.
  -o, --output=&apos;&apos;: Output format. One of:
json|yaml|name|go-template|go-template-file|template|templatefile|jsonpath|jsonpath-as-json|jsonpath-file.
      --path=&apos;&apos;: Path that the router watches to route traffic to the service.
      --port=&apos;&apos;: Name of the service port or number of the container port the route will route
traffic to
      --save-config=false: If true, the configuration of current object will be saved in its
annotation. Otherwise, the annotation will be unchanged. This flag is useful when you want to
perform kubectl apply on this object in the future.
      --service=&apos;&apos;: Name of the service that the new route is exposing
      --template=&apos;&apos;: Template string or path to template file to use when -o=go-template,
-o=go-template-file. The template format is golang templates
[http://golang.org/pkg/text/template/#pkg-overview].
      --validate=false: If true, use a schema to validate the input before sending it
      --wildcard-policy=&apos;&apos;: Sets the WilcardPolicy for the hostname, the default is &quot;None&quot;. valid
values are &quot;None&quot; and &quot;Subdomain&quot;

Use &quot;oc options&quot; for a list of global command-line options (applies to all commands).
[student@workstation tasks]$ oc describe clusterrole.rbac [| grep ^Name]
Error from server (NotFound): clusterroles.rbac.authorization.k8s.io &quot;[&quot; not found
[student@workstation tasks]$ oc describe clusterrole.rbac | grep ^Name
<font color="#EF2929"><b>Name</b></font>:         admin
<font color="#EF2929"><b>Name</b></font>:         aggregate-olm-edit
<font color="#EF2929"><b>Name</b></font>:         aggregate-olm-view
<font color="#EF2929"><b>Name</b></font>:         alertmanager-main
<font color="#EF2929"><b>Name</b></font>:         basic-user
<font color="#EF2929"><b>Name</b></font>:         cloud-credential-operator-role
<font color="#EF2929"><b>Name</b></font>:         cluster-admin
<font color="#EF2929"><b>Name</b></font>:         cluster-autoscaler
<font color="#EF2929"><b>Name</b></font>:         cluster-autoscaler-operator
<font color="#EF2929"><b>Name</b></font>:         cluster-autoscaler-operator:cluster-reader
<font color="#EF2929"><b>Name</b></font>:         cluster-debugger
<font color="#EF2929"><b>Name</b></font>:         cluster-image-registry-operator
<font color="#EF2929"><b>Name</b></font>:         cluster-monitoring-operator
<font color="#EF2929"><b>Name</b></font>:         cluster-monitoring-view
<font color="#EF2929"><b>Name</b></font>:         cluster-node-tuning-operator
<font color="#EF2929"><b>Name</b></font>:         cluster-node-tuning:tuned
<font color="#EF2929"><b>Name</b></font>:         cluster-reader
<font color="#EF2929"><b>Name</b></font>:         cluster-samples-operator
<font color="#EF2929"><b>Name</b></font>:         cluster-samples-operator-proxy-reader
<font color="#EF2929"><b>Name</b></font>:         cluster-status
<font color="#EF2929"><b>Name</b></font>:         console
<font color="#EF2929"><b>Name</b></font>:         console-extensions-reader
<font color="#EF2929"><b>Name</b></font>:         console-operator
<font color="#EF2929"><b>Name</b></font>:         dns-monitoring
<font color="#EF2929"><b>Name</b></font>:         edit
<font color="#EF2929"><b>Name</b></font>:         global-operators-admin
<font color="#EF2929"><b>Name</b></font>:         global-operators-edit
<font color="#EF2929"><b>Name</b></font>:         global-operators-view
<font color="#EF2929"><b>Name</b></font>:         grafana
<font color="#EF2929"><b>Name</b></font>:         helm-chartrepos-viewer
<font color="#EF2929"><b>Name</b></font>:         insights-operator
<font color="#EF2929"><b>Name</b></font>:         insights-operator-gather
<font color="#EF2929"><b>Name</b></font>:         kube-apiserver
<font color="#EF2929"><b>Name</b></font>:         kube-state-metrics
<font color="#EF2929"><b>Name</b></font>:         machine-api-controllers
<font color="#EF2929"><b>Name</b></font>:         machine-api-operator
<font color="#EF2929"><b>Name</b></font>:         machine-api-operator:cluster-reader
<font color="#EF2929"><b>Name</b></font>:         machine-config-controller
<font color="#EF2929"><b>Name</b></font>:         machine-config-controller-events
<font color="#EF2929"><b>Name</b></font>:         machine-config-daemon
<font color="#EF2929"><b>Name</b></font>:         machine-config-daemon-events
<font color="#EF2929"><b>Name</b></font>:         machine-config-server
<font color="#EF2929"><b>Name</b></font>:         marketplace-operator
<font color="#EF2929"><b>Name</b></font>:         metrics-daemon-role
<font color="#EF2929"><b>Name</b></font>:         monitoring-edit
<font color="#EF2929"><b>Name</b></font>:         monitoring-rules-edit
<font color="#EF2929"><b>Name</b></font>:         monitoring-rules-view
<font color="#EF2929"><b>Name</b></font>:         multus
<font color="#EF2929"><b>Name</b></font>:         multus-admission-controller-webhook
<font color="#EF2929"><b>Name</b></font>:         nfs-client-provisioner-runner
<font color="#EF2929"><b>Name</b></font>:         node-exporter
<font color="#EF2929"><b>Name</b></font>:         olm-operators-admin
<font color="#EF2929"><b>Name</b></font>:         olm-operators-edit
<font color="#EF2929"><b>Name</b></font>:         olm-operators-view
<font color="#EF2929"><b>Name</b></font>:         openshift-cluster-monitoring-admin
<font color="#EF2929"><b>Name</b></font>:         openshift-cluster-monitoring-edit
<font color="#EF2929"><b>Name</b></font>:         openshift-cluster-monitoring-view
<font color="#EF2929"><b>Name</b></font>:         openshift-csi-snapshot-controller-runner
<font color="#EF2929"><b>Name</b></font>:         openshift-dns
<font color="#EF2929"><b>Name</b></font>:         openshift-dns-operator
<font color="#EF2929"><b>Name</b></font>:         openshift-ingress-operator
<font color="#EF2929"><b>Name</b></font>:         openshift-ingress-router
<font color="#EF2929"><b>Name</b></font>:         openshift-sdn
<font color="#EF2929"><b>Name</b></font>:         openshift-sdn-controller
<font color="#EF2929"><b>Name</b></font>:         openshift-state-metrics
<font color="#EF2929"><b>Name</b></font>:         operatorhub-config-reader
<font color="#EF2929"><b>Name</b></font>:         packagemanifests-v1-admin
<font color="#EF2929"><b>Name</b></font>:         packagemanifests-v1-edit
<font color="#EF2929"><b>Name</b></font>:         packagemanifests-v1-view
<font color="#EF2929"><b>Name</b></font>:         prometheus-adapter
<font color="#EF2929"><b>Name</b></font>:         prometheus-k8s
<font color="#EF2929"><b>Name</b></font>:         prometheus-operator
<font color="#EF2929"><b>Name</b></font>:         registry-admin
<font color="#EF2929"><b>Name</b></font>:         registry-editor
<font color="#EF2929"><b>Name</b></font>:         registry-monitoring
<font color="#EF2929"><b>Name</b></font>:         registry-viewer
<font color="#EF2929"><b>Name</b></font>:         resource-metrics-server-resources
<font color="#EF2929"><b>Name</b></font>:         router-monitoring
<font color="#EF2929"><b>Name</b></font>:         self-access-reviewer
<font color="#EF2929"><b>Name</b></font>:         self-provisioner
<font color="#EF2929"><b>Name</b></font>:         storage-admin
<font color="#EF2929"><b>Name</b></font>:         sudoer
<font color="#EF2929"><b>Name</b></font>:         system:aggregate-to-admin
<font color="#EF2929"><b>Name</b></font>:         system:aggregate-to-edit
<font color="#EF2929"><b>Name</b></font>:         system:aggregate-to-view
<font color="#EF2929"><b>Name</b></font>:         system:aggregated-metrics-reader
<font color="#EF2929"><b>Name</b></font>:         system:auth-delegator
<font color="#EF2929"><b>Name</b></font>:         system:basic-user
<font color="#EF2929"><b>Name</b></font>:         system:build-strategy-custom
<font color="#EF2929"><b>Name</b></font>:         system:build-strategy-docker
<font color="#EF2929"><b>Name</b></font>:         system:build-strategy-jenkinspipeline
<font color="#EF2929"><b>Name</b></font>:         system:build-strategy-source
<font color="#EF2929"><b>Name</b></font>:         system:certificates.k8s.io:certificatesigningrequests:nodeclient
<font color="#EF2929"><b>Name</b></font>:         system:certificates.k8s.io:certificatesigningrequests:selfnodeclient
<font color="#EF2929"><b>Name</b></font>:         system:certificates.k8s.io:kube-apiserver-client-approver
<font color="#EF2929"><b>Name</b></font>:         system:certificates.k8s.io:kube-apiserver-client-kubelet-approver
<font color="#EF2929"><b>Name</b></font>:         system:certificates.k8s.io:kubelet-serving-approver
<font color="#EF2929"><b>Name</b></font>:         system:certificates.k8s.io:legacy-unknown-approver
<font color="#EF2929"><b>Name</b></font>:         system:controller:attachdetach-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:certificate-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:clusterrole-aggregation-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:cronjob-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:daemon-set-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:deployment-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:disruption-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:endpoint-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:endpointslice-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:endpointslicemirroring-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:expand-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:generic-garbage-collector
<font color="#EF2929"><b>Name</b></font>:         system:controller:horizontal-pod-autoscaler
<font color="#EF2929"><b>Name</b></font>:         system:controller:job-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:namespace-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:node-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:operator-lifecycle-manager
<font color="#EF2929"><b>Name</b></font>:         system:controller:persistent-volume-binder
<font color="#EF2929"><b>Name</b></font>:         system:controller:pod-garbage-collector
<font color="#EF2929"><b>Name</b></font>:         system:controller:pv-protection-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:pvc-protection-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:replicaset-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:replication-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:resourcequota-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:route-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:service-account-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:service-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:statefulset-controller
<font color="#EF2929"><b>Name</b></font>:         system:controller:ttl-controller
<font color="#EF2929"><b>Name</b></font>:         system:deployer
<font color="#EF2929"><b>Name</b></font>:         system:discovery
<font color="#EF2929"><b>Name</b></font>:         system:heapster
<font color="#EF2929"><b>Name</b></font>:         system:image-auditor
<font color="#EF2929"><b>Name</b></font>:         system:image-builder
<font color="#EF2929"><b>Name</b></font>:         system:image-pruner
<font color="#EF2929"><b>Name</b></font>:         system:image-puller
<font color="#EF2929"><b>Name</b></font>:         system:image-pusher
<font color="#EF2929"><b>Name</b></font>:         system:image-signer
<font color="#EF2929"><b>Name</b></font>:         system:kube-aggregator
<font color="#EF2929"><b>Name</b></font>:         system:kube-controller-manager
<font color="#EF2929"><b>Name</b></font>:         system:kube-dns
<font color="#EF2929"><b>Name</b></font>:         system:kube-scheduler
<font color="#EF2929"><b>Name</b></font>:         system:kubelet-api-admin
<font color="#EF2929"><b>Name</b></font>:         system:master
<font color="#EF2929"><b>Name</b></font>:         system:node
<font color="#EF2929"><b>Name</b></font>:         system:node-admin
<font color="#EF2929"><b>Name</b></font>:         system:node-bootstrapper
<font color="#EF2929"><b>Name</b></font>:         system:node-problem-detector
<font color="#EF2929"><b>Name</b></font>:         system:node-proxier
<font color="#EF2929"><b>Name</b></font>:         system:node-reader
<font color="#EF2929"><b>Name</b></font>:         system:oauth-token-deleter
<font color="#EF2929"><b>Name</b></font>:         system:openshift:aggregate-snapshots-to-admin
<font color="#EF2929"><b>Name</b></font>:         system:openshift:aggregate-snapshots-to-basic-user
<font color="#EF2929"><b>Name</b></font>:         system:openshift:aggregate-snapshots-to-storage-admin
<font color="#EF2929"><b>Name</b></font>:         system:openshift:aggregate-snapshots-to-view
<font color="#EF2929"><b>Name</b></font>:         system:openshift:aggregate-to-admin
<font color="#EF2929"><b>Name</b></font>:         system:openshift:aggregate-to-basic-user
<font color="#EF2929"><b>Name</b></font>:         system:openshift:aggregate-to-cluster-reader
<font color="#EF2929"><b>Name</b></font>:         system:openshift:aggregate-to-edit
<font color="#EF2929"><b>Name</b></font>:         system:openshift:aggregate-to-storage-admin
<font color="#EF2929"><b>Name</b></font>:         system:openshift:aggregate-to-view
<font color="#EF2929"><b>Name</b></font>:         system:openshift:cloud-credential-operator:cluster-reader
<font color="#EF2929"><b>Name</b></font>:         system:openshift:cluster-config-operator:cluster-reader
<font color="#EF2929"><b>Name</b></font>:         system:openshift:cluster-samples-operator:cluster-reader
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:build-config-change-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:build-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:check-endpoints
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:check-endpoints-crd-reader
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:check-endpoints-node-reader
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:cluster-quota-reconciliation-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:default-rolebindings-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:deployer-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:deploymentconfig-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:horizontal-pod-autoscaler
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:image-import-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:image-trigger-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:machine-approver
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:namespace-security-allocation-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:origin-namespace-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:pv-recycler-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:resourcequota-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:service-ca
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:service-ingress-ip-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:service-serving-cert-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:serviceaccount-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:serviceaccount-pull-secrets-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:template-instance-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:template-instance-finalizer-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:template-service-broker
<font color="#EF2929"><b>Name</b></font>:         system:openshift:controller:unidling-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:discovery
<font color="#EF2929"><b>Name</b></font>:         system:openshift:kube-controller-manager:gce-cloud-provider
<font color="#EF2929"><b>Name</b></font>:         system:openshift:machine-config-operator:cluster-reader
<font color="#EF2929"><b>Name</b></font>:         system:openshift:openshift-controller-manager
<font color="#EF2929"><b>Name</b></font>:         system:openshift:openshift-controller-manager:ingress-to-route-controller
<font color="#EF2929"><b>Name</b></font>:         system:openshift:public-info-viewer
<font color="#EF2929"><b>Name</b></font>:         system:openshift:scc:anyuid
<font color="#EF2929"><b>Name</b></font>:         system:openshift:scc:hostaccess
<font color="#EF2929"><b>Name</b></font>:         system:openshift:scc:hostmount
<font color="#EF2929"><b>Name</b></font>:         system:openshift:scc:hostmount-anyuid
<font color="#EF2929"><b>Name</b></font>:         system:openshift:scc:hostnetwork
<font color="#EF2929"><b>Name</b></font>:         system:openshift:scc:nonroot
<font color="#EF2929"><b>Name</b></font>:         system:openshift:scc:privileged
<font color="#EF2929"><b>Name</b></font>:         system:openshift:scc:restricted
<font color="#EF2929"><b>Name</b></font>:         system:openshift:templateservicebroker-client
<font color="#EF2929"><b>Name</b></font>:         system:openshift:tokenreview-openshift-controller-manager
<font color="#EF2929"><b>Name</b></font>:         system:persistent-volume-provisioner
<font color="#EF2929"><b>Name</b></font>:         system:public-info-viewer
<font color="#EF2929"><b>Name</b></font>:         system:registry
<font color="#EF2929"><b>Name</b></font>:         system:router
<font color="#EF2929"><b>Name</b></font>:         system:scope-impersonation
<font color="#EF2929"><b>Name</b></font>:         system:sdn-manager
<font color="#EF2929"><b>Name</b></font>:         system:sdn-reader
<font color="#EF2929"><b>Name</b></font>:         system:volume-scheduler
<font color="#EF2929"><b>Name</b></font>:         system:webhook
<font color="#EF2929"><b>Name</b></font>:         thanos-querier
<font color="#EF2929"><b>Name</b></font>:         view
<font color="#EF2929"><b>Name</b></font>:         whereabouts-cni
[student@workstation tasks]$ 
</pre>

