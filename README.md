---

## THỰC HÀNH 2: Cấu hình MFA (Multi-Factor Authentication)

**Mục tiêu:** Kích hoạt xác thực 2 yếu tố để bảo vệ tài khoản.

### Bước 1: Cài đặt ứng dụng Authenticator
Trên điện thoại cá nhân, cài đặt một trong các ứng dụng sau:
* **Google Authenticator** (iOS/Android)
* **Microsoft Authenticator** (iOS/Android)
* **Authy** (iOS/Android)

### Bước 2: Bật MFA cho User
Thực hiện các thao tác sau trên Console OCI:
1. Click vào **Profile Icon** (góc trên bên phải) $\rightarrow$ **My Profile**.
2. Tìm mục **Auth Tokens** $\rightarrow$ **MFA** $\rightarrow$ chọn **Enable Multi-Factor Authentication**.
3. Chọn loại: **Time-based One-Time Password (TOTP)**.
4. Dùng app Authenticator trên điện thoại để **Quét mã QR**.
5. App sẽ hiển thị mã 6 chữ số (thay đổi mỗi 30 giây).
6. Nhập mã vào Console để **Verify**.
7. **Lưu lại Recovery Codes** (cực kỳ quan trọng để dùng khi mất điện thoại).
8. Nhấn **Enable**.

### Bước 3: Kiểm tra (Test MFA)
1. **Logout** tài khoản.
2. **Login lại:** Sau khi nhập Password, hệ thống sẽ yêu cầu nhập **MFA code**.
3. Mở app trên điện thoại, lấy mã 6 số và nhập vào.
4. Đăng nhập thành công ✅.

### Bước 4: Quy trình khôi phục (Recovery)
*Trường hợp mất điện thoại hoặc không có MFA code:*
1. Tại trang Login, chọn **"I can't access my verification code"**.
2. Nhập **Recovery Code** đã lưu ở Bước 2.
3. Hệ thống sẽ cho phép **Disable MFA**.
4. Thiết lập lại MFA trên thiết bị mới.

---

### 🛡️ Best Practice cho MFA
- [x] Bật MFA cho **TẤT CẢ** users, đặc biệt là tài khoản Admin.
- [x] Lưu Recovery Codes ở nơi an toàn (như Password Manager).
- [x] Định kỳ kiểm tra lại quy trình khôi phục (Recovery process).
