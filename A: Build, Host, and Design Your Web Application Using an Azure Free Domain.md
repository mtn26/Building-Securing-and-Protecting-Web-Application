<h2>Creating the Web Application: Part 1</h2>

<p align="center">
1. I selected "App Services" from the Azure search field at the top of the page, as the following image shows<br/>
 <img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/assets/80586285/8de510ac-c455-44d8-8ba8-11fe520ce439" alt="Resume Github P1 pic 1"/>
<br />
<br />
2. I clicked on Select "+ Create" to create my application<br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/assets/80586285/bc04b829-5480-4cdf-bad0-d7aab6786e87" alt="Resume Pic"/>
<br />
<br />
3. I clicked the "Basics" tab, to make the following selections:

 Subscription/Resource group: Select the same subscription and resource group.

Name: "melaisecurityresume"

Publish: Select "Code."

Runtime stack: Select "PHP 8.2."

Operating system: Select "Linux."

Region: US East.

<br/>
<img src="https://github.com/mtn26/Securing-Web-Application/blob/main/Resume%20Project%201%20pic%203.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />  
4. For the App Service Plan, I completed the following steps:


Under "Linux Plan," select "Create New" and then enter "project1plan."


Under "Sku and size," select "Change size."


The spec picker will pop up on the right-hand side of your screen.


Note that this allows you to choose the pricing structure of your web app.


Select "Dev/Test" and "Plan B1" (the green option), and then click "Apply," as the following image shows:


:  <br/>
<img src="https://github.com/mtn26/Securing-Web-Application/blob/main/Resume%20Project%201%20pic%204.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
5. I left the default options for all of the other tabs and selected the "Review + Create" tab.

I selected the "Create" tab at the bottom of the screen to create your web app.

Once the app was created, I selected "Go to Resource".

  <br/>
<img src="https://github.com/mtn26/Securing-Web-Application/blob/main/Resume%20Project%201%20pic%205.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
6. After selecting my app, a menu appeared on the left-hand side of my app.  I selected the "Custom domains" tab. Once the new page opened, my IP was created </br>
<img src="https://github.com/mtn26/Securing-Web-Application/blob/main/Resume%20Project%201%20pic%206.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 7. Upon the creation of my app, Azure provided me with a free domain.
It begins with the name that you selected and ends with ".azurewebsites.net"<br/>
</p>

<h2>Deploy a Container on the Web App: Part 2</h2>

<p align="center">
1. For my web application, I used a Docker container that has been added to Docker Hub. 
 : <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%207.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
2. I used the Azure Cloud Shell to deploy the container to my web application  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%208.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. From the command line, I enter the command to configure my container. These are the 3 commands I used:


az webapp config container delete - This will delete your web app container's settings.


az webapp config container set - This will set your web app container's settings.


az webapp config container show - This will display the current details of your web app container's settings.




I configured my web app with my container and ran the following: az webapp config container set --name <name of your webapp> --resource-group <name of your resource group> --docker-custom-image-name <container-name> --enable-app-service-storage -t. <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%209.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
4. I verified that my container was added correctly and ran the following command to show my container for my web app: az webapp config container show --name <name of webapp> --resource-group <name of your resource group>. <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2016.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Design Your Custom Web Application: Part 3</h2>

1. Once my container was applied to my web app I began to customize my web app. I accessed the pages of my web app, using SSH over to my container, and accessed the HTML files. 
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2017.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
   2. Once I had access I changed directories to the location where the HTML files are located by running cd /var/www/html <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2018.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
   
<p>3. I nanoed into the index.html files and started making changes. These are the results after changes have been made in the index.html file.</p>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2010.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/assets/80586285/04c34c3c-8b25-4316-a456-c5c249558a73" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2012.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>



<p>4. After each update to my webpage, I made sure to back up the index.html file to the /home directory with the following command:

cp /var/www/html/index.html /home
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
