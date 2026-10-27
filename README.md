# Active Directory Lab
## Overview
•	Built a Windows Server 2025 domain controller in VMware.

•	Practiced common help desk tasks: user accounts, groups, password resets, account lockouts, account disabling, and folder access controls.

## Environment
•	VMware Workstation

•	Windows Server 2025

•	Active Directory Domain Services

•	Domain: Control.local

### 1. Domain Setup

•	Installed Windows Server 2025.

•	Set a static IP address.

•	Installed Active Directory Domain Services.

•	Promoted the server to a domain controller (Control.local).

<img width="797" height="592" alt="Screenshot 2026-10-26 053703" src="https://github.com/user-attachments/assets/bbacd8af-893c-4e02-930d-7361318c40aa" />

### 2. User Accounts

•	Created OUs for HR, Sales, and IT.

•	Created user accounts in each OU.

<img width="797" height="599" alt="Screenshot 2026-10-26 045112" src="https://github.com/user-attachments/assets/cf219454-3537-423a-b5f1-9bf877b14381" />

<img width="797" height="598" alt="Screenshot 2026-10-26 045147" src="https://github.com/user-attachments/assets/3d767ca9-925a-4012-b646-c86d885e6676" />

<img width="797" height="596" alt="Screenshot 2026-10-26 045212" src="https://github.com/user-attachments/assets/e5b6e73c-0335-448c-9158-6ce8722ce4f9" />


### 3. Security Groups

•	Created HR-Staff, Sales-Staff, and IT-Staff groups.

<img width="798" height="597" alt="Screenshot 2026-10-26 045326" src="https://github.com/user-attachments/assets/6423220d-3032-46bf-a945-16b0069c3e48" />

•	Added users to their department groups.

•	Moved a user from one group to another to simulate a department transfer.

<img width="798" height="599" alt="Screenshot 2026-10-26 045349" src="https://github.com/user-attachments/assets/9f249ee9-aaf8-4dd6-bfc4-0d55386e1945" />

### 4. Password Reset

•	Reset a user's password in Active Directory Users and Computers.

<img width="798" height="599" alt="Screenshot 2026-10-26 045411" src="https://github.com/user-attachments/assets/86f16f0e-b510-4227-b249-c43589a2b198" />

•	Required the user to change the password at next logon.

<img width="797" height="602" alt="Screenshot 2026-10-26 061809" src="https://github.com/user-attachments/assets/35740934-b843-4382-8b4b-1197498b32fe" />

### 5. Account Lockout Policy

•	Edited the Default Domain Policy in Group Policy Management.

•	Set the account lockout threshold to 3 invalid attempts.

<img width="797" height="599" alt="Screenshot 2026-10-26 045433" src="https://github.com/user-attachments/assets/a8e153ba-e474-44a3-8655-8b17cc0ac74e" />

•	Applied the policy with gpupdate /force.

<img width="576" height="125" alt="Screenshot 2026-10-26 061527" src="https://github.com/user-attachments/assets/83736876-3b98-428b-9fc8-4d44d5a9d704" />

### 6. Lock and Unlock an Account

•	Entered a wrong password 3 times using runas to lock the account.

<img width="798" height="598" alt="Screenshot 2026-10-26 045455" src="https://github.com/user-attachments/assets/cfad7aab-0862-40bb-bdf7-4112287d21a4" />

•	Unlocked the account from the user's Account tab.

<img width="797" height="597" alt="Screenshot 2026-10-26 045536" src="https://github.com/user-attachments/assets/23d99f74-d5ea-4f44-8dc3-b5439479e422" />


### 7. Disable an Account

•	Disabled the account of a user who left the company.

<img width="797" height="596" alt="Screenshot 2026-10-26 045552" src="https://github.com/user-attachments/assets/4c147c5f-6846-4c5f-8833-a60a656dc37f" />

### 8. Basic Access Controls

•	Created HR, Sales, and IT folders under C:\CompanyShares.

<img width="789" height="594" alt="Screenshot 2026-10-27 071546" src="https://github.com/user-attachments/assets/2ca38c97-6500-498b-88ef-15d579f3a0d6" />

•	Shared each folder with Authenticated Users (Change).

<img width="789" height="592" alt="Screenshot 2026-10-27 071750" src="https://github.com/user-attachments/assets/87021f89-b3d6-4e81-9c73-6cac3251c78d" />

•	Disabled inheritance and removed general Users access on each folder.

•	Gave each department's group (HR-Staff, Sales-Staff, IT-Staff) Modify access to its own folder.

<img width="790" height="554" alt="Screenshot 2026-10-27 071854" src="https://github.com/user-attachments/assets/cc91b40b-5c7b-4811-bf91-4672f4763b35" />

•	Used the Effective Access tab to confirm department users could open their folder and other users could not.

<img width="788" height="593" alt="Screenshot 2026-10-27 071917" src="https://github.com/user-attachments/assets/791b0848-545b-4cf8-b73b-d67a58f777d6" />

<img width="788" height="592" alt="Screenshot 2026-10-27 071938" src="https://github.com/user-attachments/assets/d50322c8-7ac4-4e22-bf1c-9e8ba158fd8f" />

### Takeaways
•	Active Directory organizes users, groups, and departments in one central place.

•	Groups make managing access easier than setting permissions for one user at a time.

•	Group Policy applies security rules across the whole domain.

•	Account lockout protects against password guessing.

•	Disabling an account is safer than deleting it when someone leaves.

•	Least privilege means users only get access to what they need for their job.

## Final Outcome
I built a working Active Directory domain on Windows Server 2025 and used it to complete the account and access tasks a help desk technician handles every day: creating users, managing groups, resetting passwords, enforcing a lockout policy, unlocking accounts, disabling accounts, and controlling folder access with security groups. This lab gave me hands-on experience with the tools and workflow used in real IT support roles.
