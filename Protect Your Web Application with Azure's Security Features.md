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
