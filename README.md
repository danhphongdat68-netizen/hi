# Hướng dẫn Thực hành: Quản lý IAM trên OCI

## 1. Các bước thực hiện
- **Bước 1:** Tạo IAM Groups (`developers`, `dbadmins`, `readonly`).
- **Bước 2:** Tạo IAM Users và gán vào các nhóm tương ứng.
- **Bước 3:** Thiết lập Policies (Chính sách quyền hạn).

## 2. Chi tiết Policies
- **Developers:** Quyền quản lý Instance (VM).
- **DBAdmins:** Quyền quản lý Database.
- **ReadOnly:** Chỉ có quyền xem tài nguyên.

## 3. Kết quả kiểm tra
- `alice.dev` tạo được VM nhưng không xóa được DB (Đúng).
- `charlie.auditor` xem được danh sách nhưng không tạo được VM (Đúng).

> [!TIP]
> Luôn bật MFA và không dùng Root account cho công việc hằng ngày để đảm bảo bảo mật!
