# Phiếu Bài Tập Tự Làm & Vận Dụng — Bài 2: Lập trình Python Cơ bản trong Kinh doanh
## Học phần: Khoa học Dữ liệu Cơ bản trong Kinh tế & Kinh doanh (FDA.6.1.2.01.V) — NEU

> **Thời gian làm bài gợi ý:** 60 – 90 phút  
> **Quy mô:** 10 bài tập lập trình lớn · **Tổng điểm:** 100 điểm (10 điểm/bài)  
> **Tệp giao diện tự chấm trực tuyến:** [`bai-2-bai-tap-tu-lam.html`](./bai-2-bai-tap-tu-lam.html)  
> **Tài liệu học tập nguồn:** `Bài 2_Giới thiệu ngôn ngữ lập trình Python_B1.pdf` (32 trang)

---

## 📊 Cấu trúc ma trận bài tập thực hành (10 bài - 100 điểm)

| STT | Mã bài | Tên bài tập | Nhóm nghiệp vụ | Thang điểm | Nội dung kỹ thuật trọng tâm |
| :---: | :---: | :--- | :---: | :---: | :--- |
| 1 | `p01` | **Tính hóa đơn và giảm giá** | Bán hàng | **10 điểm** | Khai báo biến, phép nhân, trừ số học, ép kiểu int() khi in |
| 2 | `p02` | **Hóa đơn có thuế và phí giao hàng** | Bán hàng | **10 điểm** | Ép kiểu chuỗi sang int(), tính thuế suất thập phân, làm tròn số |
| 3 | `p03` | **Doanh thu, chi phí và lợi nhuận** | Lợi nhuận | **10 điểm** | Nhân đơn giá và sản lượng, tính tổng chi phí và lợi nhuận gộp |
| 4 | `p04` | **Tính biên lợi nhuận tháng** | Lợi nhuận | **10 điểm** | Chia thực /, tính tỷ lệ phần trăm, hàm round() làm tròn thập phân |
| 5 | `p05` | **Kiểm kê và nhu cầu nhập hàng** | Tồn kho | **10 điểm** | Toán tử chia nguyên // và chia dư % để đóng gói combo hàng |
| 6 | `p06` | **Cập nhật danh sách hàng hóa** | Tồn kho | **10 điểm** | Cấu trúc danh sách list, tính biến đổi (mutability) và gán đè theo chỉ số |
| 7 | `p07` | **Đo chi phí chuyển đổi và ROAS** | Marketing | **10 điểm** | Phép chia thực, tính chỉ số Marketing CPA và ROAS doanh thu/chi phí |
| 8 | `p08` | **So sánh hai kênh quảng cáo** | Marketing | **10 điểm** | Toán tử so sánh logic >, == giữa hai số liệu hiệu quả chiến dịch |
| 9 | `p09` | **Tính lương và kiểm tra quỹ lương** | Nhân sự | **10 điểm** | Nhân hệ số lương, điều kiện logic bool so sánh ngân sách quỹ lương |
| 10 | `p10` | **Thống kê danh sách nhân viên** | Nhân sự | **10 điểm** | Thao tác trên list: hàm len(), chỉ số phần tử đầu [0] và phần tử cuối [-1] |
| | | **TỔNG CỘNG** | | **100 điểm** | **10 bài thực hành lập trình Python nghiệp vụ** |

---

## 📝 Chi tiết 10 bài tập tự làm

## Bài 01. Tính hóa đơn và giảm giá
- **Mã bài tập:** `p01` | **Nhóm chuyên môn:** `Bán hàng` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:**  
> NeuTech Coffee bán cà phê sữa và trà đào. Quán giảm một tỷ lệ cố định cho hóa đơn; hãy tính đúng số tiền thanh toán.

### Yêu cầu thực hiện:
1. Tính tổng trước giảm và lưu vào biến tong_goc.
2. Tính số tiền giảm vào muc_giam.
3. Tính tiền phải trả vào thanh_toan.
4. Dùng print() in đúng mẫu: Thanh toán: 137700 (số nguyên, không có chữ VNĐ).

### Đầu ra mẫu cần đạt:
```text
Thanh toán: 137700
```

### Tiêu chí chấm điểm (10 điểm):
- **Tổng tiền trước giảm** (`tong_goc`): `2 điểm`
- **Mức giảm** (`muc_giam`): `2 điểm`
- **Tiền thanh toán** (`thanh_toan`): `3 điểm`
- **Đầu ra theo mẫu** (`__output__`): `3 điểm`

### Mã nguồn khởi đầu (Điền vào chỗ trống `...`):
```python
# DỮ LIỆU ĐẦU VÀO MẪU (ĐÃ CHO)
gia_sua = 25000
so_sua = 3
gia_tra = 39000
so_tra = 2
ty_le_giam = 0.1
# === KẾT THÚC DỮ LIỆU MẪU ===

# PHẦN SINH VIÊN VIẾT TIẾP (ĐIỀN VÀO CHỖ TRỐNG ...)
# Yêu cầu 1: Tính tổng tiền trước khi giảm (giá sữa * số sữa + giá trà * số trà)
tong_goc = gia_sua * ... + gia_tra * ...

# Yêu cầu 2: Tính số tiền được giảm theo tỷ lệ giảm (tong_goc * ty_le_giam)
muc_giam = tong_goc * ...

# Yêu cầu 3: Tính số tiền thực tế phải thanh toán sau khi trừ mức giảm
thanh_toan = tong_goc - ...

# Yêu cầu 4: In kết quả theo đúng mẫu: Thanh toán: 137700 (lưu ý dùng int())
print("Thanh toán:", int(...))
```

> 💡 **Gợi ý phương pháp:** Có thể dùng int() khi in; tỷ lệ giảm là số thập phân như 0.1.

---

## Bài 02. Hóa đơn có thuế và phí giao hàng
- **Mã bài tập:** `p02` | **Nhóm chuyên môn:** `Bán hàng` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:**  
> Một cửa hàng nhận đơn qua ứng dụng. Đơn giá và số lượng được hệ thống gửi về dưới dạng chuỗi; cần chuyển thành số trước khi tính.

### Yêu cầu thực hiện:
1. Chuyển don_gia và so_luong thành số rồi tính tien_hang.
2. Tính tien_thue theo thue_suat trên tiền hàng.
3. Tính tong_hoa_don gồm tiền hàng, thuế và phí giao hàng.
4. In đúng mẫu: Tổng hóa đơn: 128400 (sử dụng round() hoặc int() với dữ liệu hiện tại).

### Đầu ra mẫu cần đạt:
```text
Tổng hóa đơn: 128400
```

### Tiêu chí chấm điểm (10 điểm):
- **Tiền hàng** (`tien_hang`): `2 điểm`
- **Tiền thuế** (`tien_thue`): `2 điểm`
- **Tổng hóa đơn** (`tong_hoa_don`): `3 điểm`
- **Đầu ra theo mẫu** (`__output__`): `3 điểm`

### Mã nguồn khởi đầu (Điền vào chỗ trống `...`):
```python
# DỮ LIỆU ĐẦU VÀO MẪU (ĐÃ CHO)
don_gia = "35000"
so_luong = "3"
phi_giao = 15000
thue_suat = 0.08
# === KẾT THÚC DỮ LIỆU MẪU ===

# PHẦN SINH VIÊN VIẾT TIẾP (ĐIỀN VÀO CHỖ TRỐNG ...)
# Yêu cầu 1: Chuyển don_gia và so_luong từ chuỗi sang số nguyên int() rồi tính tien_hang
tien_hang = int(...) * int(...)

# Yêu cầu 2: Tính tiền thuế theo thuế suất trên tiền hàng (tien_hang * thue_suat)
tien_thue = ... * ...

# Yêu cầu 3: Tính tổng hóa đơn gồm tiền hàng, tiền thuế và phí giao hàng
tong_hoa_don = tien_hang + ... + ...

# Yêu cầu 4: In ra màn hình theo đúng mẫu: Tổng hóa đơn: 128400 (dùng round() hoặc int())
print("Tổng hóa đơn:", round(...))
```

> 💡 **Gợi ý phương pháp:** int("35000") = 35000; thuế chỉ tính trên tiền hàng, không tính trên phí giao.

---

## Bài 03. Doanh thu, chi phí và lợi nhuận
- **Mã bài tập:** `p03` | **Nhóm chuyên môn:** `Lợi nhuận` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:**  
> Một quầy đồ uống bán một loại sản phẩm trong ngày. Biết doanh số, giá bán và chi phí biến đổi mỗi ly; cần tính lợi nhuận sau chi phí cố định.

### Yêu cầu thực hiện:
1. Tính doanh_thu = số ly × giá bán.
2. Tính chi_phi gồm chi phí biến đổi và chi phí cố định.
3. Tính loi_nhuan = doanh thu − chi phí.
4. In đúng mẫu: Lợi nhuận: 155000.

### Đầu ra mẫu cần đạt:
```text
Lợi nhuận: 155000
```

### Tiêu chí chấm điểm (10 điểm):
- **Doanh thu** (`doanh_thu`): `2 điểm`
- **Tổng chi phí** (`chi_phi`): `2 điểm`
- **Lợi nhuận** (`loi_nhuan`): `3 điểm`
- **Đầu ra theo mẫu** (`__output__`): `3 điểm`

### Mã nguồn khởi đầu (Điền vào chỗ trống `...`):
```python
# DỮ LIỆU ĐẦU VÀO MẪU (ĐÃ CHO)
so_ly = 25
gia_ban = 30000
chi_phi_moi_ly = 15000
chi_phi_co_dinh = 220000
# === KẾT THÚC DỮ LIỆU MẪU ===

# PHẦN SINH VIÊN VIẾT TIẾP (ĐIỀN VÀO CHỖ TRỐNG ...)
# Yêu cầu 1: Tính tổng doanh thu trong ngày (số ly * giá bán)
doanh_thu = so_ly * ...

# Yêu cầu 2: Tính tổng chi phí (chi phí biến đổi của các ly + chi phí cố định)
chi_phi = so_ly * ... + ...

# Yêu cầu 3: Tính lợi nhuận trong ngày (doanh thu trừ chi phí)
loi_nhuan = ... - ...

# Yêu cầu 4: In kết quả theo đúng mẫu: Lợi nhuận: 155000
print("Lợi nhuận:", ...)
```

> 💡 **Gợi ý phương pháp:** Chi phí biến đổi = số ly × chi phí nguyên liệu của mỗi ly.

---

## Bài 04. Tính biên lợi nhuận tháng
- **Mã bài tập:** `p04` | **Nhóm chuyên môn:** `Lợi nhuận` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:**  
> Một doanh nghiệp tổng hợp doanh thu tháng và bốn nhóm chi phí. Hãy đánh giá biên lợi nhuận bằng phép toán số học.

### Yêu cầu thực hiện:
1. Tính tổng chi phí trong biến tong_chi.
2. Tính loi_nhuan.
3. Tính ty_suat phần trăm = lợi nhuận / doanh thu × 100.
4. In: Biên lợi nhuận (%): 20.0 (làm tròn hai chữ số thập phân bằng round()).

### Đầu ra mẫu cần đạt:
```text
Biên lợi nhuận (%): 20.0
```

### Tiêu chí chấm điểm (10 điểm):
- **Tổng chi phí** (`tong_chi`): `2 điểm`
- **Lợi nhuận** (`loi_nhuan`): `2 điểm`
- **Tỷ suất lợi nhuận** (`ty_suat`): `3 điểm`
- **Đầu ra theo mẫu** (`__output__`): `3 điểm`

### Mã nguồn khởi đầu (Điền vào chỗ trống `...`):
```python
# DỮ LIỆU ĐẦU VÀO MẪU (ĐÃ CHO)
doanh_thu_thang = 200000000
nguyen_lieu = 70000000
tien_luong = 55000000
mat_bang = 20000000
chi_phi_khac = 15000000
# === KẾT THÚC DỮ LIỆU MẪU ===

# PHẦN SINH VIÊN VIẾT TIẾP (ĐIỀN VÀO CHỖ TRỐNG ...)
# Yêu cầu 1: Tính tổng các khoản chi phí (nguyên liệu, tiền lương, mặt bằng, chi phí khác)
tong_chi = nguyen_lieu + ... + ... + ...

# Yêu cầu 2: Tính lợi nhuận tháng (doanh thu tháng trừ tổng chi phí)
loi_nhuan = doanh_thu_thang - ...

# Yêu cầu 3: Tính tỷ suất lợi nhuận (%) = lợi nhuận / doanh thu tháng * 100
ty_suat = ... / ... * 100

# Yêu cầu 4: In kết quả theo mẫu: Biên lợi nhuận (%): 20.0 (làm tròn 2 chữ số bằng round())
print("Biên lợi nhuận (%):", round(..., 2))
```

> 💡 **Gợi ý phương pháp:** Tỷ suất có thể âm khi lỗ. Dùng round(ty_suat, 2) khi in.

---

## Bài 05. Kiểm kê và nhu cầu nhập hàng
- **Mã bài tập:** `p05` | **Nhóm chuyên môn:** `Tồn kho` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:**  
> Quản lý cửa hàng cần cập nhật số lượng tồn kho sau khi nhập và bán trong ngày. Cửa hàng muốn biết cần nhập thêm bao nhiêu đơn vị để đáp ứng nhu cầu dự kiến.

### Yêu cầu thực hiện:
1. Tính ton_cuoi = tồn đầu + nhập mới − đã bán.
2. Tính can_nhap = max(0, nhu cầu dự kiến − tồn cuối).
3. Tạo biến du_hang (bool) cho biết tồn cuối đã đủ nhu cầu.
4. In: Cần nhập thêm: 35.

### Đầu ra mẫu cần đạt:
```text
Cần nhập thêm: 35
```

### Tiêu chí chấm điểm (10 điểm):
- **Tồn cuối** (`ton_cuoi`): `2 điểm`
- **Nhu cầu nhập thêm** (`can_nhap`): `3 điểm`
- **Đủ hàng (bool)** (`du_hang`): `2 điểm`
- **Đầu ra theo mẫu** (`__output__`): `3 điểm`

### Mã nguồn khởi đầu (Điền vào chỗ trống `...`):
```python
# DỮ LIỆU ĐẦU VÀO MẪU (ĐÃ CHO)
ton_dau = 65
nhap_moi = 30
da_ban = 50
nhu_cau_du_kien = 80
# === KẾT THÚC DỮ LIỆU MẪU ===

# PHẦN SINH VIÊN VIẾT TIẾP (ĐIỀN VÀO CHỖ TRỐNG ...)
# Yêu cầu 1: Tính số lượng tồn kho cuối ngày (tồn đầu + nhập mới - đã bán)
ton_cuoi = ton_dau + ... - ...

# Yêu cầu 2: Tính số lượng cần nhập thêm (dùng hàm max() để không bị âm nếu đã đủ hàng)
can_nhap = max(0, ... - ...)

# Yêu cầu 3: Tạo biến kiểu bool (True/False) kiểm tra xem tồn cuối đã đủ nhu cầu chưa (>=)
du_hang = ... >= ...

# Yêu cầu 4: In kết quả theo đúng mẫu: Cần nhập thêm: 35
print("Cần nhập thêm:", ...)
```

> 💡 **Gợi ý phương pháp:** Sử dụng max(0, ...) để không sinh ra số lượng cần nhập âm.

---

## Bài 06. Cập nhật danh sách hàng hóa
- **Mã bài tập:** `p06` | **Nhóm chuyên môn:** `Tồn kho` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:**  
> Danh sách mặt hàng của một cửa hàng được lưu bằng list. Người quản lý muốn đổi tên một mặt hàng và trích những món đầu tiên để đưa lên trang chủ.

### Yêu cầu thực hiện:
1. Thay phần tử menu[vi_tri_thay] bằng mon_moi.
2. Lưu món đầu tiên vào mon_dau.
3. Lưu menu[:so_muc_chon] vào danh_sach_goi_y.
4. Tính so_mon = len(menu).
5. In danh sách gợi ý theo mẫu: Gợi ý: ['Cà phê', 'Trà đào'].

### Đầu ra mẫu cần đạt:
```text
Gợi ý: ['Cà phê', 'Trà đào']
```

### Tiêu chí chấm điểm (10 điểm):
- **Món đầu** (`mon_dau`): `1 điểm`
- **Danh sách đã cập nhật** (`menu`): `2 điểm`
- **Danh sách gợi ý** (`danh_sach_goi_y`): `2 điểm`
- **Số món** (`so_mon`): `2 điểm`
- **Đầu ra theo mẫu** (`__output__`): `3 điểm`

### Mã nguồn khởi đầu (Điền vào chỗ trống `...`):
```python
# DỮ LIỆU ĐẦU VÀO MẪU (ĐÃ CHO)
menu = ["Cà phê", "Trà xanh", "Bạc xỉu", "Nước ép"]
mon_moi = "Trà đào"
vi_tri_thay = 1
so_muc_chon = 2
# === KẾT THÚC DỮ LIỆU MẪU ===

# PHẦN SINH VIÊN VIẾT TIẾP
# Yêu cầu 1: Thay thế phần tử tại chỉ số vi_tri_thay trong menu bằng mon_moi


# Yêu cầu 2: Lưu phần tử đầu tiên của menu vào biến mon_dau


# Yêu cầu 3: Cắt lát lấy so_muc_chon món đầu tiên từ menu và lưu vào biến danh_sach_goi_y


# Yêu cầu 4: Đếm tổng số món trong menu và lưu vào biến so_mon


# Yêu cầu 5: In danh sách gợi ý theo đúng mẫu: Gợi ý: ['Cà phê', 'Trà đào']

```

> 💡 **Gợi ý phương pháp:** Chỉ số list bắt đầu từ 0; phép cắt [:k] không lấy phần tử thứ k.

---

## Bài 07. Đo chi phí chuyển đổi và ROAS
- **Mã bài tập:** `p07` | **Nhóm chuyên môn:** `Marketing` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:**  
> Một chiến dịch quảng cáo có tổng ngân sách, số đơn hàng thu về và doanh thu ghi nhận từ chiến dịch. Cần tính chỉ số đo hiệu quả ngân sách.

### Yêu cầu thực hiện:
1. Tính cpa = ngân sách / số đơn.
2. Tính roas = doanh thu từ quảng cáo / ngân sách.
3. Tính so_du_sau_quang_cao = doanh thu − ngân sách − phí nền tảng.
4. In ROAS làm tròn 2 chữ số theo mẫu: ROAS: 4.2.

### Đầu ra mẫu cần đạt:
```text
ROAS: 4.2
```

### Tiêu chí chấm điểm (10 điểm):
- **CPA** (`cpa`): `2 điểm`
- **ROAS** (`roas`): `3 điểm`
- **Số dư sau quảng cáo** (`so_du_sau_quang_cao`): `2 điểm`
- **Đầu ra theo mẫu** (`__output__`): `3 điểm`

### Mã nguồn khởi đầu (Điền vào chỗ trống `...`):
```python
# DỮ LIỆU ĐẦU VÀO MẪU (ĐÃ CHO)
ngan_sach = 2000000
so_don = 40
doanh_thu_qc = 8400000
phi_nen_tang = 400000
# === KẾT THÚC DỮ LIỆU MẪU ===

# PHẦN SINH VIÊN VIẾT TIẾP
# Yêu cầu 1: Tính chi phí cho mỗi đơn hàng (CPA = ngân sách / số đơn) lưu vào biến cpa


# Yêu cầu 2: Tính tỷ suất doanh thu trên chi phí quảng cáo (ROAS = doanh thu QC / ngân sách) lưu vào biến roas


# Yêu cầu 3: Tính số dư sau quảng cáo (doanh thu QC - ngân sách - phí nền tảng) lưu vào biến so_du_sau_quang_cao


# Yêu cầu 4: In chỉ số ROAS làm tròn 2 chữ số thập phân theo đúng mẫu: ROAS: 4.2

```

> 💡 **Gợi ý phương pháp:** ROAS là hệ số doanh thu trên chi quảng cáo, không phải tỷ suất lợi nhuận. Chi phí nền tảng chỉ dùng ở biến số dư.

---

## Bài 08. So sánh hai kênh quảng cáo
- **Mã bài tập:** `p08` | **Nhóm chuyên môn:** `Marketing` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:**  
> Bộ phận marketing lưu chi phí và đơn hàng từ hai kênh trong các list có cùng thứ tự. Hãy đánh giá kênh 1 theo chi phí mỗi đơn.

### Yêu cầu thực hiện:
1. Tính cpa_kenh1 và cpa_kenh2 từ hai list.
2. Tạo biến kenh_1_tot_hon bằng phép so sánh cpa_kenh1 < cpa_kenh2.
3. Tính chenh_lech là chênh lệch tuyệt đối của hai CPA.
4. In: Kênh 1 tốt hơn: False.

### Đầu ra mẫu cần đạt:
```text
Kênh 1 tốt hơn: False
```

### Tiêu chí chấm điểm (10 điểm):
- **CPA kênh 1** (`cpa_kenh1`): `2 điểm`
- **CPA kênh 2** (`cpa_kenh2`): `2 điểm`
- **So sánh bool** (`kenh_1_tot_hon`): `2 điểm`
- **Chênh lệch** (`chenh_lech`): `2 điểm`
- **Đầu ra theo mẫu** (`__output__`): `2 điểm`

### Mã nguồn khởi đầu (Điền vào chỗ trống `...`):
```python
# DỮ LIỆU ĐẦU VÀO MẪU (ĐÃ CHO)
ten_kenh = ["Mạng xã hội", "Tìm kiếm"]
chi_phi = [800000, 720000]
so_don = [32, 36]
# === KẾT THÚC DỮ LIỆU MẪU ===

# PHẦN SINH VIÊN VIẾT TIẾP
# Yêu cầu 1: Tính CPA của từng kênh từ các list chi_phi và so_don (lưu vào cpa_kenh1 và cpa_kenh2)


# Yêu cầu 2: Tạo biến kenh_1_tot_hon kiểu bool so sánh xem kênh 1 có CPA thấp hơn kênh 2 không (<)


# Yêu cầu 3: Tính chênh lệch chi phí tuyệt đối giữa 2 kênh bằng hàm abs() lưu vào biến chenh_lech


# Yêu cầu 4: In kết quả theo đúng mẫu: Kênh 1 tốt hơn: False

```

> 💡 **Gợi ý phương pháp:** Dùng các chỉ số [0] và [1]; abs() nhận giá trị tuyệt đối.

---

## Bài 09. Tính lương và kiểm tra quỹ lương
- **Mã bài tập:** `p09` | **Nhóm chuyên môn:** `Nhân sự` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:**  
> Cửa hàng có hai nhân viên. Lương tháng gồm lương cơ bản và khoản thưởng; phòng nhân sự cần đối chiếu tổng lương với ngân sách.

### Yêu cầu thực hiện:
1. Tính luong_a và luong_b.
2. Tính tong_luong.
3. Tính con_lai = ngân sách − tổng lương.
4. Tạo vuot_quy là bool xác định quỹ lương vượt ngân sách.
5. In: Vượt quỹ: False.

### Đầu ra mẫu cần đạt:
```text
Vượt quỹ: False
```

### Tiêu chí chấm điểm (10 điểm):
- **Lương nhân viên A** (`luong_a`): `1 điểm`
- **Lương nhân viên B** (`luong_b`): `1 điểm`
- **Tổng quỹ lương** (`tong_luong`): `2 điểm`
- **Ngân sách còn lại** (`con_lai`): `2 điểm`
- **Có vượt quỹ?** (`vuot_quy`): `2 điểm`
- **Đầu ra theo mẫu** (`__output__`): `2 điểm`

### Mã nguồn khởi đầu (Điền vào chỗ trống `...`):
```python
# DỮ LIỆU ĐẦU VÀO MẪU (ĐÃ CHO)
luong_co_ban_a = 12000000
thuong_a = 2000000
luong_co_ban_b = 10000000
thuong_b = 1500000
ngan_sach_quy = 27000000
# === KẾT THÚC DỮ LIỆU MẪU ===

# PHẦN SINH VIÊN VIẾT TIẾP
# Yêu cầu 1: Tính thu nhập thực nhận của từng nhân viên (lương cơ bản + thưởng) lưu vào luong_a và luong_b


# Yêu cầu 2: Tính tổng quỹ lương cần chi trả (luong_a + luong_b) lưu vào biến tong_luong


# Yêu cầu 3: Tính số tiền ngân sách còn lại (ngân sách quỹ - tổng lương) lưu vào biến con_lai


# Yêu cầu 4: Tạo biến vuot_quy kiểu bool kiểm tra xem tổng lương có vượt quá ngân sách quỹ không (>)


# Yêu cầu 5: In kết quả theo đúng mẫu: Vượt quỹ: False

```

> 💡 **Gợi ý phương pháp:** Dùng phép > so sánh tong_luong với ngan_sach_quy.

---

## Bài 10. Thống kê danh sách nhân viên
- **Mã bài tập:** `p10` | **Nhóm chuyên môn:** `Nhân sự` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:**  
> Bộ phận nhân sự lưu tên và mức lương từng người trong hai list song song. Hãy dùng các hàm dựng sẵn và slicing để thống kê.

### Yêu cầu thực hiện:
1. Tính so_nhan_vien = len(nhan_su).
2. Tính luong_binh_quan = sum(luong) / len(luong).
3. Tính luong_cao_nhat = max(luong).
4. Lấy hai_nhan_vien_dau = nhan_su[:2].
5. In: Số nhân viên: 4.

### Đầu ra mẫu cần đạt:
```text
Số nhân viên: 4
```

### Tiêu chí chấm điểm (10 điểm):
- **Số nhân viên** (`so_nhan_vien`): `2 điểm`
- **Lương bình quân** (`luong_binh_quan`): `2 điểm`
- **Lương cao nhất** (`luong_cao_nhat`): `2 điểm`
- **Hai nhân viên đầu** (`hai_nhan_vien_dau`): `2 điểm`
- **Đầu ra theo mẫu** (`__output__`): `2 điểm`

### Mã nguồn khởi đầu (Điền vào chỗ trống `...`):
```python
# DỮ LIỆU ĐẦU VÀO MẪU (ĐÃ CHO)
nhan_su = ["An", "Bình", "Chi", "Dung"]
luong = [12000000, 15000000, 18000000, 11000000]
# === KẾT THÚC DỮ LIỆU MẪU ===

# PHẦN SINH VIÊN VIẾT TIẾP
# Yêu cầu 1: Đếm số lượng nhân sự trong danh sách nhan_su lưu vào biến so_nhan_vien


# Yêu cầu 2: Tính lương bình quân của nhân viên (tổng lương / số lượng) lưu vào biến luong_binh_quan


# Yêu cầu 3: Tìm mức lương cao nhất trong danh sách luong lưu vào biến luong_cao_nhat


# Yêu cầu 4: Cắt lát lấy 2 nhân viên đầu tiên trong danh sách nhan_su lưu vào biến hai_nhan_vien_dau


# Yêu cầu 5: In kết quả theo đúng mẫu: Số nhân viên: 4

```

> 💡 **Gợi ý phương pháp:** Các list đã có sẵn; không cần for hay viết hàm.

---
