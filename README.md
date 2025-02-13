<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used</h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Configure Agents & Users 
- Configure SLA/Help Topics

<h2>Configuration Steps</h2>

Admin/Analyst Login Page:
http://localhost/osTicket/scp/login.php

End Users osTicket URL:
http://localhost/osTicket 

<h3>Admin Panel</h3>

<img src= https://i.imgur.com/bmyfw6Y.png >

<h3>Agent Panel</h3>

<img src= https://i.imgur.com/DG2os7l.png >

<h3>Roles Configuration</h3>
First, we need to configure roles for osTicket in order to have grouping permissions. The only role we'll be creating for this project is "Supreme Admin".
<p></p>
<img src= https://i.imgur.com/hDizvyB.png>

- Make sure you are in the Admin Panel
- Click the Agents Tab -> Roles Tab
- Click on "Add New Role"

<img src=https://i.imgur.com/FENbjkS.png>

- In the Definition tab, Set name to "Supreme Admin"

<img src=https://i.imgur.com/gbeSbyd.png>
<img src=https://i.imgur.com/lIQ9PU1.png>
<img src=https://i.imgur.com/qkgHepS.png>

- In the Permissions tab, Check every box within "Tickets", "Task" & "Knowledge"
- Now click "Add Role" once done

<h3>Departments Configuration</h3>

Now we will add Departments to delegate where Agents belong respectively.

<img src= https://i.imgur.com/JZNWPjj.png>

- Click on the Agents Tab then the Departments Tab
- Now click "Add New Department"

<img src=https://i.imgur.com/lvlkce9.png>

- For "Parent" keep it as "Top-Level Department"
- Name this Department "SysAdmin"
- Now click "Add Department"

<h3>Teams Configuration</h3>

The purpose teams is to create a group of people from different departments

- Click on the Agents Tab then Teams Tab
- Click "Add New Team"
<img src=https://i.imgur.com/CYCK4FZ.png>

- For the name, I'll just use "Online Banking"
- Click "Create Team"

<img src=https://i.imgur.com/DDMEJlE.png>

<h3>Tickets Configuartion</h3>

Now before we proceed any further, Lets allow tickets to be created by anyone

- Click on Settings Tab then click on Users Tab
- Make sure "Regristration Required" is unchecked

<img src=https://i.imgur.com/kSCfyCS.png>

<h3>Agents Configuration</h3>
Now is the time to add Agents who will be the ones solving tickets.
We will be adding 2 Agents.

- Click on Agents
- Click on "Add New Agent"

<img src=https://i.imgur.com/UznztLb.png>

Create Jane's Account

(Here you can be freely choose a name for your liking, for simplicity I'll be using Jane and John)
- Fill in the Name, Email Address & Username (Can choose how you name them)
<img src=https://i.imgur.com/z70cmTS.png>

While we're here, We can also set Jane's password
- Click "Set Password"
- Uncheck "Password Reset Email"
- Set the password to your liking
- Uncheck "Require Password Change"
- Click "Set"

<img src=https://i.imgur.com/q5lIsor.png>

- In the Access Tab, Assign Jane to "SysAdmin" Department & "Supreme Admin" Role

<img src=https://i.imgur.com/woSuU7j.png>

- In the Teams Tab, Assign Jane to the Team you have created prior then click "Create"

<img src=https://i.imgur.com/w67DEUN.png>

Creating Johns Account

- Fill in the Name, Email Address and Username like before

<img src=https://i.imgur.com/RXZBMmi.png>

- Set the password like before as well

<img src=https://i.imgur.com/q5lIsor.png>

- In the Access Tab, Assign John to "Support" Department & "View Only" Role
- We won't be assigning him to a Team so click "Create"
<img src=https://i.imgur.com/KOahRkd.png>

<h3>Users Configuration</h3>

Now we will be adding 1 user, This user can create tickets. We will be swapping to the Agent Panel for this configuration

- Click on the Agent Panel
- Click on the Users Tab
- Click "Add user"

<img src=https://i.imgur.com/iYNQ1IF.png>
<img src=https://i.imgur.com/5SxNtFs.png>

(Karen will be my user but you're free to choose your own names)
- Fill in the Name and Email Address of your User
<img src=https://i.imgur.com/pi7RyTJ.png>

<h3>SLA Configuration</h3>

SLA (Service Level Agreement) is essentially a rule/rules that determine the severity and time needed to resolve a ticket. We will be returning to the Admin Panel for this.

- Click Manage Tab
- Click SLA
- Click "Add New SLA"
- Click "Set Plane" for your SLA's
<img src=https://i.imgur.com/WQPjqRE.png>
Sev-A (Grace Period: 1 Hour, Schedule: 24/7)
<img src=https://i.imgur.com/B3lgZoJ.png>
Sev-B (Grace Period: 4 Hours, Schedule: 24/7)
<img src=https://i.imgur.com/bzjL5ZJ.png>
Sev-C (Grace Period: 8 Hours, Schedule: Business hours)
<img src=https://i.imgur.com/CFo5h4b.png>

<h3>Topics Configuration</h3>
Now we will configure "Help Topics', This'll allow our users to more specifically assign their tickets.

- In the Manage Tab click Help Topics
- Click "Add help Topics"
- We will be creating 5 topics
<img src=https://i.imgur.com/P7DyEJn.png>

- Business Critical Outage
<img src=https://i.imgur.com/eoSwA6N.png>

- Personal Computer issues
<img src=https://i.imgur.com/ap0ETCP.png>

- Equipment Request
<img src=https://i.imgur.com/7cewod5.png>

- Password Reset
<img src=https://i.imgur.com/kAljqlN.png>

- Other
<img src=https://i.imgur.com/8pGeiQi.png>

<h3>Done!</h3>
We have completed the necessary configurations to get osTicket to work.
