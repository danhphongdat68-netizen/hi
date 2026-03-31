---

## THỰC HÀNH 3: Quản lý chi phí với Budgets (1 tiết)

**Mục tiêu:** Tạo ngân sách dự kiến và thiết lập cảnh báo khi chi phí vượt ngưỡng.

### Bước 1: Truy cập thiết lập Budget
1. Mở menu chính (ba dấu gạch ngang) $\rightarrow$ **Billing & Cost Management**.
2. Chọn mục **Budgets** $\rightarrow$ Nhấn nút **Create Budget**.

### Bước 2: Thiết lập thông số ngân sách
* **Name:** `Monthly_Limit_50` (Ví dụ: Giới hạn 50$).
* **Target Compartment:** Chọn Compartment của bạn (hoặc Root).
* **Budget Amount:** Nhập số tiền giới hạn (Ví dụ: `50`).
* **Day of month to begin:** `1` (Bắt đầu từ ngày đầu tháng).

### Bước 3: Thiết lập cảnh báo (Alerts)
Thiết lập để hệ thống gửi Email khi chi phí chạm ngưỡng:
1. **Threshold Type:** Percentage (Phần trăm).
2. **Threshold Metric:** Actual Cost (Chi phí thực tế).
3. **Threshold Percentage:** `80%` (Cảnh báo khi dùng hết 80% ngân sách).
4. **Email Recipients:** Nhập địa chỉ email của bạn.
5. **Message:** `Cảnh báo: Chi tiêu Cloud đã chạm mức 80%!`

### Bước 4: Kiểm tra và Quản lý
* Sau khi nhấn **Create**, danh sách Budget sẽ hiện ra với thanh trạng thái màu sắc.
* **Màu xanh:** Chi tiêu an toàn.
* **Màu đỏ:** Đã vượt ngưỡng thiết lập.

---

## 🏁 TỔNG KẾT BÀI THỰC HÀNH
Qua 3 bài thực hành, tôi đã nắm vững:
1. Cách phân quyền an toàn với **IAM Users & Groups**.
2. Cách bảo vệ tài khoản tối đa với **MFA**.
3. Cách kiểm soát túi tiền, tránh phát sinh chi phí ngoài ý muốn với **Budgets**.
