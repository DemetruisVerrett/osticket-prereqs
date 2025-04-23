<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

-	Roles
- Departments
- Teams
- Agents (workers)
- Users (customers)
- Help Topics
- Service Level Agreements (SLAs)

<h2>Configuration Steps</h2>

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>
Now that osTicket has been successfully configured on our virtual machine, we’ll set system administrative tasks within osTicket. We will begin by configuring roles within the help desk. By doing so, we will be able to effectively manage permissions and user access. 
</p>
<br />

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>
To configure roles within help desk, we go to the Admin Panel > Agents > Roles. Click on “Add new role”. 
</p>
<br />

<p>
<img src="" height="80%" width="80%"/>
</p>

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>
We then enter the name of the new role, such as Supreme Admin. This will allow us to define the responsibilities and permissions for that role. Since we are creating a Supreme Admin role, we will ensure that all available permissions are selected to provide full administrative access. 
</p>
<br />

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>
Next, we select the “Departments” button in the Agents tab. Here we will create a new department, with each agent assigned to a specific department based on their role within our help desk. We create a “System Administrators” department. Keep in mind that additional settings, such as Service Level Agreements (SLAs), managers, and email configurations, can also be customized within the Departments tab to coincide with our help desk’s operational needs. 
</p>
<br />

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>
We then move to configure teams. Teams allow us to group agents from different departments to collaborate. We navigate to Admin Panel > Agents > Teams. We create a team called “Level II Support” and assign agents from various departments as needed. 
</p>
<br />

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>
In order to allow anyone to create tickets, we go to Admin Panel > Settings > Users. We uncheck the option called “Require registration and login to create tickets”. This will enable unregistered users (those without an account) to submit tickets as needed. 
</p>
<br />

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>
Before any tickets can be processed, we need to configure agents (workers). We go to Admin Panel > Agents > Add New Agent. We fill in the details for each agent, including their name, email address, assigned role and department. This will set up each agent’s profile and appropriate permissions. 
</p>
<br />

<p>
<img src="" height="80%" width="80%"/>
</p>

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>
For the purposes of our project, we need to configure users (customers). We go to the Agent Panel > Users > User Directory > Add User. We add users Shawn and Rachel by entering their details, including their names and email addresses. This will enable our users to submit and manage their tickets. 
</p>
<br />

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>
To assist users in submitting tickets, it’s advisable to configure help topics. We navigate to Admin Panel > Manage > Help Topics. The help topics we add can then be used as a guide to users in categorizing their tickets more effectively. 
</p>
<br />

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>
As tickets are generated, it’s a good idea for agents to categorize them based on pre-determined priorities. Service Level Agreements (SLAs) are a great way to do this so that tickets with the highest urgency are dealt with more quickly. To configure SLAs we go toAdmin Panel > Manage > SLA. 
</p>
<br /> 
