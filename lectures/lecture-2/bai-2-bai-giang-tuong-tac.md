# Giáo Trình Bài Giảng Tương Tác — Bài 2: Giới thiệu ngôn ngữ lập trình Python
## Học phần: Khoa học Dữ liệu Cơ bản trong Kinh tế & Kinh doanh (FDA.6.1.2.01.V) — NEU

> **Giao diện bài giảng tương tác trực tuyến:** [`bai-2-bai-giang-tuong-tac.html`](./bai-2-bai-giang-tuong-tac.html)  
> **Tài liệu học tập nguồn:** `Bài 2_Giới thiệu ngôn ngữ lập trình Python_B1.pdf` (32 trang)  
> **Bộ đề trắc nghiệm tự chấm:** [`bai-2-quiz-tu-cham.md`](./bai-2-quiz-tu-cham.md) · [`bai-2-quiz-dap-an.md`](./bai-2-quiz-dap-an.md)  
> **Bộ 10 bài tập tự làm thực hành:** [`bai-2-bai-tap-tu-lam.md`](./bai-2-bai-tap-tu-lam.md) · [`bai-2-bai-tap-dap-an.md`](./bai-2-bai-tap-dap-an.md)  
> **Bối cảnh kinh doanh xuyên suốt:** Chuỗi cửa hàng cà phê giả định **NeuTech Coffee**

---

## 📌 Tổng quan lộ trình học tập tuần tự (11 mục học)
Mỗi mục học tương ứng với một khối kiến thức trọng tâm từ slide bài giảng. Người học phải vượt qua câu hỏi chốt chặn (Checkpoint) của từng mục để mở khóa bài tiếp theo.

| Mục | Tiêu đề chuyên đề | Trang PDF | Khái niệm cốt lõi | Số khối code |
| :---: | :--- | :---: | :--- | :---: |
| **01** | **Bắt đầu từ quán cà phê** | tr. 1–3 | Bài toán kinh doanh → Biến, kiểu dữ liệu, tính toán doanh thu | 1 khối |
| **02** | **Python và Google Colab** | tr. 4–7 | Thông dịch, kiểu động, Code cell vs. Text cell, chạy Colab | 2 khối |
| **03** | **Biến và phép gán** | tr. 9–10 | Tên biến, gán `=`, so sánh `==`, quy tắc đặt tên, biến trung gian | 5 khối |
| **04** | **Các kiểu dữ liệu cơ bản** | tr. 11–12 | `int`, `float`, `bool`, `str`, hàm `type()` | 2 khối |
| **05** | **Toán tử số học** | tr. 13–14 | `+`, `-`, `*`, chia thực `/`, chia nguyên `//`, dư `%`, lũy thừa `**` | 4 khối |
| **06** | **Chuỗi, bool và so sánh** | tr. 15–17 | Chuỗi `str`, nối chuỗi `+`, toán tử so sánh, logic `and`, `or`, `not` | 4 khối |
| **07** | **Chuyển đổi kiểu dữ liệu** | tr. 18–20 | Ép kiểu `int()`, `float()`, `str()`, lỗi `ValueError` thường gặp | 3 khối |
| **08** | **List và tuple** | tr. 21–22, 26 | Dãy có thứ tự, tính thay đổi được (mutable) vs. bất biến (immutable) | 4 khối |
| **09** | **Indexing** | tr. 23 | Chỉ số dương (từ 0), chỉ số âm (từ -1), lỗi `IndexError` | 3 khối |
| **10** | **Slicing, set và tính bất biến** | tr. 24–26 | Cú pháp cắt lát `a[start:stop:step]`, cấu trúc `set` loại trùng | 4 khối |
| **11** | **Bài tập mẫu có lời giải** | tr. 19–20, 27–28 | Tổng hợp: đơn trà đào, quản lý thực đơn, tính chiết khấu và hóa đơn | 5 khối |
| | **TỔNG CỘNG** | **32 trang** | **Lộ trình hoàn chỉnh nền tảng lập trình Python cơ bản** | **37 khối (31 ví dụ + 6 thực hành)** |

---

## MỤC 01/11: Bắt đầu từ quán cà phê
> 📖 **Tham chiếu bài giảng:** PDF tr. 1–3 · **Chủ đề chính:** *Vì sao học Python?*

Buổi 2 sử dụng bối cảnh **NeuTech Coffee**: một quán cần lưu tên món, tính hóa đơn, quản lý thực đơn và xét điều kiện ưu đãi. Mỗi nhiệm vụ sẽ trở thành một bài toán lập trình nhỏ.

### 💡 Các khái niệm quan trọng:
- **Lưu thông tin:** Tên món, giá, số lượng → biến và kiểu dữ liệu.
- **Tính tiền:** Các phép cộng, nhân, chia và điều kiện logic.
- **Quản lý thực đơn:** Dùng list, tuple, set; truy cập theo chỉ số hoặc cắt lát.

> 📌 **Ghi chú trọng tâm:** Mục tiêu sau bài: đọc và dự đoán được chương trình Python cơ bản, giải thích kiểu dữ liệu và viết các lệnh ngắn về hoạt động kinh doanh.

### Từ bài toán kinh doanh đến câu lệnh Python
Một bài toán thường đi qua bốn bước: **(1)** xác định đầu vào, **(2)** diễn tả phép xử lý, **(3)** xác định kết quả cần hiển thị và **(4)** kiểm tra kết quả có hợp lý không. Chẳng hạn, để tính doanh thu bán cà phê, đầu vào là *số ly* và *giá mỗi ly*, phép xử lý là nhân, đầu ra là tiền thu được.

- **1. Đầu vào:** Giá 25.000 đồng/ly; số lượng 4 ly.
- **2. Xử lý:** Doanh thu = đơn giá × số lượng.
- **3. Đầu ra & kiểm tra:** 100.000 đồng; cần kiểm tra đơn giá và số lượng không âm.

### Ví dụ đầu tiên: cùng một bài toán, nhiều tình huống
Thay hai giá trị đầu vào rồi nhấn **Run** để kiểm tra kết quả. Khác với một máy tính bỏ túi chỉ có công thức cố định, khi lập trình ta có thể thay đổi quy trình tính toán và trình bày kết quả.

> ⚠️ **Lưu ý & Gợi ý:** **Tư duy quan trọng:** đừng bắt đầu bằng việc học thuộc cú pháp. Hãy xác định dữ liệu, quy tắc tính và đầu ra; Python là công cụ để diễn tả chính xác các bước đó.

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 01
```python
gia_moi_ly = 25000
so_ly = 4
doanh_thu = gia_moi_ly * so_ly
print("Doanh thu:", doanh_thu, "đồng")
```
**Kết quả in ra (Output):**
```text
Doanh thu: 100000 đồng
```

> ⚠️ **Lời khuyên thực hành:** **Tư duy quan trọng:** đừng bắt đầu bằng việc học thuộc cú pháp. Hãy xác định dữ liệu, quy tắc tính và đầu ra; Python là công cụ để diễn tả chính xác các bước đó.

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Quán muốn đổi món thứ hai trên thực đơn khi cần. Khái niệm nào sẽ giúp thực hiện việc này?

- [ ] **A.** Chỉ có thể dùng số nguyên
- [ ] **B.** Dùng danh sách list có thể chỉnh sửa
- [ ] **C.** Chỉ có thể dùng tên tệp

---

## MỤC 02/11: Python và Google Colab
> 📖 **Tham chiếu bài giảng:** PDF tr. 4–7 · **Chủ đề chính:** *Ngôn ngữ Python, cách chạy notebook*

**Python** là ngôn ngữ lập trình kiểu động, ra đời năm 1991 do Guido van Rossum phát triển. Python phổ biến trong khoa học dữ liệu và AI nhờ các thư viện như NumPy, pandas, matplotlib. Tệp mã có phần mở rộng `.py`.

### 💡 Các khái niệm quan trọng:
- **Kiểu động:** Biến không cần khai báo kiểu trước khi gán giá trị.
- **Code cell:** Ô chạy Python; dùng `Shift` + `Enter`.
- **Text cell:** Ô ghi chú Markdown, không chạy như lệnh Python.

> 📌 **Ghi chú trọng tâm:** Trong Google Colab, truy cập colab.research.google.com → New notebook → tạo Code cell → chạy Shift + Enter. Các ví dụ trong trang có nút Run: trình chạy offline xử lý một tập con các lệnh Python nhập môn. Để chạy Python đầy đủ và các thư viện chuyên ngành, sử dụng Colab.

### Thông dịch, kiểu động và mục đích của Python
Python là ngôn ngữ lập trình bậc cao, thường được thực thi bằng một **trình thông dịch**. Cách diễn đạt “chạy từng dòng” hữu ích khi mới học, nhưng trên thực tế Python còn phân tích cú pháp và tạo bytecode trước khi thực thi. **Kiểu động** có nghĩa là ta gán giá trị cho tên mà không khai báo kiểu của tên từ đầu; đối tượng được gán vẫn có một kiểu xác định.

Python dùng cho tự động hóa công việc, phân tích số liệu, xây dựng ứng dụng và khoa học dữ liệu. Trong những bài sau, sinh viên sẽ gặp NumPy (tính toán số), pandas (bảng dữ liệu) và matplotlib (biểu đồ).

### File .py và notebook khác nhau thế nào?
| Tiêu chí | Python .py | Google Colab notebook |
| :--- | :--- | :--- |
| Cách tổ chức | Các câu lệnh trong file văn bản | Các ô Code và Text đan xen |
| Phù hợp | Chương trình có cấu trúc, tái sử dụng | Thử nghiệm, học tập, phân tích khám phá |
| Trạng thái biến | Chạy từ đầu theo luồng chương trình | Biến có thể giữ trong phiên chạy; chạy ô sai thứ tự gây nhầm lẫn |
| Lưu bài | Tệp .py trên thiết bị hoặc kho mã | Tệp .ipynb, thường trên Google Drive |

### Code cell và Text cell
Trong Colab: Code cell có thể `print()`, gán biến, tính toán và tạo biểu đồ; Text cell là Markdown dùng để viết tiêu đề, công thức và lời giải thích. Nhấn `Shift` + `Enter` để chạy ô và chuyển tới ô tiếp theo. Nếu báo lỗi `NameError` vì biến chưa tồn tại, cần chạy ô khai báo biến trước.

> ⚠️ **Lưu ý & Gợi ý:** Các nút **Run** trong file này thực thi **tập con Python nhập môn** ngay trên trình duyệt, không đòi hỏi Internet. Để chạy thư viện, vòng lặp phức tạp hoặc Python đầy đủ, hãy dùng [Google Colab](https://colab.research.google.com). Đừng dùng `eval()` hoặc `exec()` với dữ liệu không tin cậy.

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 02
```python
print("Hello World!")
```
**Kết quả in ra (Output):**
```text
Hello World!
```

#### ☕ PYTHON · Ví dụ 03
```python
print("Xin chào NeuTech Coffee!")
print("Python có thể tính:", 25000 * 3)
```
**Kết quả in ra (Output):**
```text
Xin chào NeuTech Coffee!
Python có thể tính: 75000
```

> ⚠️ **Lời khuyên thực hành:** Các nút **Run** trong file này thực thi **tập con Python nhập môn** ngay trên trình duyệt, không đòi hỏi Internet. Để chạy thư viện, vòng lặp phức tạp hoặc Python đầy đủ, hãy dùng [Google Colab](https://colab.research.google.com). Đừng dùng `eval()` hoặc `exec()` với dữ liệu không tin cậy.

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Muốn thực thi một đoạn print("Hello!") trên Colab, bạn dùng ô nào?

- [ ] **A.** Text cell
- [ ] **B.** Code cell
- [ ] **C.** Tiêu đề notebook

---

## MỤC 03/11: Biến và phép gán
> 📖 **Tham chiếu bài giảng:** PDF tr. 9–10 · **Chủ đề chính:** *Tên biến, giá trị, quy tắc đặt tên*

Một biến là tên tham chiếu đến giá trị. Hình dung biến là nhãn dán trên hộp. Dấu `=` dùng để **gán**, không phải kiểm tra hai giá trị bằng nhau.

### 💡 Các khái niệm quan trọng:
- **Tên hợp lệ:** `so_ly`, `gia_1`, `_tong`.
- **Tên không hợp lệ:** `2so_ly` (bắt đầu bằng số), `gia-ca-phe` (dấu trừ), `while` (từ khóa).

### Phân biệt `=` và `==`
`=` là **gán** (đặt tên tham chiếu tới một giá trị). `==` là **so sánh**, trả về `True` hoặc `False`. Sau khi gán giá trị mới cho cùng tên, biểu thức tiếp theo sử dụng giá trị mới.

### Quy tắc đặt tên và lỗi thường gặp
Python **phân biệt chữ hoa và chữ thường**: `Gia` và `gia` là hai tên khác nhau. Nên dùng `snake_case` như `gia_ca_phe` và tránh dùng tên trùng hàm có sẵn như `list`, `str`, `sum`.

| Ví dụ | Hợp lệ? | Giải thích |
| :--- | :--- | :--- |
| `so_ly` | Đúng | Chữ và dấu gạch dưới, tên có nghĩa |
| `gia2` | Đúng | Chữ số được phép xuất hiện sau ký tự đầu |
| `2gia` | Sai | Không bắt đầu bằng chữ số |
| `gia-ca-phe` | Sai | Dấu `-` được hiểu là phép trừ |
| `while` | Sai | Là từ khóa của Python |

### Từ biến đơn đến biến trung gian
Sử dụng các biến trung gian như `tien_hang` giúp quy trình tính toán rõ ràng, mạch lạc và dễ kiểm soát lỗi nghiệp vụ hơn (chi tiết minh họa tại **Ví dụ 07**).

> ⚠️ **Lưu ý & Gợi ý:** **Bài tập nhỏ:** đổi phí vận chuyển từ 10.000 xuống 5.000 đồng. Dự đoán kết quả trước khi Run. Nếu bạn thấy `NameError`, hãy kiểm tra chính tả và việc gán biến trước khi sử dụng.

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 04
```python
ten_quan = "NeuTech Coffee"
so_ban = 12
gia_ca_phe = 20000
print("Quán có", so_ban, "bàn")
# Quán có 12 bàn
```
**Kết quả in ra (Output):**
```text
Quán có 12 bàn
```

#### ☕ PYTHON · Ví dụ 05
```python
gia_ca_phe = 20000
gia_ca_phe = 22000
print(gia_ca_phe)
# 22000
```
**Kết quả in ra (Output):**
```text
22000
```

#### 🎯 THỰC HÀNH 01 · Đổi giá trị biến & tính tiền 3 ly
**Mã nguồn khởi đầu (Điền vào chỗ trống `...`):**
```python
gia_ca_phe = 20000
# Hãy thay dấu ... đầu tiên bằng giá mới 22000 và dấu ... thứ hai bằng số lượng 3:
gia_ca_phe = ...
thanh_tien = gia_ca_phe * ...
print("Tổng tiền 3 ly:", thanh_tien)
# Kết quả mong đợi: Tổng tiền 3 ly: 66000
```
**Lời giải hoàn chỉnh:**
```python
gia_ca_phe = 20000
gia_ca_phe = 22000
thanh_tien = gia_ca_phe * 3
print("Tổng tiền 3 ly:", thanh_tien)
```
**Kết quả chạy trên Console:**
```text
Tổng tiền 3 ly: 66000
```

#### ☕ PYTHON · Ví dụ 06
```python
gia = 20000
print(gia == 20000)
gia = 22000
print(gia)
print(gia == 20000)
```
**Kết quả in ra (Output):**
```text
True
22000
False
```

#### ☕ PYTHON · Ví dụ 07
```python
gia_ly = 30000
so_ly = 3
chi_phi_van_chuyen = 10000
tien_hang = gia_ly * so_ly
tong_thanh_toan = tien_hang + chi_phi_van_chuyen
print("Tiền hàng:", tien_hang)
print("Phải trả:", tong_thanh_toan)
```
**Kết quả in ra (Output):**
```text
Tiền hàng: 90000
Phải trả: 100000
```

> ⚠️ **Lời khuyên thực hành:** **Bài tập nhỏ:** đổi phí vận chuyển từ 10.000 xuống 5.000 đồng. Dự đoán kết quả trước khi Run. Nếu bạn thấy `NameError`, hãy kiểm tra chính tả và việc gán biến trước khi sử dụng.

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Tên nào hợp lệ để lưu số ly khách gọi?

- [ ] **A.** 3ly
- [ ] **B.** so_ly
- [ ] **C.** so-ly

---

## MỤC 04/11: Các kiểu dữ liệu cơ bản
> 📖 **Tham chiếu bài giảng:** PDF tr. 11–12 · **Chủ đề chính:** *int, float, bool, str và kiểu cấu trúc*

Giá trị trong Python có kiểu dữ liệu. `type()` có thể giúp xem kiểu của một đối tượng.

### 💡 Các khái niệm quan trọng:
- **int · số nguyên:** Ví dụ: `4`, `25000`.
- **float · số thực:** Ví dụ: `3.14159`, `2.0`.
- **str · chuỗi:** Ví dụ: `"Bạc xỉu"`.
- **bool · logic:** Ví dụ: `True`, `False`.

> 📌 **Ghi chú trọng tâm:** Khác biệt rất quan trọng: `12` là số nguyên nhưng `"12"` là chuỗi. Biểu thức cộng số và nối chuỗi cho kết quả khác nhau.

### Mỗi giá trị có một kiểu
Kiểu dữ liệu xác định những phép toán hợp lệ. `25` có kiểu `int`, trong khi `"25"` có kiểu `str`: một giá trị dùng để tính toán, giá trị còn lại là dãy ký tự. Hàm `type()` trả về kiểu đối tượng.

| Kiểu | Ví dụ | Khi nào dùng? |
| :--- | :--- | :--- |
| `int` | `5`, `-2` | Số món, số đơn, đơn giá nguyên |
| `float` | `12.5`, `0.1` | Phần trăm, tỷ lệ, giá trị thực |
| `bool` | `True`, `False` | Hết hàng? Có thẻ thành viên? |
| `str` | `"Cà phê"` | Tên món, mã đơn, ghi chú |
| `list` | `["Đen", "Sữa"]` | Dãy có thứ tự, có thể sửa |
| `tuple` | `(2026, 10, 23)` | Bộ giá trị có thứ tự, bất biến |
| `set` | `{"Đen", "Sữa"}` | Nhóm phần tử duy nhất |
| `dict` | `{"Đen": 20000}` | Tra cứu theo khóa; sẽ học sâu ở bài tiếp theo |

> 📌 **Chú ý với tiền:** Giá trị `float` có thể có sai số biểu diễn trong một số phép tính thập phân. Trong bài nhập môn ta dùng `int` biểu thị đơn vị VNĐ khi có thể; trong ứng dụng tài chính chính thức thường cân nhắc số nguyên theo đơn vị nhỏ nhất hoặc kiểu số thập phân chính xác.

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 08
```python
so_ly = 4
don_gia = 25000
print(type(so_ly))   # <class 'int'>
print(so_ly*don_gia) # 100000
```
**Kết quả in ra (Output):**
```text
<class 'int'>
100000
```

#### ☕ PYTHON · Ví dụ 09
```python
a = 12
b = "12"
c = 12.0
d = True
print(type(a))
print(type(b))
print(type(c))
print(type(d))
print(a + 3)
print(b + "3")
```
**Kết quả in ra (Output):**
```text
<class 'int'>
<class 'str'>
<class 'float'>
<class 'bool'>
15
123
```

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Biểu thức type("25") trả về kiểu dữ liệu nào?

- [ ] **A.** int
- [ ] **B.** str
- [ ] **C.** float

---

## MỤC 05/11: Toán tử số học
> 📖 **Tham chiếu bài giảng:** PDF tr. 13–14 · **Chủ đề chính:** *Cộng, trừ, nhân, chia, dư và lũy thừa*

Python sử dụng các toán tử `+ - * / // % **`. Phép chia `/` trả về số thực, `//` là phép chia làm tròn xuống, `%` lấy phần dư.

### 💡 Các khái niệm quan trọng:
- **Ví dụ hóa đơn:** Một khách gọi cà phê sữa (25.000đ), trà đào (35.000đ), cà phê đen (20.000đ): tổng 80.000đ.
- **Chia hóa đơn:** `80000/3` cho 26.666,666…; `80000//3` cho 26.666.

### Ý nghĩa từng toán tử
| Toán tử | Ví dụ | Ý nghĩa |
| :--- | :--- | :--- |
| `+` | `5 + 3` | Cộng; với hai chuỗi là nối chuỗi |
| `-` | `5 - 3` | Trừ |
| `*` | `5 * 3` | Nhân |
| `/` | `7 / 2` | Chia thực → 3.5 |
| `//` | `7 // 2` | Chia lấy thương làm tròn xuống → 3 |
| `%` | `7 % 2` | Phần dư → 1 |
| `**` | `2 ** 3` | Lũy thừa → 8 |

### Thứ tự ưu tiên và dấu ngoặc
Lũy thừa có ưu tiên cao, sau đó là nhân/chia, rồi cộng/trừ. Dùng `()` khi muốn chỉ rõ phép tính theo nghiệp vụ: tổng tiền trước giảm giá thường là tổng của các dòng hóa đơn, *sau đó* mới áp dụng tỷ lệ giảm.

> 📌 **Lưu ý:** Phép `//` làm tròn về âm vô cực. Vì thế `-7 // 2` bằng `-4`, không phải `-3`. Với `b ≠ 0`, quan hệ `a = (a // b) * b + (a % b)` luôn đúng theo quy tắc của Python.

### Ví dụ thực tiễn: giới hạn tồn kho
Cửa hàng có 41 chai si-rô và mỗi combo cần 6 chai. Cửa hàng có thể chuẩn bị tối đa bao nhiêu combo trọn vẹn? Còn dư bao nhiêu chai? (Xem minh họa tại **Ví dụ 12** bên dưới).

> ⚠️ **Lưu ý & Gợi ý:** Lỗi hay gặp: nhầm `/` với `//`, dùng dấu `^` thay cho lũy thừa `**`, hoặc chia cho 0 dẫn tới `ZeroDivisionError`.

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 10
```python
print(6/3)    # 2.0
print(7//2)   # 3
print(7%2)    # 1
print(2**3)   # 8
```
**Kết quả in ra (Output):**
```text
2.0
3
1
8
```

#### 🎯 THỰC HÀNH 02 · Tính hóa đơn bằng toán tử Python
**Mã nguồn khởi đầu (Điền vào chỗ trống `...`):**
```python
# Đơn giá: Cà phê sữa (25.000đ), Trà đào (35.000đ), Cà phê đen (20.000đ)
# Hãy thay các dấu ... bằng số lượng (ví dụ: 1 sữa, 1 trà đào, 1 đen):
so_sua = ...
so_tra = ...
so_den = ...
tong_tien = so_sua * 25000 + so_tra * 35000 + so_den * 20000
print("Tổng tiền hóa đơn:", tong_tien)
# Kết quả mong đợi (với 1 sữa, 1 trà, 1 đen): Tổng tiền hóa đơn: 80000
```
**Lời giải hoàn chỉnh:**
```python
so_sua = 1
so_tra = 1
so_den = 1
tong_tien = so_sua * 25000 + so_tra * 35000 + so_den * 20000
print("Tổng tiền hóa đơn:", tong_tien)
```
**Kết quả chạy trên Console:**
```text
Tổng tiền hóa đơn: 80000
```

#### ☕ PYTHON · Ví dụ 11
```python
print(2 + 3 * 4)
print((2 + 3) * 4)
print(7 / 2)
print(7 // 2)
print(-7 // 2)
print(-7 % 2)
```
**Kết quả in ra (Output):**
```text
14
20
3.5
3
-4
1
```

#### ☕ PYTHON · Ví dụ 12
```python
ton_kho = 41
moi_combo = 6
so_combo = ton_kho // moi_combo
con_du = ton_kho % moi_combo
print("Combo hoàn chỉnh:", so_combo)
print("Chai còn dư:", con_du)
```
**Kết quả in ra (Output):**
```text
Combo hoàn chỉnh: 6
Chai còn dư: 5
```

> ⚠️ **Lời khuyên thực hành:** Lỗi hay gặp: nhầm `/` với `//`, dùng dấu `^` thay cho lũy thừa `**`, hoặc chia cho 0 dẫn tới `ZeroDivisionError`.

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Kết quả của 7 // 2 là?

- [ ] **A.** 3
- [ ] **B.** 3.5
- [ ] **C.** 1

---

## MỤC 06/11: Chuỗi, bool và toán tử so sánh
> 📖 **Tham chiếu bài giảng:** PDF tr. 15–17 · **Chủ đề chính:** *Biểu diễn lời chào và điều kiện ưu đãi*

`str` lưu nội dung văn bản; `bool` lưu `True`/`False`. Kết quả so sánh thường là logic, ví dụ `tong_tien >= 50000`.

### 💡 Các khái niệm quan trọng:
- **So sánh:** `==`, `!=`, `<`, `>`, `<=`, `>=`.
- **Logic:** `and`: cả hai đúng; `or`: ít nhất một đúng; `not`: đảo đúng/sai.

### Chuỗi: dữ liệu văn bản và thao tác ghép
Một chuỗi được viết giữa dấu nháy đơn hoặc kép. Ta có thể ghép hai chuỗi bằng `+` hoặc truyền nhiều đối số cho `print()`. Chuỗi mang số vẫn là văn bản cho đến khi được chuyển kiểu.

### Toán tử so sánh và logic
| Nhóm | Toán tử | Ví dụ và ý nghĩa |
| :--- | :--- | :--- |
| So sánh | `==`, `!=` | Bằng; khác |
| So sánh | `>`, `<`, `>=`, `<=` | Lớn, nhỏ, lớn hoặc bằng, nhỏ hoặc bằng |
| Logic | `and` | Đúng khi cả hai điều kiện đúng |
| Logic | `or` | Đúng khi có ít nhất một điều kiện đúng |
| Logic | `not` | Đảo giá trị logic |

### Tình huống: quy tắc ưu đãi hai điều kiện
Giảm giá khi khách là thành viên **và** hóa đơn không dưới 50.000 đồng. Có thể thử đổi giá trị `la_thanh_vien = False` hoặc giảm giá trị `tong_tien` để quan sát sự thay đổi.

> 📌 **Phân biệt:** `=` là gán; `==` là so sánh. Trong Python đầy đủ, `and`/`or` có cơ chế đánh giá ngắn mạch và có thể trả về toán hạng; ở các bài nhập môn ta chủ yếu kết hợp các biểu thức logic.

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 13
```python
ten_khach = "Chị An"
ghi_chu = 'Note: "ít đường, nhiều đá"'
la_thanh_vien = True
tong_tien = 80000
duoc_giam = la_thanh_vien and (tong_tien >= 50000)
print(duoc_giam)  # True
```
**Kết quả in ra (Output):**
```text
True
```

#### 🎯 THỰC HÀNH 03 · Kiểm tra điều kiện ưu đãi (and / >=)
**Mã nguồn khởi đầu (Điền vào chỗ trống `...`):**
```python
# Điều kiện ưu đãi: Là thành viên VÀ tổng hóa đơn từ 50.000đ trở lên
la_thanh_vien = True
tong_tien = 75000
# Hãy thay dấu ... bằng toán tử so sánh thích hợp (>=):
duoc_giam = la_thanh_vien and (tong_tien ... 50000)
print("Được giảm giá:", duoc_giam)
# Kết quả mong đợi: Được giảm giá: True
```
**Lời giải hoàn chỉnh:**
```python
la_thanh_vien = True
tong_tien = 75000
duoc_giam = la_thanh_vien and (tong_tien >= 50000)
print("Được giảm giá:", duoc_giam)
```
**Kết quả chạy trên Console:**
```text
Được giảm giá: True
```

#### ☕ PYTHON · Ví dụ 14
```python
ten = "Minh"
mon = "Trà đào"
print("Khách:", ten, "| Món:", mon)
print("Phiếu: " + ten + " - " + mon)
```
**Kết quả in ra (Output):**
```text
Khách: Minh | Món: Trà đào
Phiếu: Minh - Trà đào
```

#### ☕ PYTHON · Ví dụ 15
```python
la_thanh_vien = True
tong_tien = 70000
du_dieu_kien = la_thanh_vien and tong_tien >= 50000
print("Có ưu đãi:", du_dieu_kien)
print("Không đủ điều kiện:", not du_dieu_kien)
```
**Kết quả in ra (Output):**
```text
Có ưu đãi: True
Không đủ điều kiện: False
```

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Khi la_thanh_vien=True nhưng tong_tien=40000, biểu thức la_thanh_vien and tong_tien>=50000 cho?

- [ ] **A.** True
- [ ] **B.** False
- [ ] **C.** "False"

---

## MỤC 07/11: Chuyển đổi kiểu dữ liệu
> 📖 **Tham chiếu bài giảng:** PDF tr. 18–20 · **Chủ đề chính:** *int(), float(), str() và lỗi phổ biến*

Một số dữ liệu ban đầu ở dạng chữ: `so_ban = "12"`. Khi làm phép tính cần chuyển sang số với `int()` hoặc `float()`. Khi ghép với văn bản dùng `str()`.

> 📌 **Ghi chú trọng tâm:** Cảnh báo: `float("Cà phê")` gây ValueError vì chuỗi không đại diện cho số. Tương tự, không cộng trực tiếp số nguyên với chuỗi.

### Vì sao phải ép kiểu?
Dữ liệu nhập qua biểu mẫu thường là chuỗi. Nếu coi `"3"` như số nguyên mà đem cộng số, Python sẽ báo `TypeError`. Khi cần tính toán ta dùng `int()` hoặc `float()`; khi cần ghép với chuỗi dùng `str()`.

| Cách chuyển | Kết quả | Lưu ý |
| :--- | :--- | :--- |
| `int("12")` | `12` | Chuỗi cần biểu diễn số nguyên hợp lệ |
| `float("12.5")` | `12.5` | Thường dùng dấu chấm cho thập phân trong mã Python |
| `str(12)` | `"12"` | Biến số thành văn bản |
| `int(3.9)` | `3` | Cắt phần lẻ theo hướng về 0; khác làm tròn |
| `bool(0)` | `False` | Giá trị 0 là sai trong ngữ cảnh logic |

### Lỗi thường gặp
`int("3.5")` và `float("Cà phê")` không thể thực hiện trực tiếp và sẽ gây lỗi giá trị. Khi nhận dữ liệu thực tế cần kiểm tra thông tin nhập, xử lý lỗi và quyết định có chấp nhận giá trị rỗng hay không.

> ⚠️ **Lưu ý & Gợi ý:** **Câu hỏi suy nghĩ:** Mã sinh viên như `"00123"` có nên đổi sang số nguyên không? Không nên nếu các số 0 đầu là một phần của mã định danh; giữ ở dạng chuỗi.

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 16
```python
so_ban = "12"
print("Quán có " + so_ban + " bàn")
print(int(so_ban) + 3)
# Quán có 12 bàn
# 15
```
**Kết quả in ra (Output):**
```text
Quán có 12 bàn
15
```

#### ☕ PYTHON · Ví dụ 17
```python
ten_mon = "Trà đào"
so_ly = 3
tong_tien = 35000 * so_ly
print(str(so_ly) + " ly " + ten_mon + " = " + str(tong_tien) + "đ")
# 3 ly Trà đào = 105000đ
```
**Kết quả in ra (Output):**
```text
3 ly Trà đào = 105000đ
```

#### ☕ PYTHON · Ví dụ 18
```python
so_ly_dang_chu = "3"
don_gia_dang_chu = "35000"
so_ly = int(so_ly_dang_chu)
don_gia = int(don_gia_dang_chu)
print("Thành tiền:", so_ly * don_gia)
print("Số ly: " + str(so_ly))
```
**Kết quả in ra (Output):**
```text
Thành tiền: 105000
Số ly: 3
```

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Cách nào dùng để ghép một biến số nguyên so_ly với chuỗi " ly"?

- [ ] **A.** so_ly + " ly"
- [ ] **B.** str(so_ly) + " ly"
- [ ] **C.** int(" ly") + so_ly

---

## MỤC 08/11: List và tuple
> 📖 **Tham chiếu bài giảng:** PDF tr. 21–22, 26 · **Chủ đề chính:** *Thực đơn có thể sửa và dữ liệu bất biến*

Cả `list` và `tuple` có thứ tự. List có thể thay đổi sau khi tạo; tuple không cho gán sửa phần tử.

### 💡 Các khái niệm quan trọng:
- **List · ngoặc vuông:** Phù hợp cho menu và các danh sách cần cập nhật.
- **Tuple · ngoặc tròn:** Phù hợp cho các nhóm giá trị theo vị trí mà không muốn thay phần tử.

### Điểm giống và khác của list – tuple
Cả hai là **dãy có thứ tự**, truy cập được bằng chỉ số và có thể chứa các kiểu dữ liệu khác nhau. Tuy nhiên `list` có thể thay đổi phần tử, còn `tuple` không thể gán lại phần tử bằng chỉ số. Điều này không có nghĩa là mọi đối tượng nằm bên trong tuple đều bất biến.

| Đặc tính | list | tuple |
| :--- | :--- | :--- |
| Cú pháp | `["Đen", "Sữa"]` | `("Đen", "Sữa")` |
| Thứ tự | Có | Có |
| Lấy phần tử `[0]` | Có | Có |
| Thay `[0] = ...` | Có | Không |
| Tình huống | Thực đơn cập nhật thường xuyên | Bộ tọa độ/ngày tháng đã xác định |

### List có thể đổi theo chỉ số
`list` trong Python có tính chất thay đổi được (`mutable`). Ta có thể dùng chỉ số để đổi món: `thuc_don[1] = "Cà phê muối"` (chi tiết xem tại **Ví dụ 20** và **Thực hành 04**).

### Tuple dùng để lưu bộ giá trị cố định
`tuple` có tính chất bất biến (`immutable`). Mọi thao tác gán lại phần tử như `ngay[0] = 17` sẽ báo lỗi `TypeError` (chi tiết xem tại **Ví dụ 21**).

> ⚠️ **Lưu ý & Gợi ý:** Trong Python, tên biến không phải “hộp chứa giá trị” theo nghĩa tuyệt đối mà tham chiếu đến đối tượng. Khi có hai tên cùng tham chiếu tới một list, sửa list qua tên này có thể được nhìn thấy qua tên kia. Phần này sẽ được đào sâu ở các bài lập trình tiếp theo.

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 19
```python
thuc_don = ["Cà phê đen", "Cà phê sữa", "Trà đào"]
ngay_khai_truong = (16, 12, 2023)
thuc_don[0] = "Cà phê muối"
print(thuc_don)
# ngày khai trương là tuple nên ngay_khai_truong[0] = 17 sẽ lỗi
```
**Kết quả in ra (Output):**
```text
['Cà phê muối', 'Cà phê sữa', 'Trà đào']
```

#### 🎯 THỰC HÀNH 04 · Đổi món thứ hai trong thực đơn (List Mutability)
**Mã nguồn khởi đầu (Điền vào chỗ trống `...`):**
```python
thuc_don = ["Cà phê đen", "Cà phê sữa", "Bạc xỉu", "Trà đào"]
# Món thứ hai ("Cà phê sữa") có chỉ số là bao nhiêu trong Python?
# Hãy thay ... bằng chỉ số đúng để đổi thành "Cà phê muối":
thuc_don[...] = "Cà phê muối"
print(thuc_don)
# Kết quả mong đợi: ['Cà phê đen', 'Cà phê muối', 'Bạc xỉu', 'Trà đào']
```
**Lời giải hoàn chỉnh:**
```python
thuc_don = ["Cà phê đen", "Cà phê sữa", "Bạc xỉu", "Trà đào"]
thuc_don[1] = "Cà phê muối"
print(thuc_don)
```
**Kết quả chạy trên Console:**
```text
['Cà phê đen', 'Cà phê muối', 'Bạc xỉu', 'Trà đào']
```

#### ☕ PYTHON · Ví dụ 20
```python
thuc_don = ["Đen", "Sữa", "Trà đào"]
print("Ban đầu:", thuc_don)
thuc_don[1] = "Cà phê muối"
print("Sau sửa:", thuc_don)
print("Có", len(thuc_don), "món")
```
**Kết quả in ra (Output):**
```text
Ban đầu: ['Đen', 'Sữa', 'Trà đào']
Sau sửa: ['Đen', 'Cà phê muối', 'Trà đào']
Có 3 món
```

#### ☕ PYTHON · Ví dụ 21
```python
ngay = (16, 12, 2026)
print(ngay)
print("Tháng:", ngay[1])
print("Số trường:", len(ngay))
```
**Kết quả in ra (Output):**
```text
(16, 12, 2026)
Tháng: 12
Số trường: 3
```

> ⚠️ **Lời khuyên thực hành:** Trong Python, tên biến không phải “hộp chứa giá trị” theo nghĩa tuyệt đối mà tham chiếu đến đối tượng. Khi có hai tên cùng tham chiếu tới một list, sửa list qua tên này có thể được nhìn thấy qua tên kia. Phần này sẽ được đào sâu ở các bài lập trình tiếp theo.

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Phát biểu nào đúng về list và tuple?

- [ ] **A.** Tuple thay phần tử bằng chỉ số được
- [ ] **B.** Cả hai không có thứ tự
- [ ] **C.** List có thể thay phần tử, tuple không

---

## MỤC 09/11: Indexing
> 📖 **Tham chiếu bài giảng:** PDF tr. 23 · **Chủ đề chính:** *Đếm vị trí từ 0 và từ cuối*

List bắt đầu đánh chỉ số từ `0`. Với bốn món, các chỉ số tiến là 0,1,2,3 và chỉ số âm là -4,-3,-2,-1.

> 📌 **Ghi chú trọng tâm:** Lỗi phổ biến: nhầm phần tử thứ ba với `[3]`. Phần tử thứ ba có chỉ số `2`.

### Chỉ số là gì?
Python đánh chỉ số từ **0**. Với bốn phần tử, chỉ số hợp lệ là `0, 1, 2, 3`. Chỉ số âm bắt đầu từ `-1` (phần tử cuối), `-2` (kế cuối). Nếu truy cập chỉ số ngoài phạm vi, Python báo `IndexError`.

| Phần tử | Đen | Sữa | Bạc xỉu | Trà đào |
| :--- | :--- | :--- | :--- | :--- |
| Chỉ số dương | 0 | 1 | 2 | 3 |
| Chỉ số âm | -4 | -3 | -2 | -1 |

### Ứng dụng trên dữ liệu giá bán
Indexing trả về *một* phần tử, còn slicing (học mục tiếp theo) thường trả về *một dãy con*. Phải phân biệt “món thứ ba” (chỉ số 2) với “món có chỉ số 3” (món thứ tư).

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 22
```python
thuc_don = ["Cà phê đen", "Cà phê sữa", "Bạc xỉu", "Trà đào"]
print(thuc_don[0])   # Cà phê đen
print(thuc_don[-1])  # Trà đào
```
**Kết quả in ra (Output):**
```text
Cà phê đen
Trà đào
```

#### 🎯 THỰC HÀNH 05 · Lấy món đầu và món cuối bằng chỉ số (Indexing)
**Mã nguồn khởi đầu (Điền vào chỗ trống `...`):**
```python
menu = ["Cà phê đen", "Cà phê sữa", "Bạc xỉu", "Trà đào"]
# Hãy thay các dấu ... bằng chỉ số để lấy món đầu tiên và món cuối cùng (dùng chỉ số âm):
mon_dau = menu[...]
mon_cuoi = menu[...]
print("Món đầu:", mon_dau)
print("Món cuối:", mon_cuoi)
# Kết quả mong đợi:
# Món đầu: Cà phê đen
# Món cuối: Trà đào
```
**Lời giải hoàn chỉnh:**
```python
menu = ["Cà phê đen", "Cà phê sữa", "Bạc xỉu", "Trà đào"]
mon_dau = menu[0]
mon_cuoi = menu[-1]
print("Món đầu:", mon_dau)
print("Món cuối:", mon_cuoi)
```
**Kết quả chạy trên Console:**
```text
Món đầu: Cà phê đen
Món cuối: Trà đào
```

#### ☕ PYTHON · Ví dụ 23
```python
gia_ban = [20000, 25000, 28000, 35000]
print("Giá đầu:", gia_ban[0])
print("Giá cuối:", gia_ban[-1])
print("Giá thứ ba:", gia_ban[2])
print("Số món:", len(gia_ban))
```
**Kết quả in ra (Output):**
```text
Giá đầu: 20000
Giá cuối: 35000
Giá thứ ba: 28000
Số món: 4
```

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Với bốn món, thuc_don[-2] chọn món ở vị trí nào?

- [ ] **A.** Thứ hai từ đầu
- [ ] **B.** Thứ hai từ cuối
- [ ] **C.** Món cuối

---

## MỤC 10/11: Slicing, set và tính bất biến
> 📖 **Tham chiếu bài giảng:** PDF tr. 24–26 · **Chủ đề chính:** *Cắt lát; loại trùng; mutable vs immutable*

**Slicing:** biểu thức `a[start:end]` lấy từ vị trí start đến ngay trước end. Set viết bằng ngoặc nhọn (với các phần tử) và không giữ phần tử trùng.

### 💡 Các khái niệm quan trọng:
- **Mutable:** `list` (cho sửa phần tử).
- **Immutable:** `tuple` và `str` (không sửa trực tiếp phần tử).
- **Set:** Không có indexing theo vị trí; bỏ phần tử trùng.

### Cú pháp slicing chi tiết
`a[start:stop:step]` lấy từ chỉ số `start`, dừng **trước** `stop`, và nhảy theo `step`. Có thể bỏ trống start/stop; chỉ số âm và bước âm cho phép duyệt ngược. Slicing không sửa list gốc mà tạo danh sách phần tử được chọn.

### Set: khi chỉ quan tâm phần tử duy nhất
Set loại phần tử trùng, không hỗ trợ truy cập bằng chỉ số vì đây không phải một dãy được sắp thứ tự. Trong Python thực tế, thứ tự hiển thị của set không phải thứ tự dữ liệu cần dựa vào. `{}` là dict rỗng, không phải set rỗng; dùng `set()` để tạo set rỗng.

### Mutable và immutable
`list` và `set` có thể thay đổi nội dung; `str`, `tuple`, `int` không cho chỉnh sửa tại chỗ theo cách tương tự. Khi “thay” một chuỗi, ta thực tế tạo giá trị chuỗi mới và gán lại cho tên biến.

> ⚠️ **Lưu ý & Gợi ý:** **Nhận xét:** set hữu ích khi kiểm tra danh mục ngành hàng không trùng, nhưng list thích hợp hơn khi cần giữ thứ tự xuất hiện và tra cứu theo vị trí.

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 24
```python
a = ["Cà phê đen", "Cà phê sữa", "Bạc xỉu", "Trà đào"]
print(a[1:3])
# ["Cà phê sữa", "Bạc xỉu"]
nhom = {"cà phê", "trà", "cà phê"}
print(len(nhom))  # 2
```
**Kết quả in ra (Output):**
```text
['Cà phê sữa', 'Bạc xỉu']
2
```

#### 🎯 THỰC HÀNH 06 · Cắt lát danh sách thực đơn (Slicing)
**Mã nguồn khởi đầu (Điền vào chỗ trống `...`):**
```python
menu = ["Cà phê đen", "Cà phê sữa", "Bạc xỉu", "Trà đào"]
# Hãy thay các dấu ... bằng chỉ số start và stop để lấy 2 món ở giữa ["Cà phê sữa", "Bạc xỉu"]:
lat_cat = menu[... : ...]
print(lat_cat)
# Kết quả mong đợi: ['Cà phê sữa', 'Bạc xỉu']
```
**Lời giải hoàn chỉnh:**
```python
menu = ["Cà phê đen", "Cà phê sữa", "Bạc xỉu", "Trà đào"]
lat_cat = menu[1:3]
print(lat_cat)
```
**Kết quả chạy trên Console:**
```text
['Cà phê sữa', 'Bạc xỉu']
```

#### ☕ PYTHON · Ví dụ 25
```python
a = [10, 20, 30, 40, 50]
print(a[1:4])
print(a[:3])
print(a[2:])
print(a[::2])
print(a[::-1])
```
**Kết quả in ra (Output):**
```text
[20, 30, 40]
[10, 20, 30]
[30, 40, 50]
[10, 30, 50]
[50, 40, 30, 20, 10]
```

#### ☕ PYTHON · Ví dụ 26
```python
nhom_do_uong = {"cà phê", "trà", "cà phê"}
print("Số loại nhóm:", len(nhom_do_uong))
print({1, 2, 3} == {3, 2, 1})
```
**Kết quả in ra (Output):**
```text
Số loại nhóm: 2
True
```

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Với a=["A","B","C","D"], a[1:3] trả về gì?

- [ ] **A.** ["A","B","C"]
- [ ] **B.** ["B","C"]
- [ ] **C.** ["B","C","D"]

---

## MỤC 11/11: Bài tập mẫu có lời giải
> 📖 **Tham chiếu bài giảng:** PDF tr. 19–20, 27–28 · **Chủ đề chính:** *Hai bài luyện tập trong PDF và ví dụ mở rộng*

**Bài mẫu 1 – Đơn trà đào.** Dữ liệu: giá 35.000đ/ly, còn hàng. Yêu cầu khai báo biến, xem kiểu và tính ba ly (Ví dụ 27).

**Bài mẫu 2 – Quản lý thực đơn.** In món đầu/cuối, thay món thứ hai, lấy hai món đầu (Ví dụ 28).

**Ví dụ mở rộng – Tính giảm 10% với đơn 155.000đ.** Kiểm tra điều kiện thành viên và tổng tiền để giảm giá (Ví dụ 29).

### Cách đọc đề và tự xây dựng lời giải
Với mỗi bài tập Python, sinh viên nên làm theo bốn bước: phân tích dữ liệu đầu vào; lập kế hoạch tính toán/thay đổi; viết chương trình tối giản; kiểm thử với ví dụ thường, ví dụ biên và kiểu dữ liệu bất thường. Nếu kết quả khác dự đoán, dùng `print()` để xem giá trị trung gian.

### Bài mẫu 3 – Dự toán doanh thu một buổi
Giả sử quán bán 12 ly cà phê đen (20.000đ), 8 ly cà phê sữa (25.000đ) và 5 ly trà đào (35.000đ). Hãy tính doanh thu, số ly bán được và doanh thu trung bình mỗi ly (Ví dụ 30). Đây là bài bổ sung so với slide.

### Bài mẫu 4 – Phân loại đơn hàng bằng điều kiện
Quán hỗ trợ miễn phí vận chuyển khi hóa đơn từ 100.000 đồng trở lên (Ví dụ 31). Ví dụ này mở rộng nhẹ tới cú pháp `if`/`else`; nội dung câu lệnh điều kiện sẽ được học kỹ ở buổi sau.

### Tự đánh giá trước khi chuyển sang quiz
Hãy thay `tong_tien` lần lượt bằng 100.000, 99.999 và 0. Quan sát sự khác biệt giữa `>` và `>=`, đồng thời kiểm tra số lượng/đơn giá âm có hợp lệ về mặt nghiệp vụ không.

> ⚠️ **Lưu ý & Gợi ý:** Bạn có thể chạy và sửa toàn bộ code mẫu, xem kết quả ngay dưới mỗi đoạn. Bộ chạy offline chỉ hỗ trợ phần cú pháp thuộc bài này và một số mở rộng đơn giản; chương trình Python đầy đủ cần môi trường như Google Colab.

### 💻 Mã nguồn thực hành & Ví dụ Python:
#### ☕ PYTHON · Ví dụ 27
```python
ten_mon = "Trà đào"
don_gia = 35000
con_hang = True
print(type(ten_mon))  # <class 'str'>
print(type(don_gia)) # <class 'int'>
print(type(con_hang))# <class 'bool'>
so_ly = 3
tong_tien = don_gia * so_ly
print(str(so_ly) + " ly " + ten_mon + " = " + str(tong_tien) + "đ")
# 3 ly Trà đào = 105000đ
```
**Kết quả in ra (Output):**
```text
<class 'str'>
<class 'int'>
<class 'bool'>
3 ly Trà đào = 105000đ
```

#### ☕ PYTHON · Ví dụ 28
```python
thuc_don = ["Cà phê đen", "Cà phê sữa", "Bạc xỉu", "Trà đào"]
print(thuc_don[0])   # Cà phê đen
print(thuc_don[-1])  # Trà đào
thuc_don[1] = "Cà phê muối"
print(thuc_don[0:2]) # ["Cà phê đen", "Cà phê muối"]
```
**Kết quả in ra (Output):**
```text
Cà phê đen
Trà đào
['Cà phê đen', 'Cà phê muối']
```

#### ☕ PYTHON · Ví dụ 29
```python
tong_tien = 155000
la_thanh_vien = True
if la_thanh_vien and tong_tien >= 100000:
    tong_tien = tong_tien * 0.9
print(tong_tien) # 139500.0
```
**Kết quả in ra (Output):**
```text
139500.0
```

#### ☕ PYTHON · Ví dụ 30
```python
so_den = 12
so_sua = 8
so_tra = 5
doanh_thu = so_den * 20000 + so_sua * 25000 + so_tra * 35000
so_ly = so_den + so_sua + so_tra
trung_binh = doanh_thu / so_ly
print("Số ly bán:", so_ly)
print("Doanh thu:", doanh_thu)
print("Doanh thu trung bình mỗi ly:", trung_binh)
```
**Kết quả in ra (Output):**
```text
Số ly bán: 25
Doanh thu: 615000
Doanh thu trung bình mỗi ly: 24600.0
```

#### ☕ PYTHON · Ví dụ 31
```python
tong_tien = 125000
if tong_tien >= 100000:
    print("Miễn phí vận chuyển")
else:
    print("Thu phí vận chuyển")
```
**Kết quả in ra (Output):**
```text
Miễn phí vận chuyển
```

### 🛡️ Câu hỏi chốt chặn qua bài (Kiểm tra trước khi qua mục tiếp theo):
**Câu hỏi:** Sau lệnh thuc_don[1] = "Cà phê muối", món nào ở vị trí 1?

- [ ] **A.** Cà phê đen
- [ ] **B.** Cà phê muối
- [ ] **C.** Bạc xỉu

---

## ĐÁNH GIÁ CUỐI BÀI: Kiểm tra tổng kết & Chứng nhận hoàn thành
> Để nhận chứng nhận hoàn thành bài học, người học cần trả lời đúng **tối thiểu 7/8 câu hỏi tổng kết**.

### Câu 1. Lệnh in chuỗi trong Python là gì?
- [ ] **A.** show("Hi")
- [ ] **B.** print("Hi")
- [ ] **C.** write("Hi")

### Câu 2. Giá trị "12" thuộc kiểu gì?
- [ ] **A.** int
- [ ] **B.** str
- [ ] **C.** bool

### Câu 3. 7 % 3 trả về gì?
- [ ] **A.** 1
- [ ] **B.** 2
- [ ] **C.** 3

### Câu 4. Kết quả của 6 / 3 trong Python 3?
- [ ] **A.** 2
- [ ] **B.** 2.0
- [ ] **C.** 3

### Câu 5. a=["A","B","C"]; a[-1] là gì?
- [ ] **A.** A
- [ ] **B.** B
- [ ] **C.** C

### Câu 6. Tuple có thể gán sửa phần tử không?
- [ ] **A.** Có
- [ ] **B.** Không
- [ ] **C.** Chỉ sửa phần tử đầu

### Câu 7. a=[1,2,3,4]; a[1:3] là gì?
- [ ] **A.** [2,3]
- [ ] **B.** [1,2,3]
- [ ] **C.** [2,3,4]

### Câu 8. Nếu thành viên=True, tổng=40000, điều kiện member and total>=50000?
- [ ] **A.** True
- [ ] **B.** False
- [ ] **C.** 40000

---

## 🎓 Mẫu chứng nhận hoàn thành bài học (Certificate Text Format)
Khi sinh viên đạt từ 7/8 câu trở lên và hoàn thành đầy đủ 11 mục học, hệ thống sẽ cấp mã chứng nhận offline và cho phép xuất ảnh PNG chứng nhận theo mẫu:
```text
========================================================================================
                      CỔNG HỌC LIỆU TRỰC TUYẾN · DATA SCIENCE
                          CHỨNG NHẬN HOÀN THÀNH BÀI HỌC
                               XÁC NHẬN NGƯỜI HỌC
                               
Họ và tên:     [Tên sinh viên]
Mã học viên:   [Mã sinh viên]   |   Lớp / Khóa: [Mã lớp]
Nội dung:      BÀI 2: GIỚI THIỆU NGÔN NGỮ LẬP TRÌNH PYTHON
Tiến độ:       11/11 mục học hoàn thành
Kiểm tra cuối: [Điểm]/8 câu đạt chuẩn
Hình thức:     Tự học và đánh giá offline trên trình duyệt tương tác
Mã xác nhận:   DS2-[MãSV]-[MãNgẫuNhiên]
========================================================================================
```

---

## 🔑 Bảng đáp án & Giải thích (Answer Key)

### 1. Đáp án câu hỏi chốt chặn từng mục (11 Checkpoints)
| Mục | Tiêu đề chuyên đề | Đáp án | Giải thích ngắn gọn |
| :---: | :--- | :---: | :--- |
| **01** | Bắt đầu từ quán cà phê | **B** | List cho phép thay đổi phần tử theo chỉ số. |
| **02** | Python và Google Colab | **B** | Code cell thực thi Python, Text cell dùng cho phần diễn giải. |
| **03** | Biến và phép gán | **B** | Python không cho tên biến bắt đầu bằng chữ số hoặc chứa dấu `-`. |
| **04** | Các kiểu dữ liệu cơ bản | **B** | Dấu nháy biến `25` thành một chuỗi ký tự (`str`). |
| **05** | Toán tử số học | **A** | Với số dương, `//` cho thương nguyên `3`. |
| **06** | Chuỗi, bool và so sánh | **B** | Điều kiện thứ hai không đạt (`tong_tien >= 50000` là `False`), nên `and` cho `False`. |
| **07** | Chuyển đổi kiểu dữ liệu | **B** | Để nối chuỗi với số cần ép kiểu số thành chuỗi bằng `str()`. |
| **08** | List và tuple | **C** | Tính mutability (khả năng thay đổi phần tử) là điểm khác biệt then chốt giữa list và tuple. |
| **09** | Indexing | **B** | Chỉ số âm `-2` là phần tử thứ hai khi đếm ngược từ cuối danh sách. |
| **10** | Slicing, set và tính bất biến | **B** | Slice `[1:3]` lấy từ chỉ số 1 đến trước chỉ số 3 (chỉ số 1 và 2). |
| **11** | Bài tập mẫu có lời giải | **B** | Lệnh gán `thuc_don[1] = ...` đã thay thế phần tử tại vị trí chỉ số 1 thành `"Cà phê muối"`. |

### 2. Đáp án bài kiểm tra tổng kết cuối bài (8 câu Quiz)
| Câu | Đáp án đúng | Chi tiết phương án |
| :---: | :---: | :--- |
| **1** | **B** | `print("Hi")` |
| **2** | **B** | `str` |
| **3** | **A** | `1` |
| **4** | **B** | `2.0` |
| **5** | **C** | `C` |
| **6** | **B** | `Không` |
| **7** | **A** | `[2,3]` |
| **8** | **B** | `False` |

