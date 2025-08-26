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

<h2>Installation Steps</h2>

<p>
<img width="1601" height="927" alt="Capture" src="https://github.com/user-attachments/assets/6ce12c99-9799-46c8-b734-ae74cbfee1ab" />

</p>
<p>
Login to Azure an create a new virtual machine.
</p>
<br />
<img width="1889" height="775" alt="VM 1" src="https://github.com/user-attachments/assets/ff9d2fc3-d701-4838-a84c-598f10e5df05" />

<p>
  <p>
Fill in the following information fields.
    <ul>
<li>Resource group</li>
<li>Virtual machine name</li>
<li>Region</li>
<li>Image</li>
<li>Size</li>
<li>User, Password, and confirm Password</li>   
    </ul>
  
</p>
<br />
<img width="1222" height="952" alt="VM 3" src="https://github.com/user-attachments/assets/32895591-6d1e-48d9-ae02-66872d50d53c" />

After filling in the information fields check the Licensing box. Then click next Disk > next Networking page. Locate the Virtual network there should be a generated network name.
Then, review and create click again to deploy virtual machine.
</p>
<br />
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1236" height="968" alt="VM 4" src="https://github.com/user-attachments/assets/c98795c6-6699-4dd5-b6e1-3c1d9de278c0" />
</p>
<p>
At this point the deployment should be completed. Next login to the virtual machine and locate and copy the IP address.
</p>
<br />

<p>
<img width="1608" height="961" alt="VM 5" src="https://github.com/user-attachments/assets/0f22e591-1c55-44c8-a58f-dd0825ff596e" />

  <p>
Copy the IP address and open remote desktop 
</p>
</p>
<p>
<img width="1892" height="609" alt="image" src="https://github.com/user-attachments/assets/9b905913-5271-4b72-aaa0-e0a9641a3f00" />

  <p>
In the computer field paste the public IP address of the virtual machine. Next, navigate to the Show options button and click to open for more options.
</p>
</p>
<p>
<img width="420" height="262" alt="VM 8" src="https://github.com/user-attachments/assets/36c2e086-3869-4df2-9e58-88ea7520f9f3" /><br />
    <p>
You should now see more options. In the user name field type your user name and click connect.
</p>
<img width="411" height="498" alt="VM 9" src="https://github.com/user-attachments/assets/c5d14dc0-ab16-467c-8afa-33298a3208be" /><br />
    <p>
Then enter your password and click ok
</p>

<p>
<img width="465" height="341" alt="VM 10" src="https://github.com/user-attachments/assets/00d7007f-2153-47db-9bf5-56b4afabd0e0" /><br />
</p><br />
  

 <p>
   Now you should be logged on to the new virtual machine.
<img width="1904" height="1039" alt="VM 11" src="https://github.com/user-attachments/assets/3fb742aa-bb40-42be-8bbe-e87d23b5e0f8" />
</p>

  <p>
Open the browser in virtual machine and paste the link for osTicket folder hit enter. 
</p>

  <p>
<img width="1291" height="754" alt="VM 13" src="https://github.com/user-attachments/assets/82933f4e-b0ff-497b-ade9-cc02645b9f5b" />

</p><br />

<p>
  <p>When the folder is downloaded go to your downloads folder. 
Drag folder to desktop of virtual machine. </p>
<img width="1909" height="1005" alt="VM 14" src="https://github.com/user-attachments/assets/4ea60cb6-1a31-41ce-940d-f2dcd90bfaa5" />

  <p>
Right click extract all make sure it is being extracted to the desktop. After extracting all to desktop IIS needs to be installed in windows with CGI
</p>

<p>
<img width="1914" height="1032" alt="VM 15" src="https://github.com/user-attachments/assets/8f26a705-0a1b-4837-bb44-c3ceeda95554" />

  <p>
Now I will enable IIS in windows. Go to start > Control panel > Programs and Features > Turn windows features on or off then click on it.
</p>

<p>
<img width="1231" height="948" alt="VM 16" src="https://github.com/user-attachments/assets/610b481d-bc19-48df-9261-0b3525d2988e" />
  <p>
Now, select Internet Information Services in the drop down. Check this box then expand it. Next, CGI will be installed. 
Go to worldwide web services > Application Development Features > Then Check the CGI box. Then click ok.
</p>

<p>
<img width="1801" height="991" alt="image" src="https://github.com/user-attachments/assets/e5a7538f-3991-4f0c-a8d1-ebe98fddb16d" />
  <p>
Next, I will install PHP Manager for IIS from the osTicket-installation - File folder. Go to the osTicket installation file. 

    
</p>

<p>
<img width="1804" height="1022" alt="VM 19" src="https://github.com/user-attachments/assets/31fe09ce-4a4b-455e-bdff-41c74f20d129" />
</p>
<p>
  Locate PHP manager and install.
<img width="1128" height="638" alt="VM 20" src="https://github.com/user-attachments/assets/dabeed48-f264-4258-9f49-66bdccaa9fac" />

</p>

<p>
  After this is installed go back to the os Ticket folder on desktop. Locate the Rewrite Module and install.
<img width="1162" height="655" alt="VM 22" src="https://github.com/user-attachments/assets/47a21b90-88db-4cda-b1eb-fbb97964f40f" />
</p>

<p>
  Now, I will create a directory on the C drive called PHP.
  Open a new file explorer click on the C.Drive right click >  New Folder> Name this file PHP.
<img width="1362" height="769" alt="VM 23" src="https://github.com/user-attachments/assets/c842ea82-2bef-4842-83ac-0d5bd88d01a9" />
</p>

<p>
  Next, go back to the osTicket file and select the zipped file> then right click and extract all. Browse to C drive locate PHP folder extract all then close.
<img width="1697" height="814" alt="VM 24" src="https://github.com/user-attachments/assets/afe58b3a-a106-43f3-bc9a-8bf0d52c4ae5" />
</p>

<p>
  Go back to the osTicket file. Now I will be installing VC redist.
<img width="1140" height="648" alt="VM 25" src="https://github.com/user-attachments/assets/a83e028d-9fdf-434a-b5ac-9e2f02995dec" />
</p>

<p>
  Now, I will install MySQL. Select Standard > Root password will be root for example after installation hit finish.
<img width="1135" height="644" alt="VM 26" src="https://github.com/user-attachments/assets/00d58f1b-ee45-4d19-bfda-8b9b6d60e0f0" />
  Make sure to select the standard configuration the click next.
  <img width="507" height="392" alt="VM 28" src="https://github.com/user-attachments/assets/74e5298b-cbd9-42f3-8b25-35a1874350a9" />
At MySQL Server Instance Configuration window create an input your password for both fields then next.
  <img width="747" height="573" alt="VM 27" src="https://github.com/user-attachments/assets/6895a7bc-314e-436b-98f9-c3bd00cd43b7" />
</p>

<p>
  Next I will configure PHP go to the start menu > open IIS as admin >
<img width="1218" height="853" alt="VM 29" src="https://github.com/user-attachments/assets/0eb94e5b-70cf-42ec-91e7-bb9c67245a9f" />
</p>

<p>
  Now open the PHP manager by double clicking the icon > Navigate to register new PHP version click on this. 
<img width="1455" height="781" alt="VM 30" src="https://github.com/user-attachments/assets/1edfa096-5661-46bc-afba-a099a1eca9a3" />
</p>

<p>
  At the register new PHP version pop up screen locate browser button with the three dots. Go to the Cdrive when you PHP file is located > open the file locate the php-cgi > icon double click to install 
<img width="1433" height="770" alt="VM 32" src="https://github.com/user-attachments/assets/f7496c57-28f7-4d76-91f5-332ef5ec0cee" />
<img width="1494" height="849" alt="VM 33" src="https://github.com/user-attachments/assets/e2d15514-4c1a-465e-8b8e-086538ace231" />
</p>


<p>
This will take you back to the register new PHP version window > click ok 
<img width="1430" height="767" alt="VM 34" src="https://github.com/user-attachments/assets/f04527aa-ac28-44fa-99b8-54a9ccc6e5c8" />

</p>


<p>
  PHP Should be registered at this point your screen should look like the following slide.
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
  I will load the osTicket site.
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>

<p>
<img width="958" height="938" alt="VM 12" src="https://github.com/user-attachments/assets/4e93c0e3-8504-449d-97a1-ffb11a606c5d" />
</p>
