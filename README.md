# Azure Active Directory Lab – VM Deployment & User Management

<!-- TOP IMAGE: Replace with your own screenshot of the lab overview or Azure Portal -->
<img width="1500" height="1001" alt="image" src="https://github.com/user-attachments/assets/f8b651ff-7521-44b5-9796-7f896defc82e" />




---

This repository documents a hands-on lab for **preparing Active Directory infrastructure in Microsoft Azure** and creating users with PowerShell.

---

## 1️⃣ Create Resource Group & Virtual Network

- Create a Resource Group for the AD lab  
- Create a Virtual Network inside the Resource Group  
- Both VMs (Domain Controller & Client) will be deployed in this network

<img width="1221" height="734" alt="image" src="https://github.com/user-attachments/assets/a02c8f69-5d86-4e90-9445-649c8531f0af" />


---

## 2️⃣ Deploy Domain Controller & Client VMs

- **Domain Controller (DC1):** Windows Server 2022  
- **Client Machine (Client1):** Windows 10  
- Both in the same Resource Group & Virtual Network

<img width="1624" height="863" alt="image" src="https://github.com/user-attachments/assets/8fbbed58-964e-4857-bbef-1bb8fa1a4c4c" />


---

## 3️⃣ Configure Domain Controller & Client

- Set DC1 private IP to **static**  
- Disable Windows Firewall on DC1 (for lab/testing)  
- On client, set DNS to DC1 private IP  
- Restart client to apply DNS changes  
- Test connectivity using `ping <DC-IP>`  
- Confirm DNS using `ipconfig /all`

<img width="549" height="163" alt="Screenshot 2026-03-04 141943" src="https://github.com/user-attachments/assets/c66ce408-4b0e-4161-a3a3-99b35f3b0835" />


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
