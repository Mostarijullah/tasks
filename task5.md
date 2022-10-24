<pre>[student@workstation tasks]$ 

Committer: Student User &lt;student@workstation.lab.example.com&gt;
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name &quot;Your Name&quot;
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author


[student@workstation tasks]$ mkdir openssl
[student@workstation tasks]$ cd openssl/
[student@workstation openssl]$ clear

[student@workstation openssl]$ openssl genrsa -des3 -out myCA.key 2048
Generating RSA private key, 2048 bit long modulus (2 primes)
........................................................................................+++++
.............................................+++++
e is 65537 (0x010001)
Enter pass phrase for myCA.key:
Verifying - Enter pass phrase for myCA.key:
[student@workstation openssl]$ openssl req --x509 --new --nodes --key myCA.key --sha256 --days 3650 --out myCA.pem
Enter pass phrase for myCA.key:
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter &apos;.&apos;, the field will be left blank.
-----
Country Name (2 letter code) [XX]:IN
State or Province Name (full name) []:West Bengal
Locality Name (eg, city) [Default City]:Kolkata
Organization Name (eg, company) [Default Company Ltd]:RH Training Pvt Ltd
Organizational Unit Name (eg, section) []:Global Training 
Common Name (eg, your name or your server&apos;s hostname) []:ex280
Email Address []:student@redhat.com
[student@workstation openssl]$ openssl genrsa -out tls.key 2048
Generating RSA private key, 2048 bit long modulus (2 primes)
.............................+++++
..+++++
e is 65537 (0x010001)
[student@workstation openssl]$ openssl req --new --key tls.key --out tls.csr
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter &apos;.&apos;, the field will be left blank.
-----
Country Name (2 letter code) [XX]:IN
State or Province Name (full name) []:West Bengal
Locality Name (eg, city) [Default City]:Kolkata
Organization Name (eg, company) [Default Company Ltd]:RH Training Pvt Ltd
Organizational Unit Name (eg, section) []:Global Training 
Common Name (eg, your name or your server&apos;s hostname) []:ex280
Email Address []:student@redhat.com

Please enter the following &apos;extra&apos; attributes
to be sent with your certificate request
A challenge password []:ex280
An optional company name []:RT 
[student@workstation openssl]$ openssl x509 --req --in tls.csr --CA myCA.pem --CAkey myCA.key --CAcreateserial --out tls.crt --days 1650 --sha256
Signature ok
subject=C = IN, ST = West Bengal, L = Kolkata, O = RH Training Pvt Ltd, OU = &quot;Global Training &quot;, CN = ex280, emailAddress = student@redhat.com
Getting CA Private Key
Enter pass phrase for myCA.key:
[student@workstation openssl]$ oc project
Using project &quot;local-project&quot; on server &quot;https://api.ocp4.example.com:6443&quot;.
[student@workstation openssl]$ ls
myCA.key  myCA.pem  myCA.srl  tls.crt  tls.csr  tls.key
[student@workstation openssl]$ oc new-project ex280
Now using project &quot;ex280&quot; on server &quot;https://api.ocp4.example.com:6443&quot;.

You can add applications to this project with the &apos;new-app&apos; command. For example, try:

    oc new-app rails-postgresql-example

to build a new example application in Ruby. Or use kubectl to deploy a simple Kubernetes application:

    kubectl create deployment hello-node --image=k8s.gcr.io/serve_hostname

[student@workstation openssl]$ oc new-app --docker-image=sandervanvugt/openshift:latest --name ex280
--&gt; Found container image 2a1b082 (2 years old) from Docker Hub for &quot;sandervanvugt/openshift:latest&quot;

    Red Hat Universal Base Image 8 
    ------------------------------ 
    The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly.

    Tags: base rhel8

    * An image stream tag will be created as &quot;ex280:latest&quot; that will track this image

--&gt; Creating resources ...
    imagestream.image.openshift.io &quot;ex280&quot; created
    deployment.apps &quot;ex280&quot; created
    service &quot;ex280&quot; created
--&gt; Success
    Application is not exposed. You can expose services to the outside world by executing one or more of the commands below:
     &apos;oc expose service/ex280&apos; 
    Run &apos;oc status&apos; to view your app.
[student@workstation openssl]$ oc get pods
NAME                     READY   STATUS              RESTARTS   AGE
ex280-59cb457977-p7dhc   0/1     ContainerCreating   0          13s
[student@workstation openssl]$ watch oc get pods
[student@workstation openssl]$ oc logs ex280-59cb457977-p7dhc 
nginx: [warn] the &quot;user&quot; directive makes sense only if the master process runs with super-user privileges, ignored in /etc/nginx/nginx.conf:5
nginx: [emerg] BIO_new_file(&quot;/run/secrets/nginx/tls.crt&quot;) failed (SSL: error:02001002:system library:fopen:No such file or directory:fopen(&apos;/run/secrets/nginx/tls.crt&apos;,&apos;r&apos;) error:2006D080:BIO routines:BIO_new_file:no such file)
[student@workstation openssl]$ oc create secret tls ex280-tls --cert tls.crt --key tls.key 
secret/ex280-tls created
[student@workstation openssl]$ oc set volumes deployment/ex280 --add --type secret --secret-name ex280-tls --mount-path /run/se
sepermit/       setrans/        setroubleshoot/ 
[student@workstation openssl]$ oc set volumes deployment/ex280 --add --type secret --secret-name ex280-tls --mount-path /run/secrets/nginx
info: Generated volume name: volume-xrfth
deployment.apps/ex280 volume updated
[student@workstation openssl]$ watch oc get pods
[student@workstation openssl]$ oc get pods
NAME                     READY   STATUS    RESTARTS   AGE
ex280-6c69d4ccc7-4cchc   1/1     Running   0          61s
[student@workstation openssl]$ 
</pre>
