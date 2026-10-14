# Memo quyết định: Trợ lý AI tra cứu tài liệu nội bộ

> Case, số liệu và phản biện trong memo này đều là **mô phỏng theo yêu cầu**, không phải quan sát hoặc phản biện đã diễn ra. Thay bằng dữ liệu thực nếu rubric yêu cầu bằng chứng thật.

## 1. Vấn đề và nguyên nhân gốc

Trong doanh nghiệp dịch vụ giả định, nhân viên vận hành dùng trợ lý AI để tra cứu chính sách, tổng hợp tài liệu yêu cầu và kiểm phiên bản/chuyển cấp ngoại lệ, nhưng thường quay lại tìm file thủ công. Hai nguyên nhân mô phỏng: (1) câu trả lời thiếu nguồn/ngày mới và chưa có owner chất lượng; (2) AI nằm ngoài workflow chính, thiếu bàn giao và đường xử lý lỗi.

## 2. Framework và bằng chứng mô phỏng

- **Gartner-Lite:** hướng đi là giảm thời gian tra cứu; readiness/absorption yếu vì data owner, lịch cập nhật và quyền truy cập chưa rõ.
- **Mollick:** AI tìm/tóm tắt; nhân viên kiểm nguồn, quyết định và chịu trách nhiệm. **ADKAR:** thiếu nguồn làm giảm Desire; thiếu hướng dẫn ngay tại workflow ảnh hưởng Knowledge/Ability.
- QA giả lập 30 câu: 18 câu có nguồn hiện hành (60%), 7 thiếu nguồn, 5 dùng nguồn cũ. Phỏng vấn giả lập 4 người: 3 lo ngại nguồn/ngày cập nhật, 2 chưa biết cách báo lỗi.
- Log tác vụ giả lập: 10 lượt mỗi workflow; median lần lượt 18 phút (tra cứu chính sách), 32 phút (tổng hợp tài liệu), 14 phút (kiểm phiên bản/chuyển cấp). 16/30 lượt bắt đầu bằng AI.

## 3. Phản biện và thay đổi mô phỏng

1. **Nhóm 05 (giả lập):** yêu cầu định nghĩa rõ tỷ lệ câu trả lời có nguồn và mẫu số QA. **Thay đổi:** metric product là 18/30 = 60%, target >=27/30 = 90%.
2. **Nhóm 08 (giả lập):** nhận xét median chung che khuất điểm nghẽn mỗi workflow. **Thay đổi:** tách ba median, gắn owner và đặt target giảm >=20% cho từng workflow.

Đây là phản biện dựng để minh họa quy trình; không được ghi là góp ý thực tế đã nhận.

## 4. Quyết định

**SỬA, tiếp tục pilot nhỏ; chưa rollout rộng.** Chỉ xem xét mở rộng khi tỷ lệ câu trả lời có nguồn hiện hành đạt >=90%, median từng workflow giảm >=20%, rework <=10% và có owner/quyền truy cập rõ.

## 5. Lý do, bước tiếp theo và owner

Baseline mô phỏng: product 60%; thời gian workflow 18/32/14 phút; adoption 16/30 = 53%; rework 12/30 = 40%. Target đề xuất: product >=90%, mỗi workflow giảm >=20%, adoption >=70% sau khi qua cổng chất lượng, rework <=10%.

0–30 ngày: Dương Hải Minh (chủ workflow mô phỏng) chốt AS-IS/TO-BE, owner dữ liệu và quyền nguồn. 31–60 ngày: Đỗ Trương Thành Ân (QA/data owner mô phỏng) kiểm 30 câu, bật trích dẫn/ngày và theo dõi log. 61–90 ngày: cả hai so target, rồi quyết định mở rộng/sửa/dừng. Tên vai trò và mọi chỉ số ở đây là giả định.
