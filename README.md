# PHẦN 2: THỰC HÀNH (4 tiết)

## THỰC HÀNH 1: Tạo và quản lý IAM Users, Groups (1 tiết)

**Mục tiêu:** Tạo users, groups, gán quyền

---

### Bước 1: Tạo IAM Groups

Thực hiện theo các bước sau trong Console:
1.  **Oracle Cloud Console**
2.  **Identity & Security** $\rightarrow$ **Domains** $\rightarrow$ **Default Domain**
3.  **Groups** $\rightarrow$ **Create Group**

**Danh sách Groups cần tạo:**

| Group Name (Name) | Description |
| :--- | :--- |
| **developers** | Development team members |
| **dbadmins** | Database administrators |
| **readonly** | Read-only access for auditors |

---

### Bước 2: Tạo IAM Users

Thực hiện theo các bước sau trong Console:
1.  **Users** $\rightarrow$ **Create User**

**Danh sách Users cần tạo:**

* **User 1:**
    * Username: `alice.dev`
    * Email: `alice@company.com`
    * Groups: `developers`
* **User 2:**
    * Username: `bob.dba`
    * Email: `bob@company.com`
    * Groups: `dbadmins`
* **User 3:**
    * Username: `charlie.auditor`
    * Email: `charlie@company.com`
    * Groups: `readonly`

> **Lưu ý:** Mỗi user sẽ nhận email để set password lần đầu.

---

### Bước 3: Tạo Policies (Chính sách)

**1. Policy 1: Developers có quyền quản lý VM**

Thực hiện:
1.  **Identity & Security** $\rightarrow$ **Policies** $\rightarrow$ **Create Policy**
2.  Name: `DevelopersComputeAccess`
3.  Description: `Allow developers to manage compute instances`
4.  Policy Builder $\rightarrow$ **Manual Editor**

**Policy statement:**
```sql
Allow group developers to manage instance-family in compartment <your-compartment>
Allow group developers to read virtual-network-family in compartment <your-compartment>
Allow group developers to use volume-family in compartment <your-compartment>
