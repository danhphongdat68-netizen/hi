# BÁO CÁO BÀI TẬP THỰC HÀNH: QUẢN LÝ IAM TRÊN OCI

**Họ và tên:** [Danh Đạt]  
**Mã số sinh viên:** [33407CNTT]  
**Lớp:** [2404CNTT]

---

## 1. Kết quả tạo Groups và Users
Tôi đã khởi tạo thành công các nhóm và người dùng trong Default Domain.

* **Groups:** `developers`, `dbadmins`, `readonly`.
* **Users:** `alice.dev`, `bob.dba`, `charlie.auditor`.

> **[HÀNH ĐỘNG]:** Bạn hãy chụp ảnh màn hình danh sách Users trên OCI của bạn, sau đó kéo và thả trực tiếp tấm ảnh đó vào dòng này trong trình soạn thảo GitHub. Nó sẽ tự hiện mã ảnh dạng `![image](...)`.

---

## 2. Thiết lập Policies (Chính sách)
Tôi đã cấu hình các quyền hạn cụ thể bằng Manual Editor:

```sql
-- Quyền cho nhóm Developers
Allow group developers to manage instance-family in compartment <your-compartment>

-- Quyền cho nhóm DBAdmins
Allow group dbadmins to manage database-family in compartment <your-compartment>

-- Quyền cho nhóm ReadOnly
Allow group readonly to read all-resources in compartment <your-compartment>
