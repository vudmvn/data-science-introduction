# Ngân hàng Bài Tập & Đáp Án Chi Tiết — Bài 2: Lập trình Python Cơ bản trong Kinh doanh
## Học phần: Khoa học Dữ liệu Cơ bản trong Kinh tế & Kinh doanh (FDA.6.1.2.01.V) — NEU

> **Đề bài tự luyện không đáp án:** [`bai-2-bai-tap-tu-lam.md`](./bai-2-bai-tap-tu-lam.md)  
> **Tệp giao diện tự chấm trực tuyến:** [`bai-2-bai-tap-tu-lam.html`](./bai-2-bai-tap-tu-lam.html)  
> **Quy mô:** 10 bài tập lớn · **Thang điểm:** 100 điểm

---

## 📋 Bảng tra cứu kết quả mẫu chuẩn (Quick Answer Key)

| Bài | Tên bài tập | Nhóm | Điểm | Kết quả in ra mẫu (Output chuẩn) |
| :---: | :--- | :---: | :---: | :--- |
| **Bài 1** | Tính hóa đơn và giảm giá | Bán hàng | 10đ | `Thanh toán: 137700` |
| **Bài 2** | Hóa đơn có thuế và phí giao hàng | Bán hàng | 10đ | `Tổng hóa đơn: 128400` |
| **Bài 3** | Doanh thu, chi phí và lợi nhuận | Lợi nhuận | 10đ | `Lợi nhuận: 155000` |
| **Bài 4** | Tính biên lợi nhuận tháng | Lợi nhuận | 10đ | `Biên lợi nhuận (%): 20.0` |
| **Bài 5** | Kiểm kê và nhu cầu nhập hàng | Tồn kho | 10đ | `Cần nhập thêm: 35` |
| **Bài 6** | Cập nhật danh sách hàng hóa | Tồn kho | 10đ | `Gợi ý: ['Cà phê', 'Trà đào']` |
| **Bài 7** | Đo chi phí chuyển đổi và ROAS | Marketing | 10đ | `ROAS: 4.2` |
| **Bài 8** | So sánh hai kênh quảng cáo | Marketing | 10đ | `Kênh 1 tốt hơn: False` |
| **Bài 9** | Tính lương và kiểm tra quỹ lương | Nhân sự | 10đ | `Vượt quỹ: False` |
| **Bài 10** | Thống kê danh sách nhân viên | Nhân sự | 10đ | `Số nhân viên: 4` |

---

## 📝 Lời giải và hướng dẫn chi tiết từng bài

## Bài 01. Tính hóa đơn và giảm giá
- **Mã bài tập:** `p01` | **Nhóm chuyên môn:** `Bán hàng` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:** NeuTech Coffee bán cà phê sữa và trà đào. Quán giảm một tỷ lệ cố định cho hóa đơn; hãy tính đúng số tiền thanh toán.

### Yêu cầu bài toán:
1. Tính tổng trước giảm và lưu vào biến tong_goc.
2. Tính số tiền giảm vào muc_giam.
3. Tính tiền phải trả vào thanh_toan.
4. Dùng print() in đúng mẫu: Thanh toán: 137700 (số nguyên, không có chữ VNĐ).

### Lời giải mẫu hoàn chỉnh (Python):
```python
tong_goc = gia_sua * so_sua + gia_tra * so_tra
muc_giam = tong_goc * ty_le_giam
thanh_toan = tong_goc - muc_giam
print("Thanh toán:", int(thanh_toan))
```

> 💡 **Hướng dẫn giải chi tiết:** Có thể dùng int() khi in; tỷ lệ giảm là số thập phân như 0.1.

### Bảng tiêu chí chấm điểm tự động:
- `tong_goc` (Tổng tiền trước giảm): **2 điểm**
- `muc_giam` (Mức giảm): **2 điểm**
- `thanh_toan` (Tiền thanh toán): **3 điểm**
- `__output__` (Đầu ra theo mẫu): **3 điểm**

### Các bộ testcase kiểm thử tự động:
- **Testcase 1:** Đầu vào: `gia_sua = 25000 | so_sua = 3 | gia_tra = 39000 | so_tra = 2 | ty_le_giam = 0.1` → Kỳ vọng: `tong_goc: 153000, muc_giam: 15300.0, thanh_toan: 137700.0, __output__: Thanh toán: 137700`
- **Testcase 2:** Đầu vào: `gia_sua = 30000 | so_sua = 2 | gia_tra = 20000 | so_tra = 4 | ty_le_giam = 0.05` → Kỳ vọng: `tong_goc: 140000, muc_giam: 7000.0, thanh_toan: 133000.0, __output__: Thanh toán: 133000`
- **Testcase 3:** Đầu vào: `gia_sua = 45000 | so_sua = 1 | gia_tra = 25000 | so_tra = 5 | ty_le_giam = 0` → Kỳ vọng: `tong_goc: 170000, muc_giam: 0, thanh_toan: 170000, __output__: Thanh toán: 170000`

---

## Bài 02. Hóa đơn có thuế và phí giao hàng
- **Mã bài tập:** `p02` | **Nhóm chuyên môn:** `Bán hàng` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:** Một cửa hàng nhận đơn qua ứng dụng. Đơn giá và số lượng được hệ thống gửi về dưới dạng chuỗi; cần chuyển thành số trước khi tính.

### Yêu cầu bài toán:
1. Chuyển don_gia và so_luong thành số rồi tính tien_hang.
2. Tính tien_thue theo thue_suat trên tiền hàng.
3. Tính tong_hoa_don gồm tiền hàng, thuế và phí giao hàng.
4. In đúng mẫu: Tổng hóa đơn: 128400 (sử dụng round() hoặc int() với dữ liệu hiện tại).

### Lời giải mẫu hoàn chỉnh (Python):
```python
tien_hang = int(don_gia) * int(so_luong)
tien_thue = tien_hang * thue_suat
tong_hoa_don = tien_hang + tien_thue + phi_giao
print("Tổng hóa đơn:", round(tong_hoa_don))
```

> 💡 **Hướng dẫn giải chi tiết:** int("35000") = 35000; thuế chỉ tính trên tiền hàng, không tính trên phí giao.

### Bảng tiêu chí chấm điểm tự động:
- `tien_hang` (Tiền hàng): **2 điểm**
- `tien_thue` (Tiền thuế): **2 điểm**
- `tong_hoa_don` (Tổng hóa đơn): **3 điểm**
- `__output__` (Đầu ra theo mẫu): **3 điểm**

### Các bộ testcase kiểm thử tự động:
- **Testcase 1:** Đầu vào: `don_gia = "35000" | so_luong = "3" | phi_giao = 15000 | thue_suat = 0.08` → Kỳ vọng: `tien_hang: 105000, tien_thue: 8400.0, tong_hoa_don: 128400.0, __output__: Tổng hóa đơn: 128400`
- **Testcase 2:** Đầu vào: `don_gia = "45000" | so_luong = "2" | phi_giao = 20000 | thue_suat = 0.1` → Kỳ vọng: `tien_hang: 90000, tien_thue: 9000.0, tong_hoa_don: 119000.0, __output__: Tổng hóa đơn: 119000`
- **Testcase 3:** Đầu vào: `don_gia = "12500" | so_luong = "8" | phi_giao = 5000 | thue_suat = 0.05` → Kỳ vọng: `tien_hang: 100000, tien_thue: 5000.0, tong_hoa_don: 110000.0, __output__: Tổng hóa đơn: 110000`

---

## Bài 03. Doanh thu, chi phí và lợi nhuận
- **Mã bài tập:** `p03` | **Nhóm chuyên môn:** `Lợi nhuận` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:** Một quầy đồ uống bán một loại sản phẩm trong ngày. Biết doanh số, giá bán và chi phí biến đổi mỗi ly; cần tính lợi nhuận sau chi phí cố định.

### Yêu cầu bài toán:
1. Tính doanh_thu = số ly × giá bán.
2. Tính chi_phi gồm chi phí biến đổi và chi phí cố định.
3. Tính loi_nhuan = doanh thu − chi phí.
4. In đúng mẫu: Lợi nhuận: 155000.

### Lời giải mẫu hoàn chỉnh (Python):
```python
doanh_thu = so_ly * gia_ban
chi_phi = so_ly * chi_phi_moi_ly + chi_phi_co_dinh
loi_nhuan = doanh_thu - chi_phi
print("Lợi nhuận:", loi_nhuan)
```

> 💡 **Hướng dẫn giải chi tiết:** Chi phí biến đổi = số ly × chi phí nguyên liệu của mỗi ly.

### Bảng tiêu chí chấm điểm tự động:
- `doanh_thu` (Doanh thu): **2 điểm**
- `chi_phi` (Tổng chi phí): **2 điểm**
- `loi_nhuan` (Lợi nhuận): **3 điểm**
- `__output__` (Đầu ra theo mẫu): **3 điểm**

### Các bộ testcase kiểm thử tự động:
- **Testcase 1:** Đầu vào: `so_ly = 25 | gia_ban = 30000 | chi_phi_moi_ly = 15000 | chi_phi_co_dinh = 220000` → Kỳ vọng: `doanh_thu: 750000, chi_phi: 595000, loi_nhuan: 155000, __output__: Lợi nhuận: 155000`
- **Testcase 2:** Đầu vào: `so_ly = 40 | gia_ban = 25000 | chi_phi_moi_ly = 12500 | chi_phi_co_dinh = 310000` → Kỳ vọng: `doanh_thu: 1000000, chi_phi: 810000, loi_nhuan: 190000, __output__: Lợi nhuận: 190000`
- **Testcase 3:** Đầu vào: `so_ly = 10 | gia_ban = 20000 | chi_phi_moi_ly = 14000 | chi_phi_co_dinh = 150000` → Kỳ vọng: `doanh_thu: 200000, chi_phi: 290000, loi_nhuan: -90000, __output__: Lợi nhuận: -90000`

---

## Bài 04. Tính biên lợi nhuận tháng
- **Mã bài tập:** `p04` | **Nhóm chuyên môn:** `Lợi nhuận` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:** Một doanh nghiệp tổng hợp doanh thu tháng và bốn nhóm chi phí. Hãy đánh giá biên lợi nhuận bằng phép toán số học.

### Yêu cầu bài toán:
1. Tính tổng chi phí trong biến tong_chi.
2. Tính loi_nhuan.
3. Tính ty_suat phần trăm = lợi nhuận / doanh thu × 100.
4. In: Biên lợi nhuận (%): 20.0 (làm tròn hai chữ số thập phân bằng round()).

### Lời giải mẫu hoàn chỉnh (Python):
```python
tong_chi = nguyen_lieu + tien_luong + mat_bang + chi_phi_khac
loi_nhuan = doanh_thu_thang - tong_chi
ty_suat = loi_nhuan / doanh_thu_thang * 100
print("Biên lợi nhuận (%):", round(ty_suat, 2))
```

> 💡 **Hướng dẫn giải chi tiết:** Tỷ suất có thể âm khi lỗ. Dùng round(ty_suat, 2) khi in.

### Bảng tiêu chí chấm điểm tự động:
- `tong_chi` (Tổng chi phí): **2 điểm**
- `loi_nhuan` (Lợi nhuận): **2 điểm**
- `ty_suat` (Tỷ suất lợi nhuận): **3 điểm**
- `__output__` (Đầu ra theo mẫu): **3 điểm**

### Các bộ testcase kiểm thử tự động:
- **Testcase 1:** Đầu vào: `doanh_thu_thang = 200000000 | nguyen_lieu = 70000000 | tien_luong = 55000000 | mat_bang = 20000000 | chi_phi_khac = 15000000` → Kỳ vọng: `tong_chi: 160000000, loi_nhuan: 40000000, ty_suat: 20.0, __output__: Biên lợi nhuận (%): 20.0`
- **Testcase 2:** Đầu vào: `doanh_thu_thang = 120000000 | nguyen_lieu = 40000000 | tien_luong = 32000000 | mat_bang = 18000000 | chi_phi_khac = 10000000` → Kỳ vọng: `tong_chi: 100000000, loi_nhuan: 20000000, ty_suat: 16.666666666666664, __output__: Biên lợi nhuận (%): 16.67`
- **Testcase 3:** Đầu vào: `doanh_thu_thang = 90000000 | nguyen_lieu = 39000000 | tien_luong = 30000000 | mat_bang = 19000000 | chi_phi_khac = 9000000` → Kỳ vọng: `tong_chi: 97000000, loi_nhuan: -7000000, ty_suat: -7.777777777777778, __output__: Biên lợi nhuận (%): -7.78`

---

## Bài 05. Kiểm kê và nhu cầu nhập hàng
- **Mã bài tập:** `p05` | **Nhóm chuyên môn:** `Tồn kho` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:** Quản lý cửa hàng cần cập nhật số lượng tồn kho sau khi nhập và bán trong ngày. Cửa hàng muốn biết cần nhập thêm bao nhiêu đơn vị để đáp ứng nhu cầu dự kiến.

### Yêu cầu bài toán:
1. Tính ton_cuoi = tồn đầu + nhập mới − đã bán.
2. Tính can_nhap = max(0, nhu cầu dự kiến − tồn cuối).
3. Tạo biến du_hang (bool) cho biết tồn cuối đã đủ nhu cầu.
4. In: Cần nhập thêm: 35.

### Lời giải mẫu hoàn chỉnh (Python):
```python
ton_cuoi = ton_dau + nhap_moi - da_ban
can_nhap = max(0, nhu_cau_du_kien - ton_cuoi)
du_hang = ton_cuoi >= nhu_cau_du_kien
print("Cần nhập thêm:", can_nhap)
```

> 💡 **Hướng dẫn giải chi tiết:** Sử dụng max(0, ...) để không sinh ra số lượng cần nhập âm.

### Bảng tiêu chí chấm điểm tự động:
- `ton_cuoi` (Tồn cuối): **2 điểm**
- `can_nhap` (Nhu cầu nhập thêm): **3 điểm**
- `du_hang` (Đủ hàng (bool)): **2 điểm**
- `__output__` (Đầu ra theo mẫu): **3 điểm**

### Các bộ testcase kiểm thử tự động:
- **Testcase 1:** Đầu vào: `ton_dau = 65 | nhap_moi = 30 | da_ban = 50 | nhu_cau_du_kien = 80` → Kỳ vọng: `ton_cuoi: 45, can_nhap: 35, du_hang: False, __output__: Cần nhập thêm: 35`
- **Testcase 2:** Đầu vào: `ton_dau = 100 | nhap_moi = 30 | da_ban = 40 | nhu_cau_du_kien = 75` → Kỳ vọng: `ton_cuoi: 90, can_nhap: 0, du_hang: True, __output__: Cần nhập thêm: 0`
- **Testcase 3:** Đầu vào: `ton_dau = 20 | nhap_moi = 15 | da_ban = 28 | nhu_cau_du_kien = 30` → Kỳ vọng: `ton_cuoi: 7, can_nhap: 23, du_hang: False, __output__: Cần nhập thêm: 23`

---

## Bài 06. Cập nhật danh sách hàng hóa
- **Mã bài tập:** `p06` | **Nhóm chuyên môn:** `Tồn kho` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:** Danh sách mặt hàng của một cửa hàng được lưu bằng list. Người quản lý muốn đổi tên một mặt hàng và trích những món đầu tiên để đưa lên trang chủ.

### Yêu cầu bài toán:
1. Thay phần tử menu[vi_tri_thay] bằng mon_moi.
2. Lưu món đầu tiên vào mon_dau.
3. Lưu menu[:so_muc_chon] vào danh_sach_goi_y.
4. Tính so_mon = len(menu).
5. In danh sách gợi ý theo mẫu: Gợi ý: ['Cà phê', 'Trà đào'].

### Lời giải mẫu hoàn chỉnh (Python):
```python
menu[vi_tri_thay] = mon_moi
mon_dau = menu[0]
danh_sach_goi_y = menu[:so_muc_chon]
so_mon = len(menu)
print("Gợi ý:", danh_sach_goi_y)
```

> 💡 **Hướng dẫn giải chi tiết:** Chỉ số list bắt đầu từ 0; phép cắt [:k] không lấy phần tử thứ k.

### Bảng tiêu chí chấm điểm tự động:
- `mon_dau` (Món đầu): **1 điểm**
- `menu` (Danh sách đã cập nhật): **2 điểm**
- `danh_sach_goi_y` (Danh sách gợi ý): **2 điểm**
- `so_mon` (Số món): **2 điểm**
- `__output__` (Đầu ra theo mẫu): **3 điểm**

### Các bộ testcase kiểm thử tự động:
- **Testcase 1:** Đầu vào: `menu = ["Cà phê", "Trà xanh", "Bạc xỉu", "Nước ép"] | mon_moi = "Trà đào" | vi_tri_thay = 1 | so_muc_chon = 2` → Kỳ vọng: `mon_dau: Cà phê, menu: ['Cà phê', 'Trà đào', 'Bạc xỉu', 'Nước ép'], danh_sach_goi_y: ['Cà phê', 'Trà đào'], so_mon: 4, __output__: Gợi ý: ['Cà phê', 'Trà đào']`
- **Testcase 2:** Đầu vào: `menu = ["Trà", "Cacao", "Sữa chua", "Chanh"] | mon_moi = "Cacao nóng" | vi_tri_thay = 1 | so_muc_chon = 3` → Kỳ vọng: `mon_dau: Trà, menu: ['Trà', 'Cacao nóng', 'Sữa chua', 'Chanh'], danh_sach_goi_y: ['Trà', 'Cacao nóng', 'Sữa chua'], so_mon: 4, __output__: Gợi ý: ['Trà', 'Cacao nóng', 'Sữa chua']`
- **Testcase 3:** Đầu vào: `menu = ["Đen đá", "Sữa đá", "Trà", "Kem", "Bánh"] | mon_moi = "Bánh mì" | vi_tri_thay = 4 | so_muc_chon = 2` → Kỳ vọng: `mon_dau: Đen đá, menu: ['Đen đá', 'Sữa đá', 'Trà', 'Kem', 'Bánh mì'], danh_sach_goi_y: ['Đen đá', 'Sữa đá'], so_mon: 5, __output__: Gợi ý: ['Đen đá', 'Sữa đá']`

---

## Bài 07. Đo chi phí chuyển đổi và ROAS
- **Mã bài tập:** `p07` | **Nhóm chuyên môn:** `Marketing` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:** Một chiến dịch quảng cáo có tổng ngân sách, số đơn hàng thu về và doanh thu ghi nhận từ chiến dịch. Cần tính chỉ số đo hiệu quả ngân sách.

### Yêu cầu bài toán:
1. Tính cpa = ngân sách / số đơn.
2. Tính roas = doanh thu từ quảng cáo / ngân sách.
3. Tính so_du_sau_quang_cao = doanh thu − ngân sách − phí nền tảng.
4. In ROAS làm tròn 2 chữ số theo mẫu: ROAS: 4.2.

### Lời giải mẫu hoàn chỉnh (Python):
```python
cpa = ngan_sach / so_don
roas = doanh_thu_qc / ngan_sach
so_du_sau_quang_cao = doanh_thu_qc - ngan_sach - phi_nen_tang
print("ROAS:", round(roas, 2))
```

> 💡 **Hướng dẫn giải chi tiết:** ROAS là hệ số doanh thu trên chi quảng cáo, không phải tỷ suất lợi nhuận. Chi phí nền tảng chỉ dùng ở biến số dư.

### Bảng tiêu chí chấm điểm tự động:
- `cpa` (CPA): **2 điểm**
- `roas` (ROAS): **3 điểm**
- `so_du_sau_quang_cao` (Số dư sau quảng cáo): **2 điểm**
- `__output__` (Đầu ra theo mẫu): **3 điểm**

### Các bộ testcase kiểm thử tự động:
- **Testcase 1:** Đầu vào: `ngan_sach = 2000000 | so_don = 40 | doanh_thu_qc = 8400000 | phi_nen_tang = 400000` → Kỳ vọng: `cpa: 50000.0, roas: 4.2, so_du_sau_quang_cao: 6000000, __output__: ROAS: 4.2`
- **Testcase 2:** Đầu vào: `ngan_sach = 1600000 | so_don = 25 | doanh_thu_qc = 4200000 | phi_nen_tang = 250000` → Kỳ vọng: `cpa: 64000.0, roas: 2.625, so_du_sau_quang_cao: 2350000, __output__: ROAS: 2.62`
- **Testcase 3:** Đầu vào: `ngan_sach = 3000000 | so_don = 60 | doanh_thu_qc = 11250000 | phi_nen_tang = 750000` → Kỳ vọng: `cpa: 50000.0, roas: 3.75, so_du_sau_quang_cao: 7500000, __output__: ROAS: 3.75`

---

## Bài 08. So sánh hai kênh quảng cáo
- **Mã bài tập:** `p08` | **Nhóm chuyên môn:** `Marketing` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:** Bộ phận marketing lưu chi phí và đơn hàng từ hai kênh trong các list có cùng thứ tự. Hãy đánh giá kênh 1 theo chi phí mỗi đơn.

### Yêu cầu bài toán:
1. Tính cpa_kenh1 và cpa_kenh2 từ hai list.
2. Tạo biến kenh_1_tot_hon bằng phép so sánh cpa_kenh1 < cpa_kenh2.
3. Tính chenh_lech là chênh lệch tuyệt đối của hai CPA.
4. In: Kênh 1 tốt hơn: False.

### Lời giải mẫu hoàn chỉnh (Python):
```python
cpa_kenh1 = chi_phi[0] / so_don[0]
cpa_kenh2 = chi_phi[1] / so_don[1]
kenh_1_tot_hon = cpa_kenh1 < cpa_kenh2
chenh_lech = abs(cpa_kenh1 - cpa_kenh2)
print("Kênh 1 tốt hơn:", kenh_1_tot_hon)
```

> 💡 **Hướng dẫn giải chi tiết:** Dùng các chỉ số [0] và [1]; abs() nhận giá trị tuyệt đối.

### Bảng tiêu chí chấm điểm tự động:
- `cpa_kenh1` (CPA kênh 1): **2 điểm**
- `cpa_kenh2` (CPA kênh 2): **2 điểm**
- `kenh_1_tot_hon` (So sánh bool): **2 điểm**
- `chenh_lech` (Chênh lệch): **2 điểm**
- `__output__` (Đầu ra theo mẫu): **2 điểm**

### Các bộ testcase kiểm thử tự động:
- **Testcase 1:** Đầu vào: `ten_kenh = ["Mạng xã hội", "Tìm kiếm"] | chi_phi = [800000, 720000] | so_don = [32, 36]` → Kỳ vọng: `cpa_kenh1: 25000.0, cpa_kenh2: 20000.0, kenh_1_tot_hon: False, chenh_lech: 5000.0, __output__: Kênh 1 tốt hơn: False`
- **Testcase 2:** Đầu vào: `ten_kenh = ["Kênh A", "Kênh B"] | chi_phi = [300000, 360000] | so_don = [30, 18]` → Kỳ vọng: `cpa_kenh1: 10000.0, cpa_kenh2: 20000.0, kenh_1_tot_hon: True, chenh_lech: 10000.0, __output__: Kênh 1 tốt hơn: True`
- **Testcase 3:** Đầu vào: `ten_kenh = ["Kênh X", "Kênh Y"] | chi_phi = [1000000, 750000] | so_don = [50, 50]` → Kỳ vọng: `cpa_kenh1: 20000.0, cpa_kenh2: 15000.0, kenh_1_tot_hon: False, chenh_lech: 5000.0, __output__: Kênh 1 tốt hơn: False`

---

## Bài 09. Tính lương và kiểm tra quỹ lương
- **Mã bài tập:** `p09` | **Nhóm chuyên môn:** `Nhân sự` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:** Cửa hàng có hai nhân viên. Lương tháng gồm lương cơ bản và khoản thưởng; phòng nhân sự cần đối chiếu tổng lương với ngân sách.

### Yêu cầu bài toán:
1. Tính luong_a và luong_b.
2. Tính tong_luong.
3. Tính con_lai = ngân sách − tổng lương.
4. Tạo vuot_quy là bool xác định quỹ lương vượt ngân sách.
5. In: Vượt quỹ: False.

### Lời giải mẫu hoàn chỉnh (Python):
```python
luong_a = luong_co_ban_a + thuong_a
luong_b = luong_co_ban_b + thuong_b
tong_luong = luong_a + luong_b
con_lai = ngan_sach_quy - tong_luong
vuot_quy = tong_luong > ngan_sach_quy
print("Vượt quỹ:", vuot_quy)
```

> 💡 **Hướng dẫn giải chi tiết:** Dùng phép > so sánh tong_luong với ngan_sach_quy.

### Bảng tiêu chí chấm điểm tự động:
- `luong_a` (Lương nhân viên A): **1 điểm**
- `luong_b` (Lương nhân viên B): **1 điểm**
- `tong_luong` (Tổng quỹ lương): **2 điểm**
- `con_lai` (Ngân sách còn lại): **2 điểm**
- `vuot_quy` (Có vượt quỹ?): **2 điểm**
- `__output__` (Đầu ra theo mẫu): **2 điểm**

### Các bộ testcase kiểm thử tự động:
- **Testcase 1:** Đầu vào: `luong_co_ban_a = 12000000 | thuong_a = 2000000 | luong_co_ban_b = 10000000 | thuong_b = 1500000 | ngan_sach_quy = 27000000` → Kỳ vọng: `luong_a: 14000000, luong_b: 11500000, tong_luong: 25500000, con_lai: 1500000, vuot_quy: False, __output__: Vượt quỹ: False`
- **Testcase 2:** Đầu vào: `luong_co_ban_a = 17000000 | thuong_a = 3000000 | luong_co_ban_b = 14000000 | thuong_b = 2000000 | ngan_sach_quy = 34000000` → Kỳ vọng: `luong_a: 20000000, luong_b: 16000000, tong_luong: 36000000, con_lai: -2000000, vuot_quy: True, __output__: Vượt quỹ: True`
- **Testcase 3:** Đầu vào: `luong_co_ban_a = 9000000 | thuong_a = 500000 | luong_co_ban_b = 11500000 | thuong_b = 300000 | ngan_sach_quy = 20000000` → Kỳ vọng: `luong_a: 9500000, luong_b: 11800000, tong_luong: 21300000, con_lai: -1300000, vuot_quy: True, __output__: Vượt quỹ: True`

---

## Bài 10. Thống kê danh sách nhân viên
- **Mã bài tập:** `p10` | **Nhóm chuyên môn:** `Nhân sự` | **Thang điểm:** `10 điểm`  

> **Bối cảnh nghiệp vụ:** Bộ phận nhân sự lưu tên và mức lương từng người trong hai list song song. Hãy dùng các hàm dựng sẵn và slicing để thống kê.

### Yêu cầu bài toán:
1. Tính so_nhan_vien = len(nhan_su).
2. Tính luong_binh_quan = sum(luong) / len(luong).
3. Tính luong_cao_nhat = max(luong).
4. Lấy hai_nhan_vien_dau = nhan_su[:2].
5. In: Số nhân viên: 4.

### Lời giải mẫu hoàn chỉnh (Python):
```python
so_nhan_vien = len(nhan_su)
luong_binh_quan = sum(luong) / len(luong)
luong_cao_nhat = max(luong)
hai_nhan_vien_dau = nhan_su[:2]
print("Số nhân viên:", so_nhan_vien)
```

> 💡 **Hướng dẫn giải chi tiết:** Các list đã có sẵn; không cần for hay viết hàm.

### Bảng tiêu chí chấm điểm tự động:
- `so_nhan_vien` (Số nhân viên): **2 điểm**
- `luong_binh_quan` (Lương bình quân): **2 điểm**
- `luong_cao_nhat` (Lương cao nhất): **2 điểm**
- `hai_nhan_vien_dau` (Hai nhân viên đầu): **2 điểm**
- `__output__` (Đầu ra theo mẫu): **2 điểm**

### Các bộ testcase kiểm thử tự động:
- **Testcase 1:** Đầu vào: `nhan_su = ["An", "Bình", "Chi", "Dung"] | luong = [12000000, 15000000, 18000000, 11000000]` → Kỳ vọng: `so_nhan_vien: 4, luong_binh_quan: 14000000.0, luong_cao_nhat: 18000000, hai_nhan_vien_dau: ['An', 'Bình'], __output__: Số nhân viên: 4`
- **Testcase 2:** Đầu vào: `nhan_su = ["Hà", "Nam", "Mai"] | luong = [9000000, 10000000, 14000000]` → Kỳ vọng: `so_nhan_vien: 3, luong_binh_quan: 11000000.0, luong_cao_nhat: 14000000, hai_nhan_vien_dau: ['Hà', 'Nam'], __output__: Số nhân viên: 3`
- **Testcase 3:** Đầu vào: `nhan_su = ["Tuấn", "Minh", "Lan", "Hải", "Nga"] | luong = [13000000, 17000000, 14000000, 20000000, 16000000]` → Kỳ vọng: `so_nhan_vien: 5, luong_binh_quan: 16000000.0, luong_cao_nhat: 20000000, hai_nhan_vien_dau: ['Tuấn', 'Minh'], __output__: Số nhân viên: 5`

---
