<h2>Part 1: Create a Front Door Instance</h2>

<p align="center">

1. Begin by logging in to the Azure portal: https://portal.azure.com.

2. Next, access the app service resource.

3. From the menu on the left side of the screen, select “Networking.”

4. On the next page, since you haven't created your Front Door resource yet, select “Create new” under “Front Door profile.”


5. This will open a pane on the right side of your screen.

- In this pane, name your Front Door “project1-FrontDoor”.

- Enter “project1” for the Endpoint name.

- The Endpoint hostname will be created automatically based off of the Endpoint name.

- Enter in “RedTeam” for the Origin group name.

- Select “Premium” for the Pricing Tier.

- Click the “OK” button at the bottom of the pane
<br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2030.png?raw=true" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

7. This will return you to the Azure Front Door page.

-Click “Create” to update the Front Door instance to your application.

8. To verify that your Front Door instance has been set up correctly, select “Azure Front Door”.

9. The message “Azure Front Door is configured for your web app” should display as confirmation, as shown in the following image:

     <img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Project%201%20day%203%20front%20door.PNG?raw=true" width="80%" alt="Disk Sanitization Steps"/>

     <br>
     </br>

<h2>Part 2: Analyze WAF Rule Sets</h2>

   1) From your Azure portal, enter “web app” until “Web Application Firewall policies (WAF)” appears as one of the choices in the dropdown.

   2) Select that option. The WAF that you created during the previous step should display on the “Web Application Firewall policies (WAF)” page.

   3) When your WAF policies page opens, notice the options on the left side of your screen.

   4) Select “Managed rules” either from the left-hand toolbar or from the box on the bottom of the page, as the following image shows:

   <img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2031.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>   
   
   5) When the “Managed rules” page appears, scroll through the page to view the various rules

 <h2>Part 3: Configure Custom WAF Rules</h2>

 1. Select “Custom rules” from the toolbar on the left-hand side of the screen, as the following image shows:

    <img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2032.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 2. To create a custom rule, select “+ Add custom rule.”

    a) When the pane pops up on the right, name your custom rule “Project1rule”.

    b) Leave the status and rule type at the default options.

    c) Set the priority to 100.

    d) Set the following terms for the rule’s condition:
         <br>
         </br>
     -Match type: Geo location
         <br>
         </br>
     -Match variable: Remoteaddr
          <br>
         </br>
     -Operation: is not
         <br>
         </br>
     -Select the three countries (USA, Canada, Australia) - Don’t forget to add your own country if it isn’t one of the three listed.
         <br>
         </br> 
     -Then: Deny traffic



<br>
<br/>
3. Your custom rule should now display on the page, as the following image shows:

<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/assets/80586285/5f2441bb-a9f0-4000-810e-f69f45024747" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
