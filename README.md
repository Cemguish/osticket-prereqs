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
<img width="465" height="341" alt="VM 10" src="https://github.com/user-attachments/assets/00d7007f-2153-47db-9bf5-56b4afabd0e0" /><br />
</p><br />
  
<p>
Now you should be logged on to the new virtual machine.
</p>

<img width="1904" height="1039" alt="VM 11" src="https://github.com/user-attachments/assets/3fb742aa-bb40-42be-8bbe-e87d23b5e0f8" />
  <p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>

<p>
<img width="1236" height="968" alt="VM 4" src="https://github.com/user-attachments/assets/c98795c6-6699-4dd5-b6e1-3c1d9de278c0" />
  <p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
</p>
<p>
<img width="1236" height="968" alt="VM 4" src="https://github.com/user-attachments/assets/c98795c6-6699-4dd5-b6e1-3c1d9de278c0" />
  <p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
</p>
<p>
<img width="1236" height="968" alt="VM 4" src="https://github.com/user-attachments/assets/c98795c6-6699-4dd5-b6e1-3c1d9de278c0" />
  <p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
</p>
<p>
<img width="1236" height="968" alt="VM 4" src="https://github.com/user-attachments/assets/c98795c6-6699-4dd5-b6e1-3c1d9de278c0" />
  <p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
</p>
<p>
<img width="1236" height="968" alt="VM 4" src="https://github.com/user-attachments/assets/c98795c6-6699-4dd5-b6e1-3c1d9de278c0" />
  <p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
</p>
