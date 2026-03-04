# 🛠 Azure Active Directory & osTicket Lab

This repository documents my hands-on IT lab work deploying Active Directory infrastructure and installing osTicket in Microsoft Azure.

These labs demonstrate foundational system administration, networking, identity management, and web server configuration skills.

---

# 📁 Lab 1 – Active Directory Infrastructure in Azure

## 📌 Project Overview

In this lab, I built a foundational Active Directory environment inside Microsoft Azure.

### Objectives

- Create a Resource Group and Virtual Network
- Deploy a Domain Controller (Windows Server 2022)
- Deploy a Client Machine (Windows 10)
- Configure Static IP addressing
- Configure DNS settings
- Verify client-to-domain controller connectivity

---

## 🖥 Environment Setup

- **Cloud Provider:** Microsoft Azure  
- **Domain Controller:** Windows Server 2022 (DC-1)  
- **Client Machine:** Windows 10 Pro (client-1)  
- **Network:** Custom Virtual Network inside Resource Group  

---

## 📸 Screenshots

### 1️⃣ Resource Group & Virtual Network
![Resource Group](screenshots/ad-resourcegroup.png)

---

### 2️⃣ Domain Controller VM
![DC-1 VM](screenshots/ad-dc1.png)

---

### 3️⃣ Client VM
![Client-1 VM](screenshots/ad-client1.png)

---

### 4️⃣ Static Private IP Configuration
![Static IP](screenshots/ad-static-ip.png)

---

### 5️⃣ Client DNS Configuration
![DNS Configuration](screenshots/ad-dns-config.png)

---

### 6️⃣ Ping Test (Client → DC)
![Ping Test](screenshots/ad-ping-test.png)

---

### 7️⃣ ipconfig Verification
![IP Config](screenshots/ad-ipconfig.png)

---

## 🔎 Key Takeaways

- Proper DNS configuration is critical for domain joining.
- Static IP addressing ensures reliable domain controller communication.
- Network configuration issues are the most common cause of AD failures.
- Azure infrastructure setup mirrors on-premise enterprise environments.

---

# 👥 Lab 2 – Active Directory Bulk User Creation (PowerShell)

## 📌 Project Overview

This lab demonstrates bulk Active Directory user creation using PowerShell scripting.

### Objectives

- Enable Domain Users to log into client machines
- Use PowerShell ISE to create multiple AD users
- Assign default passwords
- Verify successful domain login

---

## 🛠 Tools Used

- Active Directory Users and Computers
- PowerShell ISE
- Windows Server 2022
- Windows 10 Client VM

---

## 📸 Screenshots

### 1️⃣ Remote Desktop Permissions
![Remote Desktop Users](screenshots/ad-remote-users.png)

---

### 2️⃣ PowerShell Script
![PowerShell Script](screenshots/ad-powershell-script.png)

---

### 3️⃣ Users Created in AD
![Users Created](screenshots/ad-users-created.png)

---

### 4️⃣ Successful Domain Login
![User Login](screenshots/ad-user-login.png)

---

## 🔎 Key Takeaways

- PowerShell allows scalable user provisioning.
- Organizational Units (OUs) must match script configuration exactly.
- Default passwords should always be changed in production environments.
- Group Policy is preferred for managing permissions at scale.

---

# 🎫 Lab 3 – osTicket Installation in Azure (Helpdesk Simulation)

## 📌 Project Overview

In this lab, I deployed a Windows 10 VM in Azure and installed the open-source ticketing system **osTicket** to simulate a real-world helpdesk environment.

### Objectives

- Deploy Windows 10 VM
- Install IIS Web Server with CGI
- Install PHP & configure IIS integration
- Install MySQL 5.5 database server
- Configure database access
- Deploy and configure osTicket
- Complete web-based installation
- Access Admin and User portals

---

## 🛠 Technologies Used

- Microsoft Azure
- Windows 10
- IIS (Internet Information Services)
- PHP
- MySQL 5.5
- HeidiSQL
- osTicket (Open Source Ticketing System)

---

## 📸 Screenshots

### 1️⃣ Azure VM Created
![VM Created](screenshots/osticket-vm-created.png)

---

### 2️⃣ VM Specifications
![VM Specs](screenshots/osticket-vm-specs.png)

---

### 3️⃣ IIS Installed
![IIS Installed](screenshots/osticket-iis-installed.png)

---

### 4️⃣ IIS Default Page Working
![IIS Working](screenshots/osticket-iis-working.png)

---

### 5️⃣ PHP Manager Installed
![PHP Manager](screenshots/osticket-php-manager.png)

---

### 6️⃣ MySQL Installed
![MySQL Installed](screenshots/osticket-mysql-installed.png)

---

### 7️⃣ HeidiSQL Connected
![HeidiSQL](screenshots/osticket-heidisql.png)

---

### 8️⃣ osTicket Database Created
![Database Created](screenshots/osticket-database-created.png)

---

### 9️⃣ osTicket Files in IIS Web Root
![Files](screenshots/osticket-files.png)

---

### 🔟 PHP Extensions Enabled
![PHP Extensions](screenshots/osticket-php-extensions.png)

---

### 1️⃣1️⃣ File Permissions Configured
![Permissions](screenshots/osticket-permissions.png)

---

### 1️⃣2️⃣ osTicket Web Installer
![Web Installer](screenshots/osticket-web-install.png)

---

### 1️⃣3️⃣ Admin Dashboard
![Admin Dashboard](screenshots/osticket-admin-dashboard.png)

---

### 1️⃣4️⃣ User Portal
![User Portal](screenshots/osticket-user-portal.png)

---

## 🔎 Key Takeaways

- Web applications require proper dependency management (PHP, MySQL, IIS).
- File permissions are critical for application security.
- Database configuration errors are a common troubleshooting point.
- osTicket simulates real-world helpdesk environments used in IT support roles.

---

# 🎯 Skills Demonstrated

- Azure Virtual Machine Deployment
- Active Directory Administration
- DNS Configuration
- PowerShell Scripting
- Windows Server Management
- IIS Web Server Configuration
- Database Installation & Management
- Helpdesk Ticketing System Deployment
- Troubleshooting & System Integration

---

# 🚀 Next Steps

Future improvements:

- Implement Group Policy Objects (GPOs)
- Configure domain joining for additional clients
- Harden server security settings
- Configure email integration for osTicket
- Simulate real helpdesk ticket workflows

---

📌 This repository is part of my ongoing IT and Cybersecurity hands-on lab training.
