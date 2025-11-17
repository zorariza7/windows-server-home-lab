# windows-server-home-lab
A documentation-based Windows Server practice lab simulating Active Directory, user management, permissions, and basic GPO concepts.
# Windows Server Home Lab  
A documentation-based simulation of a Windows Server environment.  
Includes Active Directory structure, user management, permissions, and basic GPO concepts.  
Designed for IT Support learning, portfolio use, and interview demonstration.

---

## 1. Lab Overview

This lab simulates a small organizational environment using Windows Server.  
The goal is to understand fundamental concepts such as:

- Active Directory (AD)
- Organizational Units (OU)
- User & Group Management
- File Share Permissions
- Basic Group Policy Objects (GPO)
- Login behavior testing

No physical server or virtualization required; this documentation reflects real-world configurations.

---

## 2. System Structure

| Component        | Description                            |
|------------------|----------------------------------------|
| Domain Controller | Windows Server (cloud/virtual/simulated) |
| Domain Name       | `al-ihsan.local`                      |
| OU Structure      | Departments & Security Groups         |
| Users             | Staff, Admin, and Student accounts    |

---

## 3. Active Directory Structure

al-ihsan.local │ ├── Admin │    ├── Admin-Group │    └── Admin-Users │ ├── Staff │    ├── Staff-Group │    └── Staff-Users │ └── Students ├── Student-Group └── Student-Users

---

## 4. User & Group Management

### Example User Accounts
| Username | Role         | Notes |
|----------|--------------|-------|
| admin01  | Admin        | Full privileges |
| staff01  | Staff        | Standard user |
| student01| Student      | Restricted access |

### Example Groups
- **Admin-Group** → Full access  
- **Staff-Group** → Read/write on staff directories  
- **Student-Group** → Restricted student share only  

---

## 5. File Share & Permissions

### Example Shares
| Share Name     | Access Level                         |
|----------------|---------------------------------------|
| `\\server\AdminShare`  | Admin only                      |
| `\\server\StaffShare`  | Staff group read/write          |
| `\\server\StudentShare`| Students read-only              |

This simulates role-based access control (RBAC).

---

## 6. Basic GPO (Group Policy Objects)

### Example GPOs
1. **Password Policy**
   - Minimum 8 characters  
   - Lockout after 3 failed attempts  

2. **User Restrictions**
   - Hide control panel for students  
   - Disable USB storage for students  

3. **Login Banner (Legal Notice)**
   - Custom message displayed before login

---

## 7. Login Behavior Testing

Simulated scenarios:
- Staff user tries accessing StudentShare → Allowed  
- Student user tries accessing StaffShare → Blocked  
- Student restricted from Control Panel → Success  
- USB disabled for Students → Confirmed  

---

## 8. Future Expansion Ideas

- DHCP server configuration  
- DNS zones & records  
- Roaming profiles  
- Folder redirection  
- Multi-DC environment  
- Windows + Linux hybrid AD integration  

---

## 9. Notes

This project is documentation-based.  
It demonstrates understanding of Windows Server fundamentals without requiring a running physical lab.


---
