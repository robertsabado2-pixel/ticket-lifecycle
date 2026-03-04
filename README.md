# 🖥 Active Directory Lab – Azure Step-by-Step

<!-- TOP IMAGE: Replace with your own screenshot of the lab overview or Azure Portal -->
📸 **Header Screenshot (Top of README)**  
👉 Screenshot could be Azure Portal showing the AD lab overview, Resource Group, or both VMs running.

![AD Lab Header](screenshots/REPLACE-header.png)

---

This repository documents a hands-on lab for **preparing Active Directory infrastructure in Microsoft Azure** and creating users with PowerShell.

---

## 1️⃣ Create Resource Group & Virtual Network

- Create a Resource Group for the AD lab  
- Create a Virtual Network inside the Resource Group  
- Both VMs (Domain Controller & Client) will be deployed in this network

📸 **Screenshot to Insert Below:**  
👉 Azure Portal showing Resource Group and Virtual Network overview

![Resource Group & VNet](screenshots/REPLACE-rg-vnet.png)

---

## 2️⃣ Deploy Domain Controller & Client VMs

- **Domain Controller (DC1):** Windows Server 2022  
- **Client Machine (Client1):** Windows 10  
- Both in the same Resource Group & Virtual Network

📸 **Screenshot to Insert Below:**  
👉 Azure Portal showing both VMs running

![VMs Screenshot](screenshots/REPLACE-vms.png)

---

## 3️⃣ Configure Domain Controller & Client

- Set DC1 private IP to **static**  
- Disable Windows Firewall on DC1 (for lab/testing)  
- On client, set DNS to DC1 private IP  
- Restart client to apply DNS changes  
- Test connectivity using `ping <DC-IP>`  
- Confirm DNS using `ipconfig /all`

📸 **Screenshot to Insert Below:**  
👉 Command Prompt on client showing successful ping to DC & DNS configuration

![DNS Verification Screenshot](screenshots/REPLACE-dns.png)

---

## 4️⃣ Enable Remote Desktop & Bulk User Creation

- Allow domain users to log into client via Remote Desktop  
- Open **PowerShell ISE as Administrator** on DC1  
- Run script to create multiple users in Active Directory under **Employees OU**  
- All users get default password “Password1”  
- Verify users in **Active Directory Users and Computers**  
- Test logins on client machine

📸 **Screenshot to Insert Below:**  
👉 Active Directory Users and Computers showing newly created users in Employees OU

![AD Users Screenshot](screenshots/REPLACE-ad-users.png)

---

## 5️⃣ Test Domain User Logins

- Log into client using a newly created domain user  
- Confirm a new user profile is created on first login  
- Lab is ready for further AD exercises

📸 **Screenshot to Insert Below:**  
👉 Client desktop showing successful login with a domain user account

![User Login Screenshot](screenshots/REPLACE-user-login.png)

---

# 💼 Skills Demonstrated

- Azure Resource Group & Virtual Network setup  
- Windows Server Deployment (Domain Controller)  
- Active Directory administration  
- DNS configuration and testing  
- PowerShell automation for bulk user creation  
- Remote Desktop configuration & testing  

---

# 🔧 Instructions for Screenshots

1. Create a folder in your repository called:

```bash
screenshots
```

2. Upload your images inside this folder.

3. Replace the `REPLACE-xxx.png` names in the README with your actual filenames.

> ⚠️ Keep the format: `![Description](screenshots/filename.png)`  
> Only replace the filename; do not remove the `![]()` syntax.
