<h2>Part 1: Create a Key Vault</h2>
<p>1. I began by logging in to the Azure portal and selected "Key vaults":
<br>
</br>

<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2022.png?raw=true" alt="Disk Sanitization Steps"/>


</p>



<p align="center">
2. I selected "+ Create" tab from the Key Vault page to my key vault


: <br>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2023.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br>
3. On the "Create key vault" tab, I made the the following selections:
Subscription/Resource Group: Red Team
<br>
</br>
Key Vault Name: Choose a key vault name, such as project1-KeyVault
<br>
</br>
Region: US East
<br>
</br>
Pricing tier: Select the "Standard" tier.
<br>
</br>
I left the default options for all of the other tabs (Access Policy, Networking, Tags).

<b>
</b>
 <br/> <img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2024.png?raw=true" alt="Disk Sanitization Steps"/>

<br />
<br />
4. I clicked the Access Configuration tab, selected Vault Access Policy, and checked the box next to my username


<br/>

<br />
<br />
5. After my key vault was created, I selected my new resource to view my new key vault.

 <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2025.png?raw=true" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Part 2: Create a Self-Signed Certificate</h2>

1. From my Azure portal, I accessed Cloud Shell. 
  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2019.png?raw=true" alt="Disk Sanitization Steps"/>
<br />
<br />
2. Next, I used OpenSSL to generate a self-signed certificate. A self-signed certificate is a certificate that has not been signed by a certificate authority. From the command line, I enter the following command: openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout <privatekeyname.key> -out <certificatename.crt> -addext "extendedKeyUsage=serverAuth"

:  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2020.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. After pressing Enter I answer the following:


Country Name (2 letter code) [AU]: Enter your country.

State or Province Name (full name) [Some State]: VA.

Locality Name (e.g., city) [ ]: Washington.

Organization Name (e.g., company) [Internet Widgits Pty Ltd]: Student.

Organizational Unit Name (e.g., section) [ ]: Left Blank .

Common Name (e.g., server FQDN or YOUR name) [ ]: Entered my full domain name: "melaisecurityresume.com".

Email Address [ ]: Left Blank.
:  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2021.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

4. To view my newly created key (.key) and certificate (.crt) "ls" into it

5. I created a PFX format, by running the following command: openssl pkcs12 -export -out new_certificatename.pfx -inkey keyname.key -in certificename.crt
  
6. After pressing Enter, I was prompted for a password to encrypt my PFX key. I "ls" back in to see if the PFX certificate was there

: <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2015.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
7. I downloaded my PFX certificate.


  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2026.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Part 3: Analyze a Self-Signed Certificate</h2>

1. From the Azure Portal, I selected “Key Vaults.” From your key vault, I selected “Certificates” and then “+ Generate/Import”



<br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2027.png?raw=true" width="80%" alt="Disk Sanitization Steps"/>
<br />
2. On the “Create a certificate” page, I selected the following:
<br>
</br>

Method of Certificate Creation: Import

Certificate Name: project1PFX-cert

Upload Certificate File: Select your PFX certificate

Password:<br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2028.png?raw=true" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. I selected the “Create” tab to upload my certificate. 
<br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/assets/80586285/dbd9f25c-f4f5-428f-97eb-42c872ab0b2c" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>4. Then I analyze a mock self-signed certificate.

<p>5.  I examine my webpage’s certificate. I clicked on “Not secure” in the search bar. After selecting “Not secure,” I selected “Certificate (Invalid)” from the menu to examine the certificate.
</p>

<h2>Part 4: Analyze a Trusted SSL Certificate</h2>

1. I opened a browser, and I accessed my domain: melaisecuirtyresume@azurewebsites.net.

2. I clicked on the lock icon to analyze my certificate and its details.




</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
