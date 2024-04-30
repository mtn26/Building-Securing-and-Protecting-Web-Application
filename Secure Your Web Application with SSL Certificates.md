<h2>Part 1: Create a Key Vault</h2>
<p>1. Begin by logging in to the Azure portal: https://portal.azure.com. Select "Key vaults" from the Azure search field at the top of the page, as the following image shows:
<br>
</br>

<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2022.png?raw=true" alt="Disk Sanitization Steps"/>


</p>



<p align="center">
2. Select "+ Create" from the Key Vault page to create your key vault, as the following image shows:


: <br>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2023.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br>
3. On the "Create key vault" tab, make the following selections:
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
Leave the default options for all of the other tabs (Access Policy, Networking, Tags).
The following image shows the completed "Create key vault" tab:
<b>
</b>
 <br/> <img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2024.png?raw=true" alt="Disk Sanitization Steps"/>

<br />
<br />
4. Click next to the Access Configuration Tab
Select Vault Access Policy
Check the box next to your username
Click Review + Create

<br/>

<br />
<br />
5. After your key vault has been created, select your new resource to view your new key vault.
Preview the options available on your key vault to store secure information, including:
Keys
Secrets
Certificates
The following image shows these options:
 <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2025.png?raw=true" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Part 2: Create a Self-Signed Certificate</h2>

1. From your Azure portal, access the same Cloud Shell that you accessed on Day 1 to load the Docker container, as the following image shows:
  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2019.png?raw=true" alt="Disk Sanitization Steps"/>
<br />
<br />
2. Next, you will use OpenSSL to generate a self-signed certificate. A self-signed certificate is a certificate that has not been signed by a certificate authority. From the command line, enter the following command: openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout <privatekeyname.key> -out <certificatename.crt> -addext "extendedKeyUsage=serverAuth"

:  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2020.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. After pressing Enter, you will be asked several questions about your certificate. Answer the following:


Country Name (2 letter code) [AU]: Enter your country.

State or Province Name (full name) [Some State]: Enter your state.

Locality Name (e.g., city) [ ]: Enter your city.

Organization Name (e.g., company) [Internet Widgits Pty Ltd]: Enter "Student".

Organizational Unit Name (e.g., section) [ ]: Leave blank by pressing Enter.

Common Name (e.g., server FQDN or YOUR name) [ ]: Enter your full domain name, such as "melaisecurityresume.com".

Email Address [ ]: Leave blank by pressing Enter.
:  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2021.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
