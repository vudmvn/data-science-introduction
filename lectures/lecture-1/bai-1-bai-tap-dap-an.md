# Ngân hàng Bài Tập & Đáp Án Chi Tiết — Bài 1: Giới thiệu về Khoa học Dữ liệu
## Học phần: Khoa học Dữ liệu Cơ bản trong Kinh tế & Kinh doanh (FDA.6.1.2.01.V) — NEU

> **Đề bài tự luyện không đáp án:** [`bai-1-bai-tap-tu-lam.md`](./bai-1-bai-tap-tu-lam.md)  
> **Tệp giao diện tự chấm trực tuyến:** [`bai-1-bai-tap-tu-lam.html`](./bai-1-bai-tap-tu-lam.html)  
> **Quy mô:** 12 bài tập lớn · 66 ý tự chấm · **Thang điểm:** 100 điểm

---

## 📋 Bảng tra cứu đáp án nhanh (Quick Answer Key)

| Mã ý | Bài tập | Dạng | Điểm | Đáp án chuẩn |
| :---: | :--- | :---: | :---: | :--- |
| `p01a` | Phân loại biến dữ liệu | `select` | 1đ | **A** (Định tính danh nghĩa) |
| `p01b` | Phân loại biến dữ liệu | `select` | 1đ | **C** (Định lượng rời rạc) |
| `p01c` | Phân loại biến dữ liệu | `select` | 1đ | **D** (Định lượng liên tục) |
| `p01d` | Phân loại biến dữ liệu | `select` | 1đ | **B** (Định tính thứ bậc) |
| `p01e` | Phân loại biến dữ liệu | `select` | 1đ | **A** (Định tính danh nghĩa) |
| `p01f` | Phân loại biến dữ liệu | `select` | 1đ | **C** (Định lượng rời rạc) |
| `p021` | Sắp xếp quy trình CRISP-DM | `select` | 1đ | **A** (1. Hiểu nghiệp vụ) |
| `p022` | Sắp xếp quy trình CRISP-DM | `select` | 1đ | **B** (2. Hiểu dữ liệu) |
| `p023` | Sắp xếp quy trình CRISP-DM | `select` | 1đ | **C** (3. Chuẩn bị dữ liệu) |
| `p024` | Sắp xếp quy trình CRISP-DM | `select` | 1đ | **D** (4. Xây dựng mô hình) |
| `p025` | Sắp xếp quy trình CRISP-DM | `select` | 1đ | **E** (5. Đánh giá) |
| `p026` | Sắp xếp quy trình CRISP-DM | `select` | 1đ | **F** (6. Triển khai) |
| `p03a` | Xác định giai đoạn xử lý công việc | `select` | 1đ | **A** (1. Hiểu nghiệp vụ) |
| `p03b` | Xác định giai đoạn xử lý công việc | `select` | 1đ | **B** (2. Hiểu dữ liệu) |
| `p03c` | Xác định giai đoạn xử lý công việc | `select` | 1đ | **C** (3. Chuẩn bị dữ liệu) |
| `p03d` | Xác định giai đoạn xử lý công việc | `select` | 1đ | **D** (4. Xây dựng mô hình) |
| `p03e` | Xác định giai đoạn xử lý công việc | `select` | 1đ | **E** (5. Đánh giá) |
| `p03f` | Xác định giai đoạn xử lý công việc | `select` | 1đ | **F** (6. Triển khai) |
| `p04a` | Xác định đúng bài toán kinh doanh | `select` | 1đ | **B** (Sản phẩm, khu vực và kênh nào kéo giảm doanh thu?) |
| `p04b` | Xác định đúng bài toán kinh doanh | `multi` | 3đ | **A, B, C, E** |
| `p04c` | Xác định đúng bài toán kinh doanh | `select` | 1đ | **A** (Một danh sách nguyên nhân có bằng chứng và đề xuất cải thiện) |
| `p04d` | Xác định đúng bài toán kinh doanh | `select` | 1đ | **B** (Xác định nhóm gây sụt giảm và có giải pháp đo được) |
| `p04e` | Xác định đúng bài toán kinh doanh | `select` | 1đ | **C** (Ghi rõ hạn chế và bổ sung/đối soát nguồn phù hợp) |
| `p05a` | Kiểm tra chất lượng dữ liệu | `select` | 2đ | **A** (Kiểm tra khóa/mã giao dịch, đối soát và gỡ bản ghi trùng hợp lệ) |
| `p05b` | Kiểm tra chất lượng dữ liệu | `select` | 2đ | **B** (Đối soát hóa đơn gốc, xác định nguyên nhân và quy tắc xử lý) |
| `p05c` | Kiểm tra chất lượng dữ liệu | `select` | 2đ | **B** (Kiểm tra chính sách hoàn tiền và giữ/biểu diễn đúng nghiệp vụ) |
| `p05d` | Kiểm tra chất lượng dữ liệu | `select` | 1đ | **A** (Đối chiếu nguồn gốc vì đây là ngày không hợp lệ) |
| `p05e` | Kiểm tra chất lượng dữ liệu | `select` | 1đ | **A** (Xác nhận quy tắc locale trước khi chuyển thành số) |
| `p05f` | Kiểm tra chất lượng dữ liệu | `select` | 1đ | **A** (Kiểm tra lại tính đầy đủ, chính xác, duy nhất và nhất quán) |
| `p06a` | Tính toán số liệu bán lẻ | `number` | 3đ | **40** |
| `p06b` | Tính toán số liệu bán lẻ | `number` | 2đ | **20** |
| `p06c` | Tính toán số liệu bán lẻ | `number` | 2đ | **58,333333** |
| `p06d` | Tính toán số liệu bán lẻ | `number` | 2đ | **480** |
| `p06e` | Tính toán số liệu bán lẻ | `number` | 2đ | **8** |
| `p07a` | Phân biệt bốn loại phân tích | `select` | 1đ | **A** (Mô tả) |
| `p07b` | Phân biệt bốn loại phân tích | `select` | 1đ | **B** (Chẩn đoán) |
| `p07c` | Phân biệt bốn loại phân tích | `select` | 1đ | **C** (Dự báo) |
| `p07d` | Phân biệt bốn loại phân tích | `select` | 1đ | **D** (Đề xuất) |
| `p07e` | Phân biệt bốn loại phân tích | `select` | 1đ | **A** (Mô tả) |
| `p07f` | Phân biệt bốn loại phân tích | `select` | 1đ | **D** (Đề xuất) |
| `p08a` | Chọn biểu đồ đúng mục tiêu | `select` | 1đ | **A** (Biểu đồ đường) |
| `p08b` | Chọn biểu đồ đúng mục tiêu | `select` | 1đ | **B** (Biểu đồ cột) |
| `p08c` | Chọn biểu đồ đúng mục tiêu | `select` | 1đ | **C** (Scatter plot) |
| `p08d` | Chọn biểu đồ đúng mục tiêu | `select` | 1đ | **D** (Histogram) |
| `p08e` | Chọn biểu đồ đúng mục tiêu | `select` | 1đ | **E** (Boxplot) |
| `p08f` | Chọn biểu đồ đúng mục tiêu | `select` | 1đ | **F** (Dashboard) |
| `p09a` | Bài toán chiến dịch ngân hàng (tính kỳ vọng) | `number` | 3đ | **40000** |
| `p09b` | Bài toán chiến dịch ngân hàng (tính kỳ vọng) | `number` | 3đ | **0** |
| `p09c` | Bài toán chiến dịch ngân hàng (tính kỳ vọng) | `number` | 3đ | **70000** |
| `p09d` | Bài toán chiến dịch ngân hàng (tính kỳ vọng) | `select` | 2đ | **C** (C) |
| `p09e` | Bài toán chiến dịch ngân hàng (tính kỳ vọng) | `number` | 3đ | **6,4** |
| `p10a` | Đánh giá tình huống ngân hàng | `select` | 2đ | **A** (Khách hàng có phản hồi/đồng ý gửi tiết kiệm không) |
| `p10b` | Đánh giá tình huống ngân hàng | `multi` | 3đ | **A, B, C** |
| `p10c` | Đánh giá tình huống ngân hàng | `select` | 2đ | **A** (Danh sách KH ưu tiên liên hệ và kênh khuyến nghị) |
| `p10d` | Đánh giá tình huống ngân hàng | `select` | 1đ | **A** (Chi phí trên mỗi khách hàng chuyển đổi) |
| `p10e` | Đánh giá tình huống ngân hàng | `select` | 1đ | **B** (Đánh giá sai lệch, làm lại mô hình/đặc trưng trước triển khai) |
| `p11a` | Diễn giải kết quả và hạn chế | `select` | 2đ | **B** (Có mối liên hệ; cần thiết kế phân tích bổ sung để đánh giá tác động nhân quả) |
| `p11b` | Diễn giải kết quả và hạn chế | `select` | 2đ | **A** (Chưa thể, vì mẫu có thể không đại diện) |
| `p11c` | Diễn giải kết quả và hạn chế | `select` | 2đ | **A** (Kết luận chính, tác động kinh doanh, đề xuất và giới hạn) |
| `p11d` | Diễn giải kết quả và hạn chế | `select` | 1đ | **A** (Có, vì dữ liệu và hành vi có thể thay đổi) |
| `p11e` | Diễn giải kết quả và hạn chế | `select` | 1đ | **A** (Xác minh quyền sử dụng, mục đích, bảo mật và mức cần thiết) |
| `p12a` | Dự án tổng hợp: giảm tồn kho thiếu hụt | `select` | 2đ | **B** (Mức đặt hàng/tồn kho hợp lý theo mặt hàng và cửa hàng) |
| `p12b` | Dự án tổng hợp: giảm tồn kho thiếu hụt | `multi` | 4đ | **A, B, C** |
| `p12c` | Dự án tổng hợp: giảm tồn kho thiếu hụt | `select` | 2đ | **A** (Dự báo nhu cầu theo sản phẩm/cửa hàng) |
| `p12d` | Dự án tổng hợp: giảm tồn kho thiếu hụt | `select` | 2đ | **A** (Prescriptive Analytics (phân tích đề xuất)) |
| `p12e` | Dự án tổng hợp: giảm tồn kho thiếu hụt | `select` | 2đ | **A** (Tỷ lệ thiếu hàng và chi phí tồn kho) |

---

## 📝 Lời giải và hướng dẫn chi tiết từng bài

## Bài 01. Phân loại biến dữ liệu
- **Mã bài:** `p01` | **Cấp độ:** `Cơ bản` | **Thang điểm:** `6 điểm` | **Tài liệu:** PDF tr. 12

> **Bối cảnh:** Một cửa hàng có các cột dữ liệu sau. Chọn loại phù hợp nhất cho **từng biến**. Các mức hài lòng 1–5 được xem là mức xếp hạng có thứ tự, không mặc định khoảng cách giữa mức là bằng nhau.  
> 💡 **Gợi ý:** Phân biệt nhãn không có thứ tự, nhãn có thứ tự, số đếm và đại lượng đo lường.

### Ý 1. Kênh mua hàng: online, tại quầy
- **Mã ý:** `p01a` | **Thang điểm:** `1 điểm`

- [x] **A.** Định tính danh nghĩa
- [ ] **B.** Định tính thứ bậc
- [ ] **C.** Định lượng rời rạc
- [ ] **D.** Định lượng liên tục

> **Đáp án đúng:** **A. Định tính danh nghĩa**  
> **Giải thích:** Đây là nhãn phân nhóm, không có thứ tự tự nhiên.

---

### Ý 2. Số đơn hàng trong tháng
- **Mã ý:** `p01b` | **Thang điểm:** `1 điểm`

- [ ] **A.** Định tính danh nghĩa
- [ ] **B.** Định tính thứ bậc
- [x] **C.** Định lượng rời rạc
- [ ] **D.** Định lượng liên tục

> **Đáp án đúng:** **C. Định lượng rời rạc**  
> **Giải thích:** Số đơn là phép đếm, nhận giá trị nguyên không âm.

---

### Ý 3. Giá trị thanh toán đo bằng VNĐ
- **Mã ý:** `p01c` | **Thang điểm:** `1 điểm`

- [ ] **A.** Định tính danh nghĩa
- [ ] **B.** Định tính thứ bậc
- [ ] **C.** Định lượng rời rạc
- [x] **D.** Định lượng liên tục

> **Đáp án đúng:** **D. Định lượng liên tục**  
> **Giải thích:** Trong mô hình nhập môn, đây là biến định lượng đo lường; dù ghi nhận theo đơn vị tiền nhỏ nhất, thường được xử lý như định lượng liên tục.

---

### Ý 4. Mức hài lòng: rất thấp, thấp, trung bình, cao, rất cao
- **Mã ý:** `p01d` | **Thang điểm:** `1 điểm`

- [ ] **A.** Định tính danh nghĩa
- [x] **B.** Định tính thứ bậc
- [ ] **C.** Định lượng rời rạc
- [ ] **D.** Định lượng liên tục

> **Đáp án đúng:** **B. Định tính thứ bậc**  
> **Giải thích:** Các mức có thứ tự nhưng không nhất thiết cách đều.

---

### Ý 5. Mã khách hàng: KH01, KH02, KH03
- **Mã ý:** `p01e` | **Thang điểm:** `1 điểm`

- [x] **A.** Định tính danh nghĩa
- [ ] **B.** Định tính thứ bậc
- [ ] **C.** Định lượng rời rạc
- [ ] **D.** Định lượng liên tục

> **Đáp án đúng:** **A. Định tính danh nghĩa**  
> **Giải thích:** Mã dùng định danh, không phải số lượng hay giá trị đo.

---

### Ý 6. Số sản phẩm trong giỏ hàng
- **Mã ý:** `p01f` | **Thang điểm:** `1 điểm`

- [ ] **A.** Định tính danh nghĩa
- [ ] **B.** Định tính thứ bậc
- [x] **C.** Định lượng rời rạc
- [ ] **D.** Định lượng liên tục

> **Đáp án đúng:** **C. Định lượng rời rạc**  
> **Giải thích:** Số sản phẩm là số đếm rời rạc.

---

## Bài 02. Sắp xếp quy trình CRISP-DM
- **Mã bài:** `p02` | **Cấp độ:** `Cơ bản` | **Thang điểm:** `6 điểm` | **Tài liệu:** PDF tr. 9–10

> **Bối cảnh:** Điền **giai đoạn** tương ứng với từng vị trí của quy trình cơ bản trong bài giảng.  
> 💡 **Gợi ý:** Quy trình bắt đầu từ quyết định kinh doanh, kết thúc ở triển khai, nhưng có thể lặp lại khi cần.

### Ý 1. Vị trí thứ 1
- **Mã ý:** `p021` | **Thang điểm:** `1 điểm`

- [x] **A.** 1. Hiểu nghiệp vụ
- [ ] **B.** 2. Hiểu dữ liệu
- [ ] **C.** 3. Chuẩn bị dữ liệu
- [ ] **D.** 4. Xây dựng mô hình
- [ ] **E.** 5. Đánh giá
- [ ] **F.** 6. Triển khai

> **Đáp án đúng:** **A. 1. Hiểu nghiệp vụ**  
> **Giải thích:** Thứ tự chuẩn trong mô hình CRISP-DM của bài giảng: Hiểu nghiệp vụ → Hiểu dữ liệu → Chuẩn bị dữ liệu → Xây dựng mô hình → Đánh giá → Triển khai.

---

### Ý 2. Vị trí thứ 2
- **Mã ý:** `p022` | **Thang điểm:** `1 điểm`

- [ ] **A.** 1. Hiểu nghiệp vụ
- [x] **B.** 2. Hiểu dữ liệu
- [ ] **C.** 3. Chuẩn bị dữ liệu
- [ ] **D.** 4. Xây dựng mô hình
- [ ] **E.** 5. Đánh giá
- [ ] **F.** 6. Triển khai

> **Đáp án đúng:** **B. 2. Hiểu dữ liệu**  
> **Giải thích:** Thứ tự chuẩn trong mô hình CRISP-DM của bài giảng: Hiểu nghiệp vụ → Hiểu dữ liệu → Chuẩn bị dữ liệu → Xây dựng mô hình → Đánh giá → Triển khai.

---

### Ý 3. Vị trí thứ 3
- **Mã ý:** `p023` | **Thang điểm:** `1 điểm`

- [ ] **A.** 1. Hiểu nghiệp vụ
- [ ] **B.** 2. Hiểu dữ liệu
- [x] **C.** 3. Chuẩn bị dữ liệu
- [ ] **D.** 4. Xây dựng mô hình
- [ ] **E.** 5. Đánh giá
- [ ] **F.** 6. Triển khai

> **Đáp án đúng:** **C. 3. Chuẩn bị dữ liệu**  
> **Giải thích:** Thứ tự chuẩn trong mô hình CRISP-DM của bài giảng: Hiểu nghiệp vụ → Hiểu dữ liệu → Chuẩn bị dữ liệu → Xây dựng mô hình → Đánh giá → Triển khai.

---

### Ý 4. Vị trí thứ 4
- **Mã ý:** `p024` | **Thang điểm:** `1 điểm`

- [ ] **A.** 1. Hiểu nghiệp vụ
- [ ] **B.** 2. Hiểu dữ liệu
- [ ] **C.** 3. Chuẩn bị dữ liệu
- [x] **D.** 4. Xây dựng mô hình
- [ ] **E.** 5. Đánh giá
- [ ] **F.** 6. Triển khai

> **Đáp án đúng:** **D. 4. Xây dựng mô hình**  
> **Giải thích:** Thứ tự chuẩn trong mô hình CRISP-DM của bài giảng: Hiểu nghiệp vụ → Hiểu dữ liệu → Chuẩn bị dữ liệu → Xây dựng mô hình → Đánh giá → Triển khai.

---

### Ý 5. Vị trí thứ 5
- **Mã ý:** `p025` | **Thang điểm:** `1 điểm`

- [ ] **A.** 1. Hiểu nghiệp vụ
- [ ] **B.** 2. Hiểu dữ liệu
- [ ] **C.** 3. Chuẩn bị dữ liệu
- [ ] **D.** 4. Xây dựng mô hình
- [x] **E.** 5. Đánh giá
- [ ] **F.** 6. Triển khai

> **Đáp án đúng:** **E. 5. Đánh giá**  
> **Giải thích:** Thứ tự chuẩn trong mô hình CRISP-DM của bài giảng: Hiểu nghiệp vụ → Hiểu dữ liệu → Chuẩn bị dữ liệu → Xây dựng mô hình → Đánh giá → Triển khai.

---

### Ý 6. Vị trí thứ 6
- **Mã ý:** `p026` | **Thang điểm:** `1 điểm`

- [ ] **A.** 1. Hiểu nghiệp vụ
- [ ] **B.** 2. Hiểu dữ liệu
- [ ] **C.** 3. Chuẩn bị dữ liệu
- [ ] **D.** 4. Xây dựng mô hình
- [ ] **E.** 5. Đánh giá
- [x] **F.** 6. Triển khai

> **Đáp án đúng:** **F. 6. Triển khai**  
> **Giải thích:** Thứ tự chuẩn trong mô hình CRISP-DM của bài giảng: Hiểu nghiệp vụ → Hiểu dữ liệu → Chuẩn bị dữ liệu → Xây dựng mô hình → Đánh giá → Triển khai.

---

## Bài 03. Xác định giai đoạn xử lý công việc
- **Mã bài:** `p03` | **Cấp độ:** `Cơ bản` | **Thang điểm:** `6 điểm` | **Tài liệu:** PDF tr. 10–13

> **Bối cảnh:** Ghép công việc trong một dự án dự báo rời bỏ dịch vụ vào giai đoạn CRISP-DM phù hợp nhất.  
> 💡 **Gợi ý:** Ghi nhớ đầu ra của từng bước: mục tiêu nghiệp vụ, khám phá dữ liệu, tập sạch, mô hình, đánh giá và vận hành.

### Ý 1. Thống nhất thế nào là “rời bỏ dịch vụ” và chi phí mất khách
- **Mã ý:** `p03a` | **Thang điểm:** `1 điểm`

- [x] **A.** 1. Hiểu nghiệp vụ
- [ ] **B.** 2. Hiểu dữ liệu
- [ ] **C.** 3. Chuẩn bị dữ liệu
- [ ] **D.** 4. Xây dựng mô hình
- [ ] **E.** 5. Đánh giá
- [ ] **F.** 6. Triển khai

> **Đáp án đúng:** **A. 1. Hiểu nghiệp vụ**  
> **Giải thích:** Xác định bài toán và mục tiêu kinh doanh là Business Understanding.

---

### Ý 2. Kiểm tra tỷ lệ thiếu của các biến trong bảng CRM
- **Mã ý:** `p03b` | **Thang điểm:** `1 điểm`

- [ ] **A.** 1. Hiểu nghiệp vụ
- [x] **B.** 2. Hiểu dữ liệu
- [ ] **C.** 3. Chuẩn bị dữ liệu
- [ ] **D.** 4. Xây dựng mô hình
- [ ] **E.** 5. Đánh giá
- [ ] **F.** 6. Triển khai

> **Đáp án đúng:** **B. 2. Hiểu dữ liệu**  
> **Giải thích:** Đánh giá chất lượng dữ liệu hiện có nằm ở Data Understanding.

---

### Ý 3. Chuẩn hóa số điện thoại, loại bản ghi trùng
- **Mã ý:** `p03c` | **Thang điểm:** `1 điểm`

- [ ] **A.** 1. Hiểu nghiệp vụ
- [ ] **B.** 2. Hiểu dữ liệu
- [x] **C.** 3. Chuẩn bị dữ liệu
- [ ] **D.** 4. Xây dựng mô hình
- [ ] **E.** 5. Đánh giá
- [ ] **F.** 6. Triển khai

> **Đáp án đúng:** **C. 3. Chuẩn bị dữ liệu**  
> **Giải thích:** Làm sạch và chuẩn bị dữ liệu thuộc Data Preparation.

---

### Ý 4. Huấn luyện mô hình phân loại nguy cơ rời bỏ
- **Mã ý:** `p03d` | **Thang điểm:** `1 điểm`

- [ ] **A.** 1. Hiểu nghiệp vụ
- [ ] **B.** 2. Hiểu dữ liệu
- [ ] **C.** 3. Chuẩn bị dữ liệu
- [x] **D.** 4. Xây dựng mô hình
- [ ] **E.** 5. Đánh giá
- [ ] **F.** 6. Triển khai

> **Đáp án đúng:** **D. 4. Xây dựng mô hình**  
> **Giải thích:** Huấn luyện mô hình là Modeling.

---

### Ý 5. Đo độ chính xác và so với KPI giữ chân khách hàng
- **Mã ý:** `p03e` | **Thang điểm:** `1 điểm`

- [ ] **A.** 1. Hiểu nghiệp vụ
- [ ] **B.** 2. Hiểu dữ liệu
- [ ] **C.** 3. Chuẩn bị dữ liệu
- [ ] **D.** 4. Xây dựng mô hình
- [x] **E.** 5. Đánh giá
- [ ] **F.** 6. Triển khai

> **Đáp án đúng:** **E. 5. Đánh giá**  
> **Giải thích:** Kiểm thử và xem sự phù hợp với KPI là Evaluation.

---

### Ý 6. Tích hợp danh sách cảnh báo vào hệ thống CRM
- **Mã ý:** `p03f` | **Thang điểm:** `1 điểm`

- [ ] **A.** 1. Hiểu nghiệp vụ
- [ ] **B.** 2. Hiểu dữ liệu
- [ ] **C.** 3. Chuẩn bị dữ liệu
- [ ] **D.** 4. Xây dựng mô hình
- [ ] **E.** 5. Đánh giá
- [x] **F.** 6. Triển khai

> **Đáp án đúng:** **F. 6. Triển khai**  
> **Giải thích:** Đưa mô hình vào sử dụng là Deployment.

---

## Bài 04. Xác định đúng bài toán kinh doanh
- **Mã bài:** `p04` | **Cấp độ:** `Cơ bản` | **Thang điểm:** `7 điểm` | **Tài liệu:** PDF tr. 11

> **Bối cảnh:** Doanh thu một chuỗi cửa hàng giảm hai tháng gần đây. Hãy lựa chọn các yếu tố phục vụ việc xây dựng đề bài phân tích.  
> 💡 **Gợi ý:** Bắt đầu bằng câu hỏi người quản lý cần quyết định gì, tiếp theo mới xác định dữ liệu và chỉ số.

### Ý 1. Câu hỏi phân tích phù hợp nhất
- **Mã ý:** `p04a` | **Thang điểm:** `1 điểm`

- [ ] **A.** Chọn Python hay R?
- [x] **B.** Sản phẩm, khu vực và kênh nào kéo giảm doanh thu?
- [ ] **C.** Sử dụng mạng nơ-ron nào?

> **Đáp án đúng:** **B. Sản phẩm, khu vực và kênh nào kéo giảm doanh thu?**  
> **Giải thích:** Câu hỏi này gắn với việc tìm nguyên nhân và cải thiện kinh doanh.

---

### Ý 2. Chọn các dữ liệu trực tiếp hữu ích để phân tích doanh thu giảm
- **Mã ý:** `p04b` | **Thang điểm:** `3 điểm`

- [x] **A.** Doanh số theo thời gian
- [x] **B.** Sản phẩm và danh mục
- [x] **C.** Kênh bán hàng
- [ ] **D.** Màu logo công ty
- [x] **E.** Khu vực cửa hàng

> **Tập hợp đáp án đúng:** **A.** Doanh số theo thời gian; **B.** Sản phẩm và danh mục; **C.** Kênh bán hàng; **E.** Khu vực cửa hàng  
> **Giải thích:** Dữ liệu phải có mối liên hệ với câu hỏi; màu logo không phải nguồn trực tiếp để phân rã doanh thu.

---

### Ý 3. Kết quả đầu ra có ý nghĩa nhất
- **Mã ý:** `p04c` | **Thang điểm:** `1 điểm`

- [x] **A.** Một danh sách nguyên nhân có bằng chứng và đề xuất cải thiện
- [ ] **B.** Một bảng dữ liệu thô chưa diễn giải
- [ ] **C.** Một mô hình bất kỳ, không cần đánh giá

> **Đáp án đúng:** **A. Một danh sách nguyên nhân có bằng chứng và đề xuất cải thiện**  
> **Giải thích:** Đầu ra KHDL phải hỗ trợ hành động, có chứng cứ.

---

### Ý 4. Tiêu chí thành công ban đầu phù hợp
- **Mã ý:** `p04d` | **Thang điểm:** `1 điểm`

- [ ] **A.** Đã chạy đủ 1 triệu dòng lệnh
- [x] **B.** Xác định nhóm gây sụt giảm và có giải pháp đo được
- [ ] **C.** Có nhiều màu sắc trên dashboard

> **Đáp án đúng:** **B. Xác định nhóm gây sụt giảm và có giải pháp đo được**  
> **Giải thích:** Đặt chỉ tiêu gắn với phát hiện hữu ích cho quyết định.

---

### Ý 5. Nếu dữ liệu thiếu kênh bán hàng, nên
- **Mã ý:** `p04e` | **Thang điểm:** `1 điểm`

- [ ] **A.** Kết luận ngay kênh nào gây giảm
- [ ] **B.** Bịa thêm cột kênh
- [x] **C.** Ghi rõ hạn chế và bổ sung/đối soát nguồn phù hợp

> **Đáp án đúng:** **C. Ghi rõ hạn chế và bổ sung/đối soát nguồn phù hợp**  
> **Giải thích:** Không suy diễn điều mà dữ liệu không cho phép.

---

## Bài 05. Kiểm tra chất lượng dữ liệu
- **Mã bài:** `p05` | **Cấp độ:** `Trung bình` | **Thang điểm:** `9 điểm` | **Tài liệu:** PDF tr. 12–13

> **Bối cảnh:** Dữ liệu đơn hàng **giả lập**: đơn D01 có hai dòng giống hệt; D02 thiếu doanh thu; D03 có doanh thu −200.000 và được đánh dấu “hoàn tiền”; D04 ghi ngày 31/02/2026; D05 có giá trị “1.200.000” nhưng hệ thống khác dùng dấu chấm thập phân. Chọn cách xử lý thận trọng.  
> 💡 **Gợi ý:** Hãy xác minh nghiệp vụ trước khi loại bỏ thông tin; giá trị âm không phải lúc nào cũng sai.

### Ý 1. D01 trùng hoàn toàn
- **Mã ý:** `p05a` | **Thang điểm:** `2 điểm`

- [x] **A.** Kiểm tra khóa/mã giao dịch, đối soát và gỡ bản ghi trùng hợp lệ
- [ ] **B.** Cộng cả hai như hai đơn mới
- [ ] **C.** Không cần kiểm tra

> **Đáp án đúng:** **A. Kiểm tra khóa/mã giao dịch, đối soát và gỡ bản ghi trùng hợp lệ**  
> **Giải thích:** Cần loại trùng sau khi xác nhận thật sự là bản ghi lặp.

---

### Ý 2. D02 thiếu doanh thu
- **Mã ý:** `p05b` | **Thang điểm:** `2 điểm`

- [ ] **A.** Thay bằng 0 trong mọi tình huống
- [x] **B.** Đối soát hóa đơn gốc, xác định nguyên nhân và quy tắc xử lý
- [ ] **C.** Ước lượng tùy ý

> **Đáp án đúng:** **B. Đối soát hóa đơn gốc, xác định nguyên nhân và quy tắc xử lý**  
> **Giải thích:** Thiếu doanh thu cần đánh giá và xử lý có căn cứ.

---

### Ý 3. D03 doanh thu âm đi kèm cờ hoàn tiền
- **Mã ý:** `p05c` | **Thang điểm:** `2 điểm`

- [ ] **A.** Xóa mọi dòng âm
- [x] **B.** Kiểm tra chính sách hoàn tiền và giữ/biểu diễn đúng nghiệp vụ
- [ ] **C.** Đổi dấu thành dương bất kể tình huống

> **Đáp án đúng:** **B. Kiểm tra chính sách hoàn tiền và giữ/biểu diễn đúng nghiệp vụ**  
> **Giải thích:** Giá trị âm có thể có nghĩa hợp lệ đối với hàng trả, hoàn tiền.

---

### Ý 4. D04 ngày 31/02/2026
- **Mã ý:** `p05d` | **Thang điểm:** `1 điểm`

- [x] **A.** Đối chiếu nguồn gốc vì đây là ngày không hợp lệ
- [ ] **B.** Giữ nguyên không kiểm tra
- [ ] **C.** Chọn một ngày ngẫu nhiên

> **Đáp án đúng:** **A. Đối chiếu nguồn gốc vì đây là ngày không hợp lệ**  
> **Giải thích:** Tháng 2 không có ngày 31; cần đối chiếu.

---

### Ý 5. D05 có dấu chấm ở chuỗi tiền tệ
- **Mã ý:** `p05e` | **Thang điểm:** `1 điểm`

- [x] **A.** Xác nhận quy tắc locale trước khi chuyển thành số
- [ ] **B.** Luôn hiểu thành 1.2
- [ ] **C.** Xóa giao dịch

> **Đáp án đúng:** **A. Xác nhận quy tắc locale trước khi chuyển thành số**  
> **Giải thích:** Cần xác nhận dấu phân tách nghìn và dấu thập phân.

---

### Ý 6. Sau khi làm sạch dữ liệu nên
- **Mã ý:** `p05f` | **Thang điểm:** `1 điểm`

- [x] **A.** Kiểm tra lại tính đầy đủ, chính xác, duy nhất và nhất quán
- [ ] **B.** Không cần kiểm định nữa

> **Đáp án đúng:** **A. Kiểm tra lại tính đầy đủ, chính xác, duy nhất và nhất quán**  
> **Giải thích:** Kiểm định dữ liệu là một công đoạn trong PDF tr. 13.

---

## Bài 06. Tính toán số liệu bán lẻ
- **Mã bài:** `p06` | **Cấp độ:** `Trung bình` | **Thang điểm:** `11 điểm` | **Tài liệu:** PDF tr. 4, 14–15

> **Bối cảnh:** Bộ số liệu **giả lập** (đơn vị doanh thu: triệu VNĐ): tháng 1 = 200, tháng 2 = 240; riêng tháng 2 cửa hàng A = 140, B = 100; tháng 2 có 500 đơn hàng và 1.200 lượt truy cập, trong đó 96 lượt phát sinh mua hàng.  
> 💡 **Gợi ý:** Tăng trưởng % = (mới − cũ) / cũ × 100. Giá trị trung bình đơn = doanh thu / số đơn. Tỷ lệ chuyển đổi = số lượt mua / số lượt truy cập × 100.

### Ý 1. Mức tăng doanh thu tháng 2 so với tháng 1 (triệu VNĐ)
- **Mã ý:** `p06a` | **Thang điểm:** `3 điểm`

> **Đáp án số học:** **`40`**  
> **Hướng dẫn tính:** 240 − 200 = 40 triệu VNĐ.

---

### Ý 2. Tỷ lệ tăng doanh thu (%)
- **Mã ý:** `p06b` | **Thang điểm:** `2 điểm`

> **Đáp án số học:** **`20`**  
> **Hướng dẫn tính:** (240 − 200) / 200 × 100 = 20%.

---

### Ý 3. Doanh thu cửa hàng A chiếm bao nhiêu % doanh thu tháng 2?
- **Mã ý:** `p06c` | **Thang điểm:** `2 điểm`

> **Đáp án số học:** **`58,333333`**  
> **Hướng dẫn tính:** 140 / 240 × 100 = 58,33%.

---

### Ý 4. Giá trị trung bình một đơn tháng 2 (nghìn VNĐ)
- **Mã ý:** `p06d` | **Thang điểm:** `2 điểm`

> **Đáp án số học:** **`480`**  
> **Hướng dẫn tính:** 240.000 nghìn / 500 = 480 nghìn VNĐ/đơn.

---

### Ý 5. Tỷ lệ chuyển đổi lượt truy cập → mua hàng (%)
- **Mã ý:** `p06e` | **Thang điểm:** `2 điểm`

> **Đáp án số học:** **`8`**  
> **Hướng dẫn tính:** 96 / 1.200 × 100 = 8%.

---

## Bài 07. Phân biệt bốn loại phân tích
- **Mã bài:** `p07` | **Cấp độ:** `Cơ bản` | **Thang điểm:** `6 điểm` | **Tài liệu:** PDF tr. 14

> **Bối cảnh:** Mỗi câu hỏi sau thuộc loại phân tích nào?  
> 💡 **Gợi ý:** Mô tả = chuyện đã xảy ra; Chẩn đoán = tìm nguyên nhân; Dự báo = tương lai; Đề xuất = nên làm gì.

### Ý 1. Doanh thu theo từng quý năm trước là bao nhiêu?
- **Mã ý:** `p07a` | **Thang điểm:** `1 điểm`

- [x] **A.** Mô tả
- [ ] **B.** Chẩn đoán
- [ ] **C.** Dự báo
- [ ] **D.** Đề xuất

> **Đáp án đúng:** **A. Mô tả**  
> **Giải thích:** Thống kê quá khứ → mô tả.

---

### Ý 2. Vì sao số đơn tại cửa hàng A giảm 25%?
- **Mã ý:** `p07b` | **Thang điểm:** `1 điểm`

- [ ] **A.** Mô tả
- [x] **B.** Chẩn đoán
- [ ] **C.** Dự báo
- [ ] **D.** Đề xuất

> **Đáp án đúng:** **B. Chẩn đoán**  
> **Giải thích:** Giải thích nguyên nhân → chẩn đoán.

---

### Ý 3. Tháng tới số đơn hàng có thể đạt bao nhiêu?
- **Mã ý:** `p07c` | **Thang điểm:** `1 điểm`

- [ ] **A.** Mô tả
- [ ] **B.** Chẩn đoán
- [x] **C.** Dự báo
- [ ] **D.** Đề xuất

> **Đáp án đúng:** **C. Dự báo**  
> **Giải thích:** Ước lượng tương lai → dự báo.

---

### Ý 4. Cần đặt mức tồn kho nào để giảm tổng chi phí?
- **Mã ý:** `p07d` | **Thang điểm:** `1 điểm`

- [ ] **A.** Mô tả
- [ ] **B.** Chẩn đoán
- [ ] **C.** Dự báo
- [x] **D.** Đề xuất

> **Đáp án đúng:** **D. Đề xuất**  
> **Giải thích:** Lựa chọn hành động → đề xuất/tối ưu.

---

### Ý 5. Tỷ lệ rời bỏ tháng vừa rồi của khách hàng là bao nhiêu?
- **Mã ý:** `p07e` | **Thang điểm:** `1 điểm`

- [x] **A.** Mô tả
- [ ] **B.** Chẩn đoán
- [ ] **C.** Dự báo
- [ ] **D.** Đề xuất

> **Đáp án đúng:** **A. Mô tả**  
> **Giải thích:** Đo lường hiện trạng vừa qua → mô tả.

---

### Ý 6. Kênh quảng cáo nào nên được tăng ngân sách với mức lợi nhuận dự kiến cao nhất?
- **Mã ý:** `p07f` | **Thang điểm:** `1 điểm`

- [ ] **A.** Mô tả
- [ ] **B.** Chẩn đoán
- [ ] **C.** Dự báo
- [x] **D.** Đề xuất

> **Đáp án đúng:** **D. Đề xuất**  
> **Giải thích:** Chọn phương án hành động tối ưu → đề xuất.

---

## Bài 08. Chọn biểu đồ đúng mục tiêu
- **Mã bài:** `p08` | **Cấp độ:** `Cơ bản` | **Thang điểm:** `6 điểm` | **Tài liệu:** PDF tr. 15

> **Bối cảnh:** Mỗi tình huống ưu tiên một dạng biểu đồ trong danh sách sau.  
> 💡 **Gợi ý:** Hãy dựa vào cấu trúc dữ liệu: thời gian, nhóm, hai biến số, một phân phối hay nhiều KPI.

### Ý 1. Diễn biến doanh thu theo 12 tháng
- **Mã ý:** `p08a` | **Thang điểm:** `1 điểm`

- [x] **A.** Biểu đồ đường
- [ ] **B.** Biểu đồ cột
- [ ] **C.** Scatter plot
- [ ] **D.** Histogram
- [ ] **E.** Boxplot
- [ ] **F.** Dashboard

> **Đáp án đúng:** **A. Biểu đồ đường**  
> **Giải thích:** Biểu đồ đường cho xu hướng theo thời gian.

---

### Ý 2. So sánh doanh thu giữa năm vùng
- **Mã ý:** `p08b` | **Thang điểm:** `1 điểm`

- [ ] **A.** Biểu đồ đường
- [x] **B.** Biểu đồ cột
- [ ] **C.** Scatter plot
- [ ] **D.** Histogram
- [ ] **E.** Boxplot
- [ ] **F.** Dashboard

> **Đáp án đúng:** **B. Biểu đồ cột**  
> **Giải thích:** Biểu đồ cột so sánh các nhóm.

---

### Ý 3. Mối liên hệ giữa giá sản phẩm và lượng bán
- **Mã ý:** `p08c` | **Thang điểm:** `1 điểm`

- [ ] **A.** Biểu đồ đường
- [ ] **B.** Biểu đồ cột
- [x] **C.** Scatter plot
- [ ] **D.** Histogram
- [ ] **E.** Boxplot
- [ ] **F.** Dashboard

> **Đáp án đúng:** **C. Scatter plot**  
> **Giải thích:** Scatter plot thể hiện mối quan hệ hai đại lượng.

---

### Ý 4. Phân phối giá trị của 1.000 đơn hàng
- **Mã ý:** `p08d` | **Thang điểm:** `1 điểm`

- [ ] **A.** Biểu đồ đường
- [ ] **B.** Biểu đồ cột
- [ ] **C.** Scatter plot
- [x] **D.** Histogram
- [ ] **E.** Boxplot
- [ ] **F.** Dashboard

> **Đáp án đúng:** **D. Histogram**  
> **Giải thích:** Histogram thể hiện phân phối tần suất.

---

### Ý 5. So sánh trung vị và ngoại lệ thu nhập của các nhóm nhân viên
- **Mã ý:** `p08e` | **Thang điểm:** `1 điểm`

- [ ] **A.** Biểu đồ đường
- [ ] **B.** Biểu đồ cột
- [ ] **C.** Scatter plot
- [ ] **D.** Histogram
- [x] **E.** Boxplot
- [ ] **F.** Dashboard

> **Đáp án đúng:** **E. Boxplot**  
> **Giải thích:** Boxplot cho trung vị, tứ phân vị và ngoại lệ.

---

### Ý 6. Một trang tổng hợp doanh thu, đơn hàng và tồn kho
- **Mã ý:** `p08f` | **Thang điểm:** `1 điểm`

- [ ] **A.** Biểu đồ đường
- [ ] **B.** Biểu đồ cột
- [ ] **C.** Scatter plot
- [ ] **D.** Histogram
- [ ] **E.** Boxplot
- [x] **F.** Dashboard

> **Đáp án đúng:** **F. Dashboard**  
> **Giải thích:** Dashboard cho nhiều KPI đồng thời.

---

## Bài 09. Bài toán chiến dịch ngân hàng (tính kỳ vọng)
- **Mã bài:** `p09` | **Cấp độ:** `Nâng cao` | **Thang điểm:** `14 điểm` | **Tài liệu:** PDF tr. 16 – mở rộng bằng dữ liệu giả lập

> **Bối cảnh:** Một ngân hàng có 3 nhóm khách hàng. Khi liên hệ, mỗi chuyển đổi thành công tạo **200.000 VNĐ** giá trị kinh tế, chi phí liên hệ **20.000 VNĐ/khách**. Xác suất chuyển đổi nhóm A = 30% (120 KH), nhóm B = 10% (200 KH), nhóm C = 45% (80 KH). Giới hạn có thể liên hệ tối đa 100 khách, nhóm nào cũng có thể liên hệ một phần. Giả định các xác suất/chi phí cố định, không có ràng buộc khác.  
> 💡 **Gợi ý:** Lợi ích kỳ vọng mỗi lần liên hệ = p × 200.000 − 20.000. Ưu tiên nhóm có lợi ích kỳ vọng lớn nhất trước.

### Ý 1. Lợi ích kỳ vọng/1 khách nhóm A (VNĐ)
- **Mã ý:** `p09a` | **Thang điểm:** `3 điểm`

> **Đáp án số học:** **`40000`**  
> **Hướng dẫn tính:** 0,30 × 200.000 − 20.000 = 40.000 VNĐ.

---

### Ý 2. Lợi ích kỳ vọng/1 khách nhóm B (VNĐ)
- **Mã ý:** `p09b` | **Thang điểm:** `3 điểm`

> **Đáp án số học:** **`0`**  
> **Hướng dẫn tính:** 0,10 × 200.000 − 20.000 = 0 VNĐ.

---

### Ý 3. Lợi ích kỳ vọng/1 khách nhóm C (VNĐ)
- **Mã ý:** `p09c` | **Thang điểm:** `3 điểm`

> **Đáp án số học:** **`70000`**  
> **Hướng dẫn tính:** 0,45 × 200.000 − 20.000 = 70.000 VNĐ.

---

### Ý 4. Nhóm được ưu tiên liên hệ trước
- **Mã ý:** `p09d` | **Thang điểm:** `2 điểm`

- [ ] **A.** A
- [ ] **B.** B
- [x] **C.** C

> **Đáp án đúng:** **C. C**  
> **Giải thích:** C có lợi ích kỳ vọng/khách cao nhất (70.000 VNĐ).

---

### Ý 5. Nếu liên hệ 80 KH nhóm C và 20 KH nhóm A, tổng lợi ích kỳ vọng (triệu VNĐ)
- **Mã ý:** `p09e` | **Thang điểm:** `3 điểm`

> **Đáp án số học:** **`6,4`**  
> **Hướng dẫn tính:** 80 × 70.000 + 20 × 40.000 = 6.400.000 VNĐ = 6,4 triệu VNĐ.

---

## Bài 10. Đánh giá tình huống ngân hàng
- **Mã bài:** `p10` | **Cấp độ:** `Trung bình` | **Thang điểm:** `9 điểm` | **Tài liệu:** PDF tr. 16

> **Bối cảnh:** Trả lời các câu hỏi dựa trên tình huống lựa chọn người nhận lời mời gửi tiết kiệm của bài giảng.  
> 💡 **Gợi ý:** Nên mô tả đúng quyết định, dữ liệu dự đoán, đầu ra và KPI kinh tế; không lấy dữ liệu tương lai để dự đoán quá khứ.

### Ý 1. Biến kết quả mô hình có thể dự báo
- **Mã ý:** `p10a` | **Thang điểm:** `2 điểm`

- [x] **A.** Khách hàng có phản hồi/đồng ý gửi tiết kiệm không
- [ ] **B.** ID khách hàng của ngân hàng
- [ ] **C.** Màu ứng dụng

> **Đáp án đúng:** **A. Khách hàng có phản hồi/đồng ý gửi tiết kiệm không**  
> **Giải thích:** Mục tiêu là khả năng khách hàng chấp nhận đề nghị gửi tiết kiệm.

---

### Ý 2. Chọn dữ liệu đầu vào phù hợp khi có quyền và cơ sở sử dụng hợp lệ
- **Mã ý:** `p10b` | **Thang điểm:** `3 điểm`

- [x] **A.** Lịch sử giao dịch trước chiến dịch
- [x] **B.** Thu nhập/số dư trước chiến dịch
- [x] **C.** Kênh liên hệ
- [ ] **D.** Kết quả cuối cùng của chính chiến dịch đang dự đoán

> **Tập hợp đáp án đúng:** **A.** Lịch sử giao dịch trước chiến dịch; **B.** Thu nhập/số dư trước chiến dịch; **C.** Kênh liên hệ  
> **Giải thích:** Không dùng kết quả tương lai của chiến dịch như một biến dự báo khi ra quyết định trước chiến dịch.

---

### Ý 3. Đầu ra phục vụ người quản lý
- **Mã ý:** `p10c` | **Thang điểm:** `2 điểm`

- [x] **A.** Danh sách KH ưu tiên liên hệ và kênh khuyến nghị
- [ ] **B.** Chỉ bộ trọng số mô hình
- [ ] **C.** Một file chứa cột không có giải thích

> **Đáp án đúng:** **A. Danh sách KH ưu tiên liên hệ và kênh khuyến nghị**  
> **Giải thích:** Ưu tiên danh sách có thể hành động.

---

### Ý 4. Một KPI có ý nghĩa kinh doanh
- **Mã ý:** `p10d` | **Thang điểm:** `1 điểm`

- [x] **A.** Chi phí trên mỗi khách hàng chuyển đổi
- [ ] **B.** Số dòng code
- [ ] **C.** Số biến trước khi xử lý

> **Đáp án đúng:** **A. Chi phí trên mỗi khách hàng chuyển đổi**  
> **Giải thích:** KPI kinh tế nằm trong ví dụ của bài giảng.

---

### Ý 5. Khi dự báo tốt trên tập huấn luyện nhưng tệ trên dữ liệu mới
- **Mã ý:** `p10e` | **Thang điểm:** `1 điểm`

- [ ] **A.** Triển khai ngay vì điểm train tốt
- [x] **B.** Đánh giá sai lệch, làm lại mô hình/đặc trưng trước triển khai
- [ ] **C.** Không cần ghi nhận

> **Đáp án đúng:** **B. Đánh giá sai lệch, làm lại mô hình/đặc trưng trước triển khai**  
> **Giải thích:** Kết quả phải được đánh giá trên dữ liệu phù hợp trước khi sử dụng.

---

## Bài 11. Diễn giải kết quả và hạn chế
- **Mã bài:** `p11` | **Cấp độ:** `Trung bình` | **Thang điểm:** `8 điểm` | **Tài liệu:** PDF tr. 7, 12–16

> **Bối cảnh:** Lựa chọn kết luận và hành động có cơ sở từ dữ liệu. Các ví dụ được bổ sung để làm rõ giới hạn suy luận.  
> 💡 **Gợi ý:** Phân tích kinh doanh phải minh bạch về nguồn, đơn vị, thiên lệch và giới hạn; tương quan không tự khẳng định quan hệ nhân quả.

### Ý 1. Chi tiêu quảng cáo và doanh thu có tương quan dương. Kết luận nào đúng?
- **Mã ý:** `p11a` | **Thang điểm:** `2 điểm`

- [ ] **A.** Quảng cáo chắc chắn là nguyên nhân duy nhất làm tăng doanh thu
- [x] **B.** Có mối liên hệ; cần thiết kế phân tích bổ sung để đánh giá tác động nhân quả

> **Đáp án đúng:** **B. Có mối liên hệ; cần thiết kế phân tích bổ sung để đánh giá tác động nhân quả**  
> **Giải thích:** Tương quan không đủ để kết luận nhân quả.

---

### Ý 2. Một tập dữ liệu chỉ gồm khách mua online. Có nên kết luận cho toàn bộ khách?
- **Mã ý:** `p11b` | **Thang điểm:** `2 điểm`

- [x] **A.** Chưa thể, vì mẫu có thể không đại diện
- [ ] **B.** Có, vì dữ liệu đã ở dạng bảng

> **Đáp án đúng:** **A. Chưa thể, vì mẫu có thể không đại diện**  
> **Giải thích:** Thiên lệch chọn mẫu làm hạn chế khả năng khái quát.

---

### Ý 3. Khi báo cáo cho trưởng bộ phận bán hàng, nên ưu tiên
- **Mã ý:** `p11c` | **Thang điểm:** `2 điểm`

- [x] **A.** Kết luận chính, tác động kinh doanh, đề xuất và giới hạn
- [ ] **B.** Toàn bộ mã nguồn trên trang đầu

> **Đáp án đúng:** **A. Kết luận chính, tác động kinh doanh, đề xuất và giới hạn**  
> **Giải thích:** Thông tin phục vụ quyết định cần được trình bày đúng đối tượng.

---

### Ý 4. Mô hình tốt có cần giám sát sau khi triển khai?
- **Mã ý:** `p11d` | **Thang điểm:** `1 điểm`

- [x] **A.** Có, vì dữ liệu và hành vi có thể thay đổi
- [ ] **B.** Không, độ chính xác không bao giờ đổi

> **Đáp án đúng:** **A. Có, vì dữ liệu và hành vi có thể thay đổi**  
> **Giải thích:** Giám sát/bảo trì thuộc giai đoạn Deployment.

---

### Ý 5. Trước khi dùng dữ liệu khách hàng cá nhân, nên
- **Mã ý:** `p11e` | **Thang điểm:** `1 điểm`

- [x] **A.** Xác minh quyền sử dụng, mục đích, bảo mật và mức cần thiết
- [ ] **B.** Thu thập tất cả dữ liệu không cần hỏi

> **Đáp án đúng:** **A. Xác minh quyền sử dụng, mục đích, bảo mật và mức cần thiết**  
> **Giải thích:** Quản trị dữ liệu có trách nhiệm là phần mở rộng quan trọng trong thực tế.

---

## Bài 12. Dự án tổng hợp: giảm tồn kho thiếu hụt
- **Mã bài:** `p12` | **Cấp độ:** `Vận dụng` | **Thang điểm:** `12 điểm` | **Tài liệu:** PDF tr. 4, 8–16

> **Bối cảnh:** Chuỗi bán lẻ thường xuyên thiếu một số sản phẩm nhưng lại tồn kho quá nhiều sản phẩm khác. Hãy lựa chọn các bước hợp lý khi bắt đầu một dự án khoa học dữ liệu.  
> 💡 **Gợi ý:** Gắn mỗi bước với quyết định thực tế, nguồn dữ liệu có thể thu thập và chỉ số hiệu quả.

### Ý 1. Quyết định kinh doanh cuối cùng
- **Mã ý:** `p12a` | **Thang điểm:** `2 điểm`

- [ ] **A.** Chọn một thuật toán ngẫu nhiên
- [x] **B.** Mức đặt hàng/tồn kho hợp lý theo mặt hàng và cửa hàng
- [ ] **C.** Chọn màu biểu đồ

> **Đáp án đúng:** **B. Mức đặt hàng/tồn kho hợp lý theo mặt hàng và cửa hàng**  
> **Giải thích:** Bài toán kinh doanh là quyết định tồn kho, mô hình chỉ hỗ trợ.

---

### Ý 2. Dữ liệu cần thiết
- **Mã ý:** `p12b` | **Thang điểm:** `4 điểm`

- [x] **A.** Lịch sử bán hàng
- [x] **B.** Mức tồn kho
- [x] **C.** Thời gian giao hàng
- [ ] **D.** Màu áo đồng phục

> **Tập hợp đáp án đúng:** **A.** Lịch sử bán hàng; **B.** Mức tồn kho; **C.** Thời gian giao hàng  
> **Giải thích:** Lịch sử nhu cầu, tồn kho và lead time có ích cho quyết định nhập hàng.

---

### Ý 3. Một đầu ra mô hình dữ liệu phù hợp
- **Mã ý:** `p12c` | **Thang điểm:** `2 điểm`

- [x] **A.** Dự báo nhu cầu theo sản phẩm/cửa hàng
- [ ] **B.** Tên miền website
- [ ] **C.** Bộ biểu tượng thương hiệu

> **Đáp án đúng:** **A. Dự báo nhu cầu theo sản phẩm/cửa hàng**  
> **Giải thích:** Dự báo nhu cầu là đầu vào hợp lý cho bài toán quyết định.

---

### Ý 4. Hướng phân tích phục vụ chọn mức tồn kho
- **Mã ý:** `p12d` | **Thang điểm:** `2 điểm`

- [x] **A.** Prescriptive Analytics (phân tích đề xuất)
- [ ] **B.** Chỉ phân tích mô tả
- [ ] **C.** Phát triển phần cứng

> **Đáp án đúng:** **A. Prescriptive Analytics (phân tích đề xuất)**  
> **Giải thích:** Cần chọn phương án/mức tồn kho đáp ứng mục tiêu.

---

### Ý 5. Chỉ số đánh giá vận hành phù hợp
- **Mã ý:** `p12e` | **Thang điểm:** `2 điểm`

- [x] **A.** Tỷ lệ thiếu hàng và chi phí tồn kho
- [ ] **B.** Số biểu đồ đã vẽ
- [ ] **C.** Số tên biến trong file

> **Đáp án đúng:** **A. Tỷ lệ thiếu hàng và chi phí tồn kho**  
> **Giải thích:** Đánh giá phải gắn với chi phí và hiệu quả phục vụ khách.

---
