Spring Boot with HTTPS

Command to create self signed SSL Certificate JKS

Note : Missed to include Subject Alternate Name in the certificate

keytool -genkey -alias spring-boot-https-example -storetype JKS -keyalg RSA -keysize 2048 -validity 365 -keystore https-example.jks

keytool -list -v -keystore https-example.jks


keytool -importkeystore -srckeystore https-example.jks -destkeystore https-example.p12 -srcstoretype JKS -deststoretype PKCS12 -srcstorepass password -deststorepass password -srcalias spring-boot-https-example -destalias spring-boot-https-example_p12 -srckeypass password -destkeypass password -noprompt



Step 1: Open MMC on the machine that you are getting the warning
Click on Start -> Run -> type MMC -> Click OK

Step 2: Click on File -> Add/Remove Snap-in...

Step 3: Click on Certificates -> Add>

Step 4: Click on User Account -> Finish

Then Click OK

Step 5: Expand Certificates -> Trusted Root Certification Authority -> Certificates

Right click on the right pane -> All Tasks -> Import

Step 6: Go through the Import Wizard

Browse to the certificate file, Click Next, Select Trusted Root Certification Authorities, Click Next, then Finish.

Click yes on the Security Warning.