## THỰC HÀNH 4: Quản lý Compartments (1 tiết)

**Mục tiêu:** Tạo cấu trúc cây thư mục (Compartments) để quản lý tài nguyên tách biệt giữa các môi trường.

### Bước 1: Truy cập quản lý Compartment
1. Vào menu chính $\rightarrow$ **Identity & Security** $\rightarrow$ **Compartments**.
2. Tại đây bạn sẽ thấy Compartment gốc (Root).

### Bước 2: Tạo cấu trúc Compartment con
Nhấn **Create Compartment** và tạo theo cấu trúc sau:

1. **Compartment Cha:** `Project_A`
   - *Description:* Compartment chính cho dự án A.
2. **Compartment Con (nằm trong Project_A):**
   - `Dev_Env`: Dành cho môi trường phát triển.
   - `Prod_Env`: Dành cho môi trường vận hành thực tế.

### Bước 3: Di chuyển tài nguyên (Nếu có)
* Chọn tài nguyên (như VM hoặc Database).
* Chọn **Move Resource** để chuyển tài nguyên vào đúng "phòng" (Compartment) đã tạo.

### Bước 4: Kiểm tra phân quyền theo Compartment
* Cập nhật Policy để giới hạn nhóm `developers` chỉ có quyền trong `Dev_Env`:
```sql
Allow group developers to manage all-resources in compartment Project_A:Dev_Env
