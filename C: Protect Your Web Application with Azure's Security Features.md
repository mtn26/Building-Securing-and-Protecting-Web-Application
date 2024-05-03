<h2>Part 1: Create a Front Door Instance</h2>

<p align="center">

1. I begin by searching “Networking” in my web app service portal 

2. On the next page, I select “Create new” under “Front Door profile.”


 3. I named my Front Door “project1-FrontDoor”.

-  “project1” for my Endpoint name.

- The Endpoint hostname was automatically based on the Endpoint name.

-  I entered in “RedTeam” for the Origin group name.

- I selected “Premium” for the Pricing Tier.

<br/>
<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2030.png?raw=true" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

4) I clicked on the “Create” tab to update the Front Door instance of my web application and verified it was set up correctly. The message “Azure Front Door is configured for your web app” is displayed as a confirmation

     <img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/assets/80586285/b5de5b2d-d13f-4bc5-b528-da83129e4ac3" width="80%" alt="Disk Sanitization Steps"/>

     <br>
     </br>

<h2>Part 2: Analyze WAF Rule Sets</h2>

   1) From your Azure portal, I entered “web app” until “Web Application Firewall policies (WAF)” appeared

   2)  The WAF policies page opened and I selected “Managed rules” 

   <img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2031.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>   
   
   3) When the “Managed rules” page appeared, I looked through the various rules

 <h2>Part 3: Configure Custom WAF Rules</h2>

 1. I selected “Custom rules” 

    <img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/blob/main/Resume%20Project%201%20pic%2032.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 2. To create a custom rule, I selected “+ Add custom rule.”

    a) I named my custom rule “Project1rule”.

    b) I left the status and rule type at the default options.

    c) I set the priority to 100.

    d) I set the following terms for the rule’s condition:
         <br>
         </br>
     -Match type: Geolocation
         <br>
         </br>
     -Match variable: Remoteaddr
          <br>
         </br>
     -Operation: is not
         <br>
         </br>
     -I selected the three countries (USA, Canada, Australia) 
         <br>
         </br> 
     -Then: Deny traffic


<img src="https://github.com/mtn26/Building-Securing-and-Protecting-Web-Application/assets/80586285/5f2441bb-a9f0-4000-810e-f69f45024747" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Part 4: Analyze and Fix a Security Center Recommendation</h2>

1. I access the Azure Security Center by clicking on “Microsoft Defender for Cloud” from the toolbar
2. When the Security Center page opens, it displays counts for both recommendations and alerts. I reviewed all the recommendations.
   <br/>
