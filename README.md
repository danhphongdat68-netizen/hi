### Bước 2: Tạo IAM Users
1. Truy cập **Users** → **Create User**.
2. Tạo 3 người dùng: `alice.dev`, `bob.dba`, `charlie.auditor`.
3. Gán họ vào các nhóm tương ứng (`developers`, `dbadmins`, `readonly`).

### Bước 3: Tạo Policies (Chính sách)
Sử dụng **Manual Editor** để dán các câu lệnh phân quyền sau:

- **Policy 1 (Dev):** `Allow group developers to manage instance-family in compartment <your-compartment>`
- **Policy 2 (DBA):** `Allow group dbadmins to manage database-family in compartment <your-compartment>`
- **Policy 3 (Read):** `Allow group readonly to read all-resources in compartment <your-compartment>`
