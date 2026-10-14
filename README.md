# Day26 Track01 - VinTay

## Thông tin nộp bài

| Mục | Thông tin |
|---|---|
| Tên repo | `Day26_Track01_VinTay` |
| Link repo | https://github.com/minhdh329/Day26_Track01_VinTay |
| Nhánh | `main` |
| Quyền truy cập | Public; trang GitHub mở được khi chưa đăng nhập |
| Hạn nộp | Cuối buổi, phút 120 |
| Nơi nộp | Dán link repo trên vào Vlearn; mỗi thành viên dùng cùng một link trên tài khoản Vlearn của mình |
| Trạng thái | Chưa nộp: GitHub hiện báo repo trống; các file trong workspace chưa được commit/push |

Trước khi nộp, commit và push đủ file lên nhánh `main`, rồi mở link ở cửa sổ ẩn danh để xác nhận người chấm xem được nội dung.

## 1. Thành viên

| Họ tên | MSSV | Phần phụ trách | Góp ý đã đưa cho nhóm bạn |
|---|---|---|---|
| Dương Hải Minh | 2A202602680S | Chốt phạm vi và AS-IS/TO-BE; phụ trách Gartner-Lite, readiness và tổng hợp bằng chứng cho nguyên nhân gốc. | Mô phỏng, Nhóm 05: “Số login/số câu hỏi là activity; hãy định nghĩa tỷ lệ câu trả lời có nguồn và mẫu số QA.” |
| Đỗ Trương Thành Ân | 2A202602899 | Phụ trách Mollick, ADKAR, phân công người-AI; xây dashboard, lộ trình 30-60-90 và memo quyết định. | Mô phỏng, Nhóm 08: “Tách thời gian theo từng workflow và ghi rõ owner, ngưỡng qua cổng cùng hành động nếu metric xấu.” |

Hai thành viên cùng chốt nguyên nhân, rà logic và thống nhất quyết định. Case, số liệu và hai góp ý trên đều là **mô phỏng theo yêu cầu**, không phải quan sát/phản biện đã diễn ra; thay bằng dữ liệu thật nếu lớp yêu cầu.

## 2. Phạm vi

**Case mô phỏng:** trợ lý AI tra cứu tài liệu nội bộ cho nhân viên vận hành; 3 workflow là tra cứu chính sách, tổng hợp tài liệu yêu cầu và kiểm phiên bản/chuyển cấp ngoại lệ.

## 3. Nguyên nhân gốc

Hai giả thuyết: thiếu nguồn/ngày cập nhật và owner chất lượng; AI chưa nằm trong workflow có bàn giao. Gartner-Lite rà readiness, Mollick phân chia việc, ADKAR chẩn đoán điểm nghẽn người dùng; **bằng chứng mô phỏng:** 18/30 câu có nguồn/ngày hiện hành, 7 thiếu nguồn, 5 nguồn cũ; 3/4 người phỏng vấn lo ngại về nguồn, 2/4 chưa biết báo lỗi.

## 4. Cách làm mới và lộ trình

**AS-IS -> TO-BE:** tìm file/hỏi đồng nghiệp -> hỏi AI, mở nguồn/ngày, người kiểm chứng, dùng hoặc báo lỗi; bổ sung source, owner và QA/escalation. **Lộ trình mô phỏng:** 0–30 ngày đo baseline/chốt nguồn (Minh); 31–60 pilot và QA (Ân); 61–90 quyết định mở rộng/sửa/dừng (cả hai), chỉ qua cổng khi đạt ngưỡng.

## 5. Chỉ số

- **Product:** tỷ lệ câu trả lời có nguồn/ngày cập nhật; baseline mô phỏng 60% (18/30), target >=90% (>=27/30) ngày 60, log + QA mẫu, owner Đỗ Trương Thành Ân.
- **Workflow:** trung vị mô phỏng 18/32/14 phút cho ba workflow (n=10 mỗi workflow); target giảm >=20% từng workflow ngày 60, task log, owner Dương Hải Minh; adoption 16/30 (53%) -> >=70%, guardrail rework 12/30 (40%) -> <=10%. Đây là dữ liệu giả lập, không phải số đo thực tế.

## 6. Quyết định

**Quyết định mô phỏng: SỬA, giữ pilot nhỏ; chưa rollout rộng** vì độ tin cậy/readiness thấp. Hai phản biện mô phỏng dẫn tới thay đổi: (1) định nghĩa mẫu số QA và chỉ số nguồn; (2) tách thời gian theo 3 workflow, thêm owner/ngưỡng/hành động; thay bằng phản biện thật nếu lớp yêu cầu bằng chứng chặng 3.

## 7. Kiểm tra kết quả

### Hai checkpoint

| Mốc | Pass khi | Trạng thái bản nháp |
|---|---|---|
| Phút 40: phạm vi và chẩn đoán | Nêu rõ sản phẩm, nhóm người dùng, 2–4 workflow; chốt 1–2 nguyên nhân gốc, mỗi nguyên nhân có framework phù hợp và bằng chứng. | **Đạt theo mô phỏng:** có case, mẫu QA và phỏng vấn giả lập; không phải bằng chứng thực tế. |
| Phút 80: logic chỉ số | Có ít nhất một product metric và một workflow metric; mỗi chỉ số có baseline, target, nguồn, owner và hành động khi xấu. | **Đạt theo mô phỏng:** đã có baseline/target/owner giả định; cần thay bằng dữ liệu thật nếu rubric yêu cầu. |

### Năm dấu hiệu bài đạt

1. Phạm vi cụ thể, không kết luận chung về “AI trong công ty”.
2. Dùng framework đúng việc: Gartner-Lite cho readiness, Mollick cho phân chia việc, ADKAR cho điểm nghẽn ở người dùng.
3. Đo cả workflow/chất lượng/giá trị, không chỉ login hoặc số câu hỏi.
4. Mỗi metric chỉ rõ nguồn dữ liệu, owner và hành động khi kết quả xấu.
5. Có quyết định rõ: tiếp tục, sửa hoặc dừng.

### Lỗi thường gặp và cách sửa

| Lỗi | Cách sửa |
|---|---|
| Gọi “ít người dùng” là nguyên nhân gốc | Hỏi tiếp vì sao; kiểm tra độ tin cậy và workflow. |
| Mặc định giải quyết bằng đào tạo | Dùng ADKAR để tìm đúng điểm nghẽn; xử lý dữ liệu, quyền hoặc hỗ trợ tại workflow nếu đó mới là nguyên nhân. |
| Đo activity thay vì giá trị | Bổ sung thời gian từ log, tỷ lệ không phải làm lại, chất lượng và kết quả theo workflow. |
| Metric không dẫn đến hành động | Điền rõ việc cần làm, người làm và điều kiện xem xét lại cho từng chỉ số xấu. |
| Phạm vi quá rộng | Chốt một sản phẩm, một nhóm người dùng và 2–4 workflow. |
| Chỉ thêm AI mà không đổi cách chia việc | Dùng Mollick để nêu rõ AI làm gì, người kiểm chứng/quyết định là ai và ai chịu trách nhiệm. |
| Lộ trình chỉ là danh sách việc | Biến mỗi mốc thành cổng có owner và dấu hiệu hoàn thành. |
| Chẩn đoán không có bằng chứng | Bổ sung ít nhất một quan sát, log, phỏng vấn ngắn hoặc case tham khảo phù hợp. |

### Tự kiểm trước khi kết thúc

- [ ] AI đi vào workflow nào?
- [ ] Nguyên nhân gốc nằm ở đâu và bằng chứng là gì?
- [ ] Framework nào giúp trả lời từng nguyên nhân?
- [ ] Metric nào chứng minh chất lượng/giá trị, và lấy dữ liệu từ đâu?
- [ ] Điều kiện nào khiến nhóm tiếp tục, sửa hoặc dừng?
