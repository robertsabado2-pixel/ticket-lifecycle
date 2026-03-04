
# 🛠 Azure Active Directory & osTicket Lab

This project demonstrates hands-on experience deploying core IT infrastructure in Microsoft Azure.

---

## 1️⃣ Active Directory Infrastructure Setup

- Created Resource Group and Virtual Network
- Deployed Domain Controller (Windows Server 2022)
- Deployed Windows 10 Client VM
- Configured static IP for DC
- Configured DNS and verified connectivity

📸 **Screenshot to Insert Below:**  
👉 Azure Portal showing BOTH VMs (DC-1 and client-1) running inside the same Resource Group.

![AD Infrastructure Screenshot](screenshots/REPLACE-ad-infrastructure.png)

---

## 2️⃣ DNS & Network Configuration

- Set DC private IP to Static
- Configured Client DNS to point to DC
- Restarted client to apply changes
- Verified connectivity using `ping`
- Confirmed DNS using `ipconfig /all`

📸 **Screenshot to Insert Below:**  
👉 Command Prompt on client-1 showing successful `ping` to DC and `ipconfig /all` showing DNS = DC private IP.

![DNS Verification Screenshot](screenshots/REPLACE-dns-verification.png)

---

## 3️⃣ Active Directory User Creation (PowerShell)

- Enabled Domain Users for Remote Desktop access
- Used PowerShell ISE to bulk-create users
- Verified users in Active Directory Users and Computers
- Assigned default passwords (lab environment)
- Successfully tested domain login

📸 **Screenshot to Insert Below:**  
👉 Active Directory Users and Computers window showing multiple created users inside Employees OU.

![AD Users Screenshot](screenshots/REPLACE-ad-users.png)

---

## 4️⃣ IIS & Database Configuration (osTicket)

- Installed IIS with CGI
- Installed PHP and configured IIS integration
- Installed MySQL 5.5
- Created osTicket database using HeidiSQL
- Enabled required PHP extensions (IMAP, International, OPCache)

📸 **Screenshot to Insert Below:**  
👉 IIS Manager open OR HeidiSQL showing the created "osTicket" database.

![IIS or Database Screenshot](screenshots/REPLACE-osticket-database.png)

---

## 5️⃣ osTicket Installation & Verification

- Copied osTicket files into IIS web root
- Configured file permissions
- Completed web-based installer
- Configured admin account
- Verified Admin Dashboard and User Portal access

📸 **Screenshot to Insert Below:**  
👉 osTicket Admin Dashboard after successful installation.

![osTicket Dashboard Screenshot](screenshots/REPLACE-osticket-dashboard.png)

---

# 💼 Skills Demonstrated

- Azure Virtual Machine Deployment
- Active Directory Administration
- DNS & Network Configuration
- PowerShell Automation
- IIS Web Server Setup
- Database Installation & Management
- Helpdesk Ticketing System Deployment
- Troubleshooting & System Integration
