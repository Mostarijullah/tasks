<pre>

[student@workstation tasks]$ 
[student@workstation tasks]$ man openssl-x509
[student@workstation tasks]$ 
[student@workstation tasks]$ man openssl-x509 | less
[student@workstation tasks]$ 
[student@workstation tasks]$ man openssl-req | less
[student@workstation tasks]$ ls
config.env                                    <font color="#0087FF">openssl</font>                task1.md  task5.md
essential_oc_help.md                          project_template.md    task2.md  template-by-sidd.yaml
imp_documentation.md                          README.md              task3.md  tolerate_app.yaml
Manage_users__policies_groups_permissions.md  taints_tolerations.md  task4.md  wordpress_example.md
[student@workstation tasks]$ mkdir openssl-05112022
[student@workstation tasks]$ cd openssl-05112022/
[student@workstation openssl-05112022]$ openssl -h
Invalid command &apos;-h&apos;; type &quot;help&quot; for a list.
[student@workstation openssl-05112022]$ openssl --help
Invalid command &apos;--help&apos;; type &quot;help&quot; for a list.
[student@workstation openssl-05112022]$ openssl gen
gendh   gendsa  genrsa  
[student@workstation openssl-05112022]$ openssl gen
gendh   gendsa  genrsa  
[student@workstation openssl-05112022]$ openssl genrsa -des3 
Generating RSA private key, 2048 bit long modulus (2 primes)
........................................+++++
...............................................+++++
e is 65537 (0x010001)
Enter pass phrase:
140206311089984:error:28078065:UI routines:UI_set_result_ex:result too small:crypto/ui/ui_lib.c:903:You must type in 4 to 1023 characters
Enter pass phrase:
140206311089984:error:2807106B:UI routines:UI_process:processing error:crypto/ui/ui_lib.c:543:while reading strings
Enter pass phrase:
140206311089984:error:28078065:UI routines:UI_set_result_ex:result too small:crypto/ui/ui_lib.c:903:You must type in 4 to 1023 characters
Enter pass phrase:
140206311089984:error:2807106B:UI routines:UI_process:processing error:crypto/ui/ui_lib.c:543:while reading strings
Enter pass phrase:
Verifying - Enter pass phrase:
Verify failure
User interface error
140206311089984:error:28078065:UI routines:UI_set_result_ex:result too small:crypto/ui/ui_lib.c:903:You must type in 4 to 1023 characters
140206311089984:error:2807106B:UI routines:UI_process:processing error:crypto/ui/ui_lib.c:543:while reading strings
140206311089984:error:28078065:UI routines:UI_set_result_ex:result too small:crypto/ui/ui_lib.c:903:You must type in 4 to 1023 characters
140206311089984:error:2807106B:UI routines:UI_process:processing error:crypto/ui/ui_lib.c:543:while reading strings
140206311089984:error:2807106B:UI routines:UI_process:processing error:crypto/ui/ui_lib.c:543:while reading strings
140206311089984:error:0906906F:PEM routines:PEM_ASN1_write_bio:read key:crypto/pem/pem_lib.c:357:
[student@workstation openssl-05112022]$ openssl genrsa -des3 -out myCA.key 2048
Generating RSA private key, 2048 bit long modulus (2 primes)
..................+++++
................................................+++++
e is 65537 (0x010001)
Enter pass phrase for myCA.key:
Verifying - Enter pass phrase for myCA.key:
[student@workstation openssl-05112022]$ ls
myCA.key
[student@workstation openssl-05112022]$ openssl genrsa -des3 -out myCA.key 2048
Generating RSA private key, 2048 bit long modulus (2 primes)
........................+++++
..........................+++++
e is 65537 (0x010001)
Enter pass phrase for myCA.key:
Verifying - Enter pass phrase for myCA.key:
[student@workstation openssl-05112022]$ openssl r
rand        rc2-40-cbc  rc2-cbc     rc2-ecb     rc4         req         rsa         
rc2         rc2-64-cbc  rc2-cfb     rc2-ofb     rc4-40      rmd160      rsautl      
[student@workstation openssl-05112022]$ openssl req -x509 -new -nodes -key myCA.key -sha256 -days 3650 -out myCA.pem
Enter pass phrase for myCA.key:
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter &apos;.&apos;, the field will be left blank.
-----
Country Name (2 letter code) [XX]:
State or Province Name (full name) []:
Locality Name (eg, city) [Default City]:
Organization Name (eg, company) [Default Company Ltd]:
Organizational Unit Name (eg, section) []:
Common Name (eg, your name or your server&apos;s hostname) []:apps.ocp4.example.com^[[D^[[D^[[D^[[D^[[D^[[D^[[D^[[D^[                              
Email Address []:
[student@workstation openssl-05112022]$ openssl req -x509 -new -nodes -key myCA.key -sha256 -days 3650 -out myCA.pem
Enter pass phrase for myCA.key:
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter &apos;.&apos;, the field will be left blank.
-----
Country Name (2 letter code) [XX]:
State or Province Name (full name) []:
Locality Name (eg, city) [Default City]:
Organization Name (eg, company) [Default Company Ltd]:
Organizational Unit Name (eg, section) []:
Common Name (eg, your name or your server&apos;s hostname) []:apps.ocp4.example.com
Email Address []:
[student@workstation openssl-05112022]$ ls
myCA.key  myCA.pem
[student@workstation openssl-05112022]$ openssl gen
gendh   gendsa  genrsa  
[student@workstation openssl-05112022]$ openssl gen
gendh   gendsa  genrsa  
[student@workstation openssl-05112022]$ openssl genrsa -out tls.key 2048
Generating RSA private key, 2048 bit long modulus (2 primes)
...+++++
............................+++++
e is 65537 (0x010001)
[student@workstation openssl-05112022]$ openssl req -new -key tls.key -out tls.csr
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter &apos;.&apos;, the field will be left blank.
-----
Country Name (2 letter code) [XX]:
State or Province Name (full name) []:
Locality Name (eg, city) [Default City]:
Organization Name (eg, company) [Default Company Ltd]:
Organizational Unit Name (eg, section) []:
Common Name (eg, your name or your server&apos;s hostname) []:apps.ocp4.example.com
Email Address []:

Please enter the following &apos;extra&apos; attributes
to be sent with your certificate request
A challenge password []:ex280
An optional company name []:
[student@workstation openssl-05112022]$ openssl 
aes-128-cbc       camellia-192-ecb  des-ede           enc               rc2               sha224
aes-128-ecb       camellia-256-cbc  des-ede3          engine            rc2-40-cbc        sha256
aes-192-cbc       camellia-256-ecb  des-ede3-cbc      errstr            rc2-64-cbc        sha384
aes-192-ecb       cast              des-ede3-cfb      gendh             rc2-cbc           sha512
aes-256-cbc       cast5-cbc         des-ede3-ofb      gendsa            rc2-cfb           smime
aes-256-ecb       cast5-cfb         des-ede-cbc       genrsa            rc2-ecb           speed
asn1parse         cast5-ecb         des-ede-cfb       md2               rc2-ofb           spkac
base64            cast5-ofb         des-ede-ofb       md4               rc4               s_server
bf                cast-cbc          des-ofb           md5               rc4-40            s_time
bf-cbc            ciphers           desx              nseq              req               verify
bf-cfb            crl               dgst              ocsp              rmd160            version
bf-ecb            crl2pkcs7         dh                passwd            rsa               x509
bf-ofb            des               dhparam           pkcs12            rsautl            
ca                des3              dsa               pkcs7             s_client          
camellia-128-cbc  des-cbc           dsaparam          pkcs8             sess_id           
camellia-128-ecb  des-cfb           ec                prime             sha               
camellia-192-cbc  des-ecb           ecparam           rand              sha1              
[student@workstation openssl-05112022]$ openssl x509 -req -in tls.csr -CA myCA.pem -CAkey myCA.key -CAcreateserial -out tls.crt -days 3650 -sha256
Signature ok
subject=C = XX, L = Default City, O = Default Company Ltd, CN = apps.ocp4.example.com
Getting CA Private Key
Enter pass phrase for myCA.key:
[student@workstation openssl-05112022]$ ls
myCA.key  myCA.pem  myCA.srl  tls.crt  tls.csr  tls.key
[student@workstation openssl-05112022]$ 
</pre>




openssl genrsa -des3 -out myCA.key 2048

openssl req -x509 -new -nodes -key myCA.key -sha256 -days 3650 -out myCA.pem

openssl genrsa -out tls.key 2048

openssl req -new -key tls.key -out tls.csr

openssl x509 -req -in tls.csr -CA myCA.pem -CAkey myCA.key -CAcreateserial -out tls.crt -days 1650 -sha256



Use myCA.key and myCA.pem for the CA, 

and 

use tls.key, tls.csr and tls.crt for the application

1: man openssl-req: "Generate a self-signed root cert"

2: man openssl-req: "Create a private key and generate a certificate request from it"

3: man openssl-x509: "Sign a certificate request using the ... certificate extensions"




Create a private key and then generate a certificate request from it:

        openssl genrsa -out key.pem 2048
        openssl req -new -key key.pem -out req.pem


 Generate a self signed root certificate:

        openssl req -x509 -newkey rsa:2048 -keyout key.pem -out req.pem


 Sign a certificate request using the CA certificate above and add user certificate extensions:

        openssl x509 -req -in req.pem -extfile openssl.cnf -extensions v3_usr \
               -CA cacert.pem -CAkey key.pem -CAcreateserial

[student@workstation tasks]$ man openssl-req
[student@workstation tasks]$ man opens
openssl/           openssl-dgst       openssl-genrsa     openssl-prime      openssl-srp
openssl/           openssl-dhparam    openssl-list       openssl-rand       openssl-s_server
openssl-05112022/  openssl-dsa        openssl-nseq       openssl-rehash     openssl-s_time
openssl-asn1parse  openssl-dsaparam   openssl-ocsp       openssl-req        openssl-storeutl
openssl-ca         openssl-ec         openssl-passwd     openssl-rsa        openssl-ts
openssl-ciphers    openssl-ecparam    openssl-pkcs12     openssl-rsautl     openssl-verify
openssl-cms        openssl-enc        openssl-pkcs7      openssl-s_client   openssl-version
openssl.cnf        openssl-engine     openssl-pkcs8      openssl-sess_id    openssl-x509
openssl-c_rehash   openssl-errstr     openssl-pkey       openssl-smime      
openssl-crl        openssl-gendsa     openssl-pkeyparam  openssl-speed      
openssl-crl2pkcs7  openssl-genpkey    openssl-pkeyutl    openssl-spkac    

