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

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
