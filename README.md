# Step 02 — Domain Controller Promotion (Windows Server 2019)

This repository documents the second stage of my cybersecurity home lab: installing Active Directory Domain Services (AD DS), configuring a static IP address, and promoting a Windows Server 2019 virtual machine to the first domain controller in a new forest (`lab.local`). This step establishes the core identity infrastructure that future lab components will rely on.

---

## 🔧 Objectives

- Rename the server to **DC01**
- Configure a **static IPv4 address**
- Install **Active Directory Domain Services (AD DS)**
- Create a new forest: **lab.local**
- Promote the server to a **domain controller**
- Verify successful domain creation and login

---

## 🖥️ Environment

- **Host Machine:** Windows (ThinkPad)
- **Hypervisor:** VirtualBox
- **Guest OS:** Windows Server 2019 (GUI)
- **Network:** Host‑only Adapter (`192.168.56.0/24`)

---

## 📝 Configuration Summary

### 1. Server Preparation
- Renamed server to **DC01**
- Rebooted to apply changes

### 2. Network Configuration
- Assigned static IP: `192.168.56.10`
- Subnet mask: `255.255.255.0`
- DNS server: `127.0.0.1` (self)

### 3. AD DS Installation
- Installed **Active Directory Domain Services**
- Launched domain controller promotion wizard

### 4. Domain Creation
- Created new forest: **lab.local**
- Configured domain/forest functional levels
- Enabled DNS and Global Catalog roles
- Set DSRM password

### 5. Verification
- Passed all prerequisite checks
- Server rebooted and displayed domain login screen
- Successfully logged in as **lab\Administrator**

---

## 📸 Screenshots

### 1. Server renamed to DC01  
<img width="398" height="492" alt="Server Rename" src="https://github.com/user-attachments/assets/6ff76d7c-2b19-4818-b60e-a7a0ce92cb48" />

### 2. Static IP configuration  
<img width="801" height="484" alt="Static IP Configuration" src="https://github.com/user-attachments/assets/d2bae2b0-5077-4ac4-8938-588118373044" />

### 3. AD DS role selected in Add Roles and Features  
<img width="753" height="517" alt="Server Roles - Active Directory Domain Services 1" src="https://github.com/user-attachments/assets/c0bd4091-6fcc-4e8d-ac53-025039d78341" />

<img width="787" height="561" alt="Server Roles - Active Directory Domain Services 2" src="https://github.com/user-attachments/assets/daf017fb-0b00-44dc-874f-fcfb94b46127" />

### 4. Domain promotion wizard — Add new forest (lab.local)  
<img width="773" height="568" alt="Deployment Configuration" src="https://github.com/user-attachments/assets/5637e4c0-0333-4027-9bc6-f5fb4a9676be" />

### 5. Domain Controller Options
<img width="778" height="582" alt="Domain Controller Options" src="https://github.com/user-attachments/assets/ce162b35-3471-415c-a923-398b5f4fdbd1" />

### 6. Prerequisites Check  
<img width="777" height="569" alt="Prerequisites Checks" src="https://github.com/user-attachments/assets/4d09c34c-6093-4eec-83d7-b5f070094e3b" />

### 7. Login screen showing `lab\Administrator`  
<img width="524" height="400" alt="Login Screen Showing Domain Promotion Success" src="https://github.com/user-attachments/assets/7361d773-f9b8-442d-a00d-a68d071c129c" />

---


## 📚 What I Learned

- How AD DS integrates DNS and identity services
- Why domain controllers require static IP addresses
- How forests, domains, and functional levels work together
- The purpose of the DSRM password
- How to troubleshoot common promotion warnings (e.g., DNS delegation)

---

## 🚀 Next Steps

**Step 03:**  
Create Organizational Units (OUs), security groups, and user accounts inside the new `lab.local` domain.

---

## 📂 Repository Structure


---

## 🏁 Status

✔️ Step 02 complete  
➡️ Moving on to domain structure and user provisioning


