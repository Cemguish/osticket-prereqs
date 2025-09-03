<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>Enhancing IT Support with OS Ticket: Deployment and Lifecycle Management</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Azure 
- PHP Manager for IIS
- Rewrite Module
- VC relist
- MySQL
- HeidiSQL

<h2>Installation Steps for Azure</h2>
<p>
  <ul>
  <li>Step 1: Go to the Azure Website https://azure.microsoft.com</li>
  <li>Step 2: Click Start free</li>
  <li> Step 3: Sign in / Create a Microsoft Account</li>
  <li>Step 4: Verify Your Identity</li>
  <li>Step 5: Accept Terms & Conditions</li>
  <li>Step 6: Start Using Azure</li>
    </ul>
    <img width="1909" height="1001" alt="image" src="https://github.com/user-attachments/assets/cd545f5d-90e3-4ae4-88ec-01ce45b03b5b" />
</p>
<br>


<p>
<img width="1601" height="927" alt="Capture" src="https://github.com/user-attachments/assets/6ce12c99-9799-46c8-b734-ae74cbfee1ab" />

</p>
<p>
Login to Azure an create a new virtual machine.
   <b>Creating a Virtual machine.</b>  
  <li>Click + Create → Azure virtual machine.</li>
<li>Fill in the Basics tab:</li>
<li>Subscription: Select your subscription ( Azure subscription1.)</li>
<li>Resource group: Pick your existing one (e.g., MyResourceGroup) (osTicket).</li>
<li>VM name: Choose a name (e.g., MyVM01) (osTicket-vm).</li>
<li>Region: Same region as your VNet.(East US 2)</li>
<li>Image: Choose the OS (Windows Server, Ubuntu, etc.)(Windows 10 Pro,Version 22H2 - x64 Gen2).</li>
<li>Size: Pick a VM size (e.g., B1s for free-tier)(Standard_D2s_v3 -2 vcpus,8 GiB memory).</li>
<li>Authentication type: Choose Password or SSH key.(osTicketPassword1!)</li>
<li>Username/Password or SSH Key: Set login credentials.(labuser)</li> 
<li>Check Licensing box </li> 
<li>Inbound ports: Select what to allow (e.g., RDP for Windows, SSH for Linux).</li>
<li>Go to Networking:</li>
<li>Select your Virtual network (e.g., MyVNet01)(vnet-eastus2(osTicket).</li>
<li>Choose an existing Subnet (e.g., MySubnet01)(snet-eastus2-1) .</li>
<li>Leave defaults for Disks and Management (or customize if needed).</li>
<li>Click Review + Create → Create.</li>
<li>After deployment, you can connect via SSH (Linux) or RDP (Windows).</li><br>
</ul>
<img width="1889" height="775" alt="VM 1" src="https://github.com/user-attachments/assets/ff9d2fc3-d701-4838-a84c-598f10e5df05" />
<img width="1222" height="952" alt="VM 3" src="https://github.com/user-attachments/assets/32895591-6d1e-48d9-ae02-66872d50d53c" />
<img width="1236" height="968" alt="VM 4" src="https://github.com/user-attachments/assets/c98795c6-6699-4dd5-b6e1-3c1d9de278c0" />
</p>



<p>
 <b>Next login to the virtual machine and locate and copy the IP address.</b> 
<li>Copy the IP address and open remote desktop</li>
  <li>In the computer field paste the public IP address of the virtual machine.</li> 
    <li>Next, navigate to the Show options button and click to open for more options.</li>
  <li>You should now see more options. In the user name field type your user name and click connect.</li>
  <li>Then enter your password and click ok.</li><br>
<img width="1608" height="961" alt="VM 5" src="https://github.com/user-attachments/assets/0f22e591-1c55-44c8-a58f-dd0825ff596e" />
<img width="1892" height="609" alt="image" src="https://github.com/user-attachments/assets/9b905913-5271-4b72-aaa0-e0a9641a3f00" />
<img width="420" height="262" alt="VM 8" src="https://github.com/user-attachments/assets/36c2e086-3869-4df2-9e58-88ea7520f9f3" />
<img width="411" height="498" alt="VM 9" src="https://github.com/user-attachments/assets/c5d14dc0-ab16-467c-8afa-33298a3208be" />
<img width="465" height="341" alt="VM 10" src="https://github.com/user-attachments/assets/00d7007f-2153-47db-9bf5-56b4afabd0e0" />
</p><br />
  

 <p>
    <b>Now you should be logged on to the new virtual machine.</b> 
   <li>Open the browser in virtual machine and paste the link for osTicket folder hit enter.</li><br> 
<img width="1904" height="1039" alt="VM 11" src="https://github.com/user-attachments/assets/3fb742aa-bb40-42be-8bbe-e87d23b5e0f8" />
<img width="1291" height="754" alt="VM 13" src="https://github.com/user-attachments/assets/82933f4e-b0ff-497b-ade9-cc02645b9f5b" />
</p><br />


<p>
   <b>When the folder is downloaded go to your downloads folder.</b>  
<li>Drag folder to desktop of virtual machine.</li>
    <li>Right click extract all make sure it is being extracted to the desktop.</li> 
    <li>After extracting all to desktop IIS needs to be installed in windows with CGI.</li><br>
<img width="1909" height="1005" alt="VM 14" src="https://github.com/user-attachments/assets/4ea60cb6-1a31-41ce-940d-f2dcd90bfaa5" />
<img width="1914" height="1032" alt="VM 15" src="https://github.com/user-attachments/assets/8f26a705-0a1b-4837-bb44-c3ceeda95554" />
</p><br />
  <p>
 <b>Now I will enable IIS in windows.</b>  
    <li>Go to start</li>  
    <li>Control panel</li>  
    <li>Programs and Features</li>  
    <li>Turn windows features on or off then click on it.</li>
    <li>Now, select Internet Information Services in the drop down.</li> 
    <li>Check this box then expand it.</li> 
    <li>Next, CGI will be installed.</li> 
<li>Go to worldwide web services > Application Development Features > Check the CGI box.</li> 
    <li>Then click ok.</li><br>
<img width="1231" height="948" alt="VM 16" src="https://github.com/user-attachments/assets/610b481d-bc19-48df-9261-0b3525d2988e" />
<img width="1801" height="991" alt="image" src="https://github.com/user-attachments/assets/e5a7538f-3991-4f0c-a8d1-ebe98fddb16d" />
</p><br />

  <p>
<b>Next, I will install PHP Manager for IIS from the osTicket-installation - File folder.</b>  
<li>Go to the osTicket installation file.</li> 
<li>Locate PHP manager and install.</li>
<li>After this is installed go back to the os Ticket folder on desktop.</li> 
<li>Locate the Rewrite Module and install.</li>
<li>Now, I will create a directory on the C drive called PHP.</li>
<li>Open a new file explorer click on the C.Drive right click > New Folder> Name this file PHP.</li>
<li>Next, go back to the osTicket file and select the zipped file> then right click and extract all.</li> 
<li>Browse to C drive locate PHP folder extract all then close.</li><br>
<img width="1804" height="1022" alt="VM 19" src="https://github.com/user-attachments/assets/31fe09ce-4a4b-455e-bdff-41c74f20d129" />
<img width="1128" height="638" alt="VM 20" src="https://github.com/user-attachments/assets/dabeed48-f264-4258-9f49-66bdccaa9fac" />
<img width="1162" height="655" alt="VM 22" src="https://github.com/user-attachments/assets/47a21b90-88db-4cda-b1eb-fbb97964f40f" />
<img width="1362" height="769" alt="VM 23" src="https://github.com/user-attachments/assets/c842ea82-2bef-4842-83ac-0d5bd88d01a9" />
<img width="1697" height="814" alt="VM 24" src="https://github.com/user-attachments/assets/afe58b3a-a106-43f3-bc9a-8bf0d52c4ae5" />
</p><br>

<p>
  <b>Go back to the osTicket file.</b>  
  <li>Now I will be installing VC redist.</li><br> 
<img width="1140" height="648" alt="VM 25" src="https://github.com/user-attachments/assets/a83e028d-9fdf-434a-b5ac-9e2f02995dec" />
</p>

<p>
    <b>Now, I will install MySQL.</b>   
  <li>Select Standard > Root password will be root for example after installation hit finish.</li> 
    <li>Make sure to select the standard configuration the click next.</li> 
  <li>At MySQL Server Instance Configuration window create an input your password for both fields then next.</li><br> 
<img width="1135" height="644" alt="VM 26" src="https://github.com/user-attachments/assets/00d58f1b-ee45-4d19-bfda-8b9b6d60e0f0" />
  <img width="507" height="392" alt="VM 28" src="https://github.com/user-attachments/assets/74e5298b-cbd9-42f3-8b25-35a1874350a9" />
  <img width="747" height="573" alt="VM 27" src="https://github.com/user-attachments/assets/6895a7bc-314e-436b-98f9-c3bd00cd43b7" />
</p>

<p>
     <b>Next, I will configure PHP</b> 
    <li>Go to the start menu</li>  
    <li>Open IIS as admin</li> 
    <li>Now open the PHP manager by double clicking the icon</li>   
    <li>Navigate to register new PHP version click on this.</li> 
    <li>At the register new PHP version pop up screen locate browser button with the three dots.</li>  
    <li>Go to the Cdrive when you PHP file is located.</li>  
    <li>Open the file locate the php-cgi.</li>  
    <li>Icon double click to install.</li>  
    <li>This will take you back to the register new PHP version window.</li>  
    <li>click ok.</li><br>  
<img width="1218" height="853" alt="VM 29" src="https://github.com/user-attachments/assets/0eb94e5b-70cf-42ec-91e7-bb9c67245a9f" />
<img width="1455" height="781" alt="VM 30" src="https://github.com/user-attachments/assets/1edfa096-5661-46bc-afba-a099a1eca9a3" />
<img width="1433" height="770" alt="VM 32" src="https://github.com/user-attachments/assets/f7496c57-28f7-4d76-91f5-332ef5ec0cee" />
<img width="1494" height="849" alt="VM 33" src="https://github.com/user-attachments/assets/e2d15514-4c1a-465e-8b8e-086538ace231" />
<img width="1430" height="767" alt="VM 34" src="https://github.com/user-attachments/assets/f04527aa-ac28-44fa-99b8-54a9ccc6e5c8" />

</p>


<p>
  PHP should be registered at this point your screen should look like the following slide.
<img width="1435" height="764" alt="VM 35" src="https://github.com/user-attachments/assets/d67ae88f-50dd-4a90-929b-111aeeb9d40d" />

</p>

<p>
  Now I will reload IIS stop start the server
<img width="1437" height="766" alt="image" src="https://github.com/user-attachments/assets/6f05ad29-5904-44d0-8df4-deab7dcac403" />

</p>

<p>
  Finally, I will install osTicket.
  Go to the osTicket installation folder on desktop > open the folder navigate to osTicket file > extract all
  <img width="1704" height="802" alt="VM 37png" src="https://github.com/user-attachments/assets/415921b5-0dc2-4727-9345-129d8c81cd43" />
</p>

<p>
    After the file extraction go to the osTicket folder > inside the folder there should be two folders scripts and uploads.
<img width="1693" height="795" alt="VM 38" src="https://github.com/user-attachments/assets/e360b81e-0b4e-41c5-bd47-be722ce0b804" />
</p>


<p>
  Next, I will open file explorer navigate to the C.drive > inetpub folder > wwwroot folder > Copy upload folder to wwwroot folder.
  Rename upload folder to osTicket. Then restart/Reload the server again.
<img width="1475" height="821" alt="VM 39" src="https://github.com/user-attachments/assets/ae889772-c91a-455c-976d-4a077bb345c8" />
</p>

<p>
I will load the osTicket site. Go to the IIS manager window > click on site > Default Website > click osTicket folder > navigate to the right side of screen > 
  Go to Browser folder Click on the Browse*:80 (http). The osTicket website should pop up. You will notice some of the features are not enabled.
<img width="1838" height="1008" alt="VM 40" src="https://github.com/user-attachments/assets/46c69e35-bef9-41ac-9cf7-9dbb6400806f" />
</p>

<p>
  To enable go back to IIS Manager. Go to sites >  Default Website > osTicket folder > Double click PHP manager > Go to Enable or disable an extension.
<img width="910" height="1036" alt="VM 41" src="https://github.com/user-attachments/assets/b07f9736-d5d8-47d2-b6a4-e4af16e96313" />

</p>

<p>
  Enable the following - Enable: php_imap.dll > Enable: php_intl.dll > Enable: php_opcache.dll
  After enabling the following refresh the osTicket browser. 
<img width="913" height="967" alt="VM 42" src="https://github.com/user-attachments/assets/738281d9-4e15-4e64-8018-dc492e38f753" />
</p>

<p>
  Now PHP IMAP Extension — Required for mail fetching and Intl Extension — recommended for improved localization is now enabled.
<img width="928" height="1014" alt="VM 43" src="https://github.com/user-attachments/assets/179ddbe5-32d7-4fe9-8c9f-ba3cbdd5b221" />

</p>

<p>
  Next, I will rename ost-config.php. Go osTicket file > open file explorer navigate to the C.drive > inetpub folder > wwwroot > osTicket > include.
  Scroll down to ost-sampleconfig.php file and rename it to ost-config.php
  From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
  To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

  Next, right click > Properties > security > Advanced > Disable inheritance > remove permissions. 
  Now add new permissions > Select principle > type everyone then click ok> check full control box> click ok
<img width="1466" height="941" alt="VM 45" src="https://github.com/user-attachments/assets/4c2c4e6c-a67b-4e37-939d-d19445c12cc0" />

</p>

<p>
  Advance Security window setting should say principal should say everyone Access full control now click apply and ok > then ok to properties 
<img width="785" height="530" alt="VM 46" src="https://github.com/user-attachments/assets/27dd2fc5-92b8-428c-8fbe-c2e70135b661" />

</p>

<p>
  Now go back to the osTicket website and click continue.
  Fill in the appropriate fields. Before clicking the install Now create a database connection. 
  Go back to the osTicket installation file folder > Navigate to HeidiSQL and install 
<img width="1393" height="917" alt="VM 47" src="https://github.com/user-attachments/assets/ac057557-df77-4dd6-81b4-eb0b05e77324" />
</p>

<p>
   Go back to the osTicket installation file folder > Navigate to HeidiSQL and install 
<img width="1198" height="846" alt="VM 48" src="https://github.com/user-attachments/assets/54379fdb-b084-40ca-b49e-55847d7f26b6" />

</p>

<p>
  Now I will make a connection to the database for osTicket in HeidiSQL. 
  Click new user and password is root. Click open.
<img width="736" height="498" alt="VM 49" src="https://github.com/user-attachments/assets/fa9f4a84-3543-4e20-972b-5641eb611945" />
<img width="955" height="612" alt="VM 50" src="https://github.com/user-attachments/assets/5748cdda-bd5b-457c-9bb6-6964d2a6e3bf" />
</p>

<p>
  Create database called osTicket. Right click on unnamed > create new > Database> Name it osTicket.
  You will now see osTicket in the database list. Now go back to the osTicket browser.
<img width="1541" height="877" alt="image" src="https://github.com/user-attachments/assets/8cc289c6-10e5-4839-bc4c-e08696193210" />

</p>

<p>
  Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”
<img width="1166" height="929" alt="VM 52" src="https://github.com/user-attachments/assets/7e21af9f-e459-4360-9d4c-a37341455d03" />

</p>

<p>
  Now osTicket should be completely installed.
<img width="1089" height="763" alt="image" src="https://github.com/user-attachments/assets/79ac39c8-867f-4ca8-a48d-5394b24f704c" />

</p>

<p>
  Check to see if it is working login using the user name and paasword. Once logged in osTicket is working.
<img width="1047" height="442" alt="VM 55" src="https://github.com/user-attachments/assets/901efd34-2e39-4dbf-9337-fcd8e7916a8d" />
</p>

