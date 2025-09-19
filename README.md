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

- Configure Roles (for grouping permissions)
- Configure Departments ( Tiket Visibility, Help desk Vs SysAdmin Vs Networking)
- Configure Teams
- Configure Agents (Workers)
- Configure Users (Customers)
- Configure SLA
- Configure Help Topics (When users create a ticket)

<h2>Configuration Steps</h2>

<p>
<img width="1274" height="758" alt="Annotation 2025-09-01 010921" src="https://github.com/user-attachments/assets/f417e166-2e5b-4f6e-9ef0-d77fae8a1493" />
<img width="1278" height="944" alt="Annotation 2025-09-01 011229" src="https://github.com/user-attachments/assets/b9d3608c-c412-4d81-b22b-147960dcbccd" />
<img width="1280" height="740" alt="Annotation 2025-09-01 011343" src="https://github.com/user-attachments/assets/633ba213-11d1-41f3-89c0-2ab303372bb5" />
<img width="1282" height="546" alt="Annotation 2025-09-01 011537" src="https://github.com/user-attachments/assets/58c8cb40-5494-4abe-9625-cb9073396add" />
<img width="1276" height="594" alt="Annotation 2025-09-01 011725" src="https://github.com/user-attachments/assets/c3688206-6ee3-4f62-9666-5a9df5167de9" />

</p>
<p>
We are going to configure roles (for grouping permissions). On Admin Panel--> Agents--> Roles--> Name it Supreme Admin--> Under permissions and tickets, check the box everything--> Tasks, check box everything--> Knowledge, check the box. Surpreme Admin role should be created.
</p>
<br />

<p>
<img width="956" height="1128" alt="Annotation 2025-09-01 012447" src="https://github.com/user-attachments/assets/d291a1e4-939a-4a37-bd1e-2368f10bc133" />



</p>
<p>
Configure Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)--> Parent, select "Top Level Department"--> Name, SysAdmins--> Create Dept

</p>
<br />

<p>
<img width="1276" height="398" alt="Annotation 2025-09-01 012702" src="https://github.com/user-attachments/assets/249c26c8-99a4-4505-9605-02bf6a5864de" />
<img width="1276" height="898" alt="Annotation 2025-09-01 012856" src="https://github.com/user-attachments/assets/0f054e39-bd84-40da-8aaa-9246aea19909" />
<img width="1276" height="908" alt="Annotation 2025-09-01 013102" src="https://github.com/user-attachments/assets/5cdbd81b-be7a-42b7-8c10-45728cab1561" />

</p>
<p>
Next we are going to configure teams--> Admin Panel --> Agents --> Teams (Pull Agents from different Departments)--> Name it Online Banking--> Create Team

On Admin Panel, allow anyone (end users) to create tickets--> settings--> Users--> UNCHECK: unregistered users can create tickets

</p>
<br />

<p>
<img width="1276" height="1280" alt="Annotation 2025-09-01 013529" src="https://github.com/user-attachments/assets/7f5e3556-24f0-474c-a211-93eb511d3a50" />
<img width="1278" height="714" alt="Annotation 2025-09-01 013648" src="https://github.com/user-attachments/assets/8dbb69af-3daa-43a9-98db-902d91b2ad90" />
<img width="1274" height="670" alt="Annotation 2025-09-01 013844" src="https://github.com/user-attachments/assets/659a9a38-3135-470d-9165-7423d07ef95d" />
<img width="1278" height="650" alt="Annotation 2025-09-01 014238" src="https://github.com/user-attachments/assets/ae40456d-978c-48f4-bd21-d8577ce057da" />

</p>
<p>
On Admin Panel, configure Agents (workers)--> Agents--> Add new--> Name the Agent, for this tutorial, Jane Doe--> create email for Jane Doe--> username, jane. Make sure you keep track of this information--> For access, Primary department, select support/SysAdmins--> set under Supreme Admin role--> Teams, set to the Online Banking team that was created then click add--> click create. 
  
  
</p>
<br />

<p>
<img width="1272" height="1266" alt="Annotation 2025-09-01 014412" src="https://github.com/user-attachments/assets/260d65fc-e018-4198-8b18-8ff77e495a08" />
<img width="1278" height="718" alt="Annotation 2025-09-01 014531" src="https://github.com/user-attachments/assets/539ae7f9-95ff-4b52-8e08-a4424f7fd8cf" />
<img width="860" height="510" alt="Annotation 2025-09-01 015127" src="https://github.com/user-attachments/assets/a66f6ad2-4f32-4730-85f0-e9ad8b9e39c5" />

</p>
<p>
Repeat this same proccess and create another Agent and name him John Doe--> Primary Department, support--> view ony role--> click create

  Go back to account for the agents--> click set password--> uncheck the box and you can set the passwords for both agents--> Set agent Jane and John's password to "password1" to keep it simple for this tutorial. Uncheck box "require password change at next login"
</p>
<br />

<p>
<img width="1272" height="458" alt="Annotation 2025-09-01 015407" src="https://github.com/user-attachments/assets/eab9aca6-0636-4175-8924-bc8400a4dad2" />
<img width="860" height="520" alt="Annotation 2025-09-01 015542" src="https://github.com/user-attachments/assets/27f809ea-2947-4916-b361-ca3320d67a70" />

</p>
<p>
Next lets configure Users (customers)--> Go to Agent panel--> users--> add user--> name her Karen and give an email address to her--> add user. Keep track of login information
</p>
<br />

<p>
<img width="1274" height="874" alt="Annotation 2025-09-01 020140" src="https://github.com/user-attachments/assets/f501269f-d67d-4c11-96e5-617a8643ceda" />
<img width="1276" height="878" alt="Annotation 2025-09-01 020259" src="https://github.com/user-attachments/assets/21c84b0f-5bb3-44f9-ae80-3ba00575e9a0" />
<img width="1282" height="878" alt="Annotation 2025-09-01 020403" src="https://github.com/user-attachments/assets/d507ca82-ddd7-49fb-a99f-33b0f685fb60" />

</p>
<p>
Configure SLA--> Admin Panel --> Manage --> SLA--> add new SLA plan

We are going to create 3 SLAs.

Name--> Sev-A--> grace, 1 hour--> schedule, 24/7--> add plan

Name--> Sev-B--> grace, 4 hour--> schedule, 24/7--> add plan

Name--> Sev-C--> grace, 8 hour--> schedule, Mon-Fri 8am-5pm with US holidays--> add plan
</p>
<br />



<p>
<img width="1274" height="834" alt="Annotation 2025-09-01 020601" src="https://github.com/user-attachments/assets/66920d7e-79e9-47fd-bc59-01a7469f14ad" />
<img width="1276" height="838" alt="Annotation 2025-09-01 020721" src="https://github.com/user-attachments/assets/02b9b26a-14d0-4cda-a434-e940934fc85a" />
<img width="1280" height="882" alt="Annotation 2025-09-01 020832" src="https://github.com/user-attachments/assets/60ebbd6a-6724-475d-ad6c-6de7a2e565a0" />
<img width="1262" height="832" alt="Annotation 2025-09-01 021029" src="https://github.com/user-attachments/assets/e8a8f76e-742f-4daa-bed8-2a9f30fb2144" />
<img width="1278" height="840" alt="Annotation 2025-09-01 021316" src="https://github.com/user-attachments/assets/67b5e6ae-5bb2-4183-af67-ee549f01ac36" />

</p>
<p>
Configure Help Topics (For when users create a ticket)--> Admin Panel --> Manage --> Help Topics. We are going to create several different topics depending on the situation.

  Help Topic information--> topic, Business critical outage--> parent topic, report a problem
  
  Help Topic information--> topic, Personal Computer Issures--> parent topic, report a problem
  
  Help Topic information--> topic, Equipment request --> parent topic, general inquiry
 
  Help Topic information--> topic, Password Reset--> parent topic, report a problem
  
  Help Topic information--> topic, other--> parent topic, general inquiry
</p>

This ends this part of the tutorial and I hope you found this helpful.
