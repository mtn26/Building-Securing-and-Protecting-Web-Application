<h2>Creating the Web Application: Part 1</h2>

<p align="center">
1. First you select "App Services" from the Azure search field at the top of the page, as the following image shows<br/>
 <img src="https://github.com/mtn26/Securing-Web-Application/blob/main/Resume%20Github%20P1%20pic%201.PNG?raw=true" alt="Resume Github P1 pic 1"/>
<br />
<br />
2. Select "+ Create" to create your application, as the following image shows:<br/>
<img src="https://github.com/mtn26/Securing-Web-Application/blob/main/Resume%20Github%20P1%20pic%202.PNG?raw=true" height="80%" width="80%" alt="Resume Pic"/>
<br />
<br />
3. Under the "Basics" tab, make the following selections:

 Subscription/Resource group: Select the same subscription and resource group.

Name: "melaisecurityresume"

Publish: Select "Code."

Runtime stack: Select "PHP 8.2."

Operating system: Select "Linux."

Region: US East.

The following image shows the completed "Basics" tab:: <br/>
<img src="https://github.com/mtn26/Securing-Web-Application/blob/main/Resume%20Project%201%20pic%203.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />  
4. For the App Service Plan, complete the following steps:


Under "Linux Plan," select "Create New" and then enter "project1plan."


Under "Sku and size," select "Change size."


The spec picker will pop up on the right-hand side of your screen.


Note that this allows you to choose the pricing structure of your web app.


Select "Dev/Test" and "Plan B1" (the green option), and then click "Apply," as the following image shows:


:  <br/>
<img src="https://github.com/mtn26/Securing-Web-Application/blob/main/Resume%20Project%201%20pic%204.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
5. Leave the default options for all of the other tabs. Select the "Review + Create" tab.

Select "Create" at the bottom of the screen to create your web app.

Once your app has been created, either select "Go to Resource" or find the app that you just created by selecting "App Services" from the Azure search field at the top of the page.

The app that you just created should now appear on the list.

Select your app from this page, as the following image shows:  <br/>
<img src="https://github.com/mtn26/Securing-Web-Application/blob/main/Resume%20Project%201%20pic%205.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
6. After selecting your app, a menu of available options should appear on the left-hand side of your app. Select "Custom domains" Once this new page opens, note that your unique IP has been created, as the following image shows:  </br>
<img src="https://github.com/mtn26/Securing-Web-Application/blob/main/Resume%20Project%201%20pic%206.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 7. Upon the creation of this app, Azure provides you with a free domain.
It begins with the name that you selected and ends with ".azurewebsites.net"<br/>
</p>

<h2>Deploy a Container on the Web App: Part 2</h2>

<p align="center">
1. For your web application, you will use a Docker container that has been added to Docker Hub. Note that the Docker container image name is cyberxsecurity/project1-apachewebserver, as the following image shows:
 : <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%207.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
2. Next, you will use the Azure Cloud Shell to deploy this container to your web application. To open Azure Cloud Shell, click the shell logo in the tool bar at the top of the screen, as indicated by the red arrow in the following image:  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%208.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. Once you've clicked this icon, the Cloud Shell will be accessible at the bottom of your page. Next, from the command line, you'll enter a command to configure your container. There are three types of commands that manage your web app container settings:


az webapp config container delete - This will delete your web app container's settings.


az webapp config container set - This will set your web app container's settings.


az webapp config container show - This will display the current details of your web app container's settings.




To configure your web app with your provided container, run the following: az webapp config container set --name <name of your webapp> --resource-group <name of your resource group> --docker-custom-image-name <container-name> --enable-app-service-storage -t. After pressing Enter, an output similar to the image below should appear: <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%209.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
4. To verify that the container has been added correctly, run the following command to show the container for your web app: az webapp config container show --name <name of webapp> --resource-group <name of your resource group>. Now, check the unique domain that you selected to verify that the container has been successfully deployed. A cyber blog webpage that looks like the following image should appear (note that it may take five to eight minutes to load):  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2016.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Design Your Custom Web Application: Part 3</h2>

1. The container that you just loaded onto your web application is a framework for a cyber blog page that you can customize.
To design and customize your webpage, you'll need to access the HTML pages of your new web application.To access these pages, you need to SSH over to your container and access the HTML files. Return to your web app in Azure, select "SSH" from the left-hand toolbar, and then select "GO," as shown in the following image:  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2017.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
2. This will SSH you right into the container. Once you have access, change directories to the location where the HTML files are located by running cd /var/www/html, as the following image shows::  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2018.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. This directory contains the index.html file that makes up your webpage. To customize your webpage, complete the following steps:


To change your name:


Run: nano index.html


Replace "ROBERT SMITH'S CYBER BLOG" with your name/text.


Replace "Hi, I'm Robert!" with your name/text.




To change your email:

In the same index.html file, replace "aaggarwal@2u.com" with your email address.



To change your LinkedIn profile link:

In the same index.html file, replace "https://www.linkedin.com/" with the link to your LinkedIn profile.



To change your introduction:

In the same index.html file, replace the paragraph beginning "This is a little introductory paragraph" with your own introduction

To change your "Blogs 1 and 2"
In the same index.html file, replace "Blog Post 1 & 2 Titles, change "Add Keywords" to relevant keywords for your post " to the title of your first blog post, and change the section beginning "Add a short description here" to the text of your blog post:  <br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2013.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2014.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>4. After each update to your webpage, make sure you back up your index.html file to your /home directory (which stays persistent across reboots) with the following command:

cp /var/www/html/index.html /home



In case you need to restore your index.html file, run the following command:

cp /home/index.html /var/www/html/ 



After you have saved and backed up your changes, return to your browser and refresh your webpage.</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
