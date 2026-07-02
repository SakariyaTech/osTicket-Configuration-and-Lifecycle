osTicket (Help Desk) Configuration and Ticket Lifecycle
=========================================================

### Description

This project continues from my [osTicket installation,](https://github.com/SakariyaTech/osTicket-Installation) covering post-installation configuration and simulating real support tickets from submission through resolution.

### Environments and Technologies Used

- Microsoft Azure (Virtual Machines, Networking)
- osTicket
- IIS / PHP / MySQL

### Operating Systems Used

- Windows 10

### High-Level Configuration Steps


**Step 1: Roles and Access Control**

<img width="1038" height="834" alt="image" src="https://github.com/user-attachments/assets/c274d839-885d-40ef-833d-aa7b549c732b" />

- Created a custom "Supreme Admin" role with full permissions across 
  tickets, tasks, and the knowledge base.
  

<img width="1221" height="456" alt="image" src="https://github.com/user-attachments/assets/c01aabee-1658-4fcf-a2e8-6f3d1af34e70" />


**Step 2: Departments and Teams**

- Set up departments (Support, System Admins) and teams (Level I 
  Support, Remote Access) to organize how tickets get routed and 
  escalated.

<img width="1075" height="259" alt="image" src="https://github.com/user-attachments/assets/2cae492f-0a1e-4c71-870c-093b78714660" />

<img width="1143" height="278" alt="image" src="https://github.com/user-attachments/assets/d87d4401-4a0a-4230-8bf6-587898d6b7a4" />


**Step 3: Agents**

- Created agent accounts and assigned each one a role, department, 
  and team.

<img width="1120" height="387" alt="image" src="https://github.com/user-attachments/assets/e5294c2a-a76c-40b0-b193-28e44caff682" />


**Step 4: Help Topics**

- Built out help topics to categorize incoming tickets (password 
  resets, equipment requests, business critical outages, etc.).

<img width="1301" height="617" alt="image" src="https://github.com/user-attachments/assets/d839c0ff-0103-48aa-bf42-a95814e95c57" />


**Step 5: SLA Plans**

- Configured four SLA tiers (Default, Sev-A, Sev-B, Sev-C) to control 
  response time expectations based on ticket priority.

<img width="1181" height="311" alt="image" src="https://github.com/user-attachments/assets/2602fe46-fd0d-4685-a2a9-2dcef587d269" />


**Step 6: User Registration Settings**

- Enabled ticket submission for unregistered users so anyone could 
  open a ticket without needing an account first.

### Ticket Lifecycle Simulation

Once configuration was complete, I simulated real support scenarios 
end-to-end to test the full workflow: submission, triage, SLA 
assignment, escalation, investigation, and resolution.

**Ticket #209160: Microsoft Office Activation Issue**

- Reported after multiple users got activation errors following an 
  update. Triaged and reassigned SLA, investigated as a server-side 
  sync issue, manually activated the affected users, and closed as 
  resolved.

<img width="927" height="343" alt="image" src="https://github.com/user-attachments/assets/709bef31-298b-4ea7-bebb-3f3b07e7d0f3" />

<img width="1293" height="809" alt="image" src="https://github.com/user-attachments/assets/c62bb379-4fe7-4fc9-b243-867f9adde612" />

<img width="1043" height="760" alt="image" src="https://github.com/user-attachments/assets/4fc11bb7-b29a-4e83-8a69-3796a6330d69" />


**Ticket #846596: VPN Not Working**

- Reported by a user unable to connect to the company VPN. Triaged 
  and escalated to the Remote Access team, who diagnosed a firewall 
  misconfiguration blocking the connection. Fixed the rule and closed 
  as resolved after user confirmation.

**Ticket #304028: Marketing Team Can't Send Emails**

- Reported by a marketing team member unable to send emails from a 
  shared mailbox. Investigated and identified an SMTP configuration 
  issue on the mailbox. Corrected the settings and closed as resolved 
  after user confirmation.

<img width="1047" height="272" alt="image" src="https://github.com/user-attachments/assets/fde95ab6-6680-4a53-8165-916bd1d24194" />
<img width="1230" height="356" alt="image" src="https://github.com/user-attachments/assets/6918a48b-15d2-4150-8a7c-165b4c8893fc" />

