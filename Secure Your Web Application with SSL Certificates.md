<h2>Part 1: Create a Key Vault</h2>
<p>1. Begin by logging in to the Azure portal: https://portal.azure.com. Select "Key vaults" from the Azure search field at the top of the page, as the following image shows:

<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2022.png?raw=true" alt="Disk Sanitization Steps"/>


</p>



<p align="center">
2. Select "+ Create" from the Key Vault page to create your key vault, as the following image shows:


: <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2022.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. On the "Create key vault" tab, make the following selections:
Subscription/Resource Group: Select the same subscription and resource groups that you selected on Day 1.
Key Vault Name: Choose a key vault name, such as project1-KeyVault. (Note: This name must be globally unique, so you will be prompted to choose a different name if the one you enter has been used before.)
Region: Select the same region that you selected on Day 1.
Pricing tier: Select the "Standard" tier.
Leave the default options for all of the other tabs (Access Policy, Networking, Tags).
The following image shows the completed "Create key vault" tab:
 <br/> <img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2021.png?raw=true" alt="Disk Sanitization Steps"/>

<br />
<br />
5. Now, view your newly created key (.key) and certificate (.crt) by running ls, as the following image shows:
: <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2015.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
