# BÁO CÁO BÀI TẬP: LẬP KẾ HOẠCH SPRINT CHO HỆ THỐNG ĐẶT LỊCH SẠC XE MÁY ĐIỆN

> 👤 **Học viên:** Đỗ Hoàng Sơn | **Mã SV:** PTIT-HCM-066
> 🏫 **Môn học:** IT206-K25-Agile-va-Scrum

---

## Nhiệm vụ 1: Phân tích Velocity và Capacity

Dưới đây là bảng Velocity tham khảo từ 3 Sprint trước và bảng tính Capacity chi tiết cho Sprint hiện tại của nhóm Phát triển RikkeiCharge.

| Sprint | SP hoàn thành (Done) | Ghi chú |
| --- | --- | --- |
| Sprint -3 | 15 | Đủ thành viên |
| Sprint -2 | 16 | Đủ thành viên |
| Sprint -1 | 17 | Đủ thành viên |
| Velocity tham khảo | 16 SP | Tính trung bình cộng (15 + 16 + 17) / 3 để dùng làm mức dự báo cơ sở cho Sprint mới. |

## Bảng Capacity chi tiết của Sprint

Sprint kéo dài 10 ngày, gồm 4 Developers với thời gian tập trung 5 giờ/ngày. Dev C nghỉ 2 ngày trong Sprint.

| Developers | Ngày Sprint | Ngày không tham gia | Ngày khả dụng | Giờ tập trung/ngày | Capacity (giờ) |
| --- | --- | --- | --- | --- | --- |
| Dev A | 10 | 0 | 10 | 5 | 50 |
| Dev B | 10 | 0 | 10 | 5 | 50 |
| Dev C | 10 | 2 | 8 | 5 | 40 |
| Dev D | 10 | 0 | 10 | 5 | 50 |
| Tổng | 40 | 2 | 38 | 20 | 190 giờ |

## Nhận xét Capacity và Velocity

Nhận xét: Capacity của Sprint này là 190 giờ, thấp hơn mức tối đa 200 giờ do Dev C nghỉ 2 ngày. Ta dùng Velocity trung bình (16 SP) để dự báo khả năng hoàn thành số lượng Product Backlog Item, kết hợp với Capacity (190 giờ) để kiểm tra xem khối lượng công việc chọn vào Sprint có vượt quá tổng số giờ làm việc thực tế của Developers hay không.

## Nhiệm vụ 2: Viết lại Sprint Goal

Sprint Goal đã chỉnh sửa: Người dùng có thể dễ dàng tìm kiếm trạm sạc, xem khung giờ trống chính xác và thực hiện đặt chỗ trước để an tâm đến sạc xe mà không phải chờ đợi.

## Nhiệm vụ 3: Lập Sprint Backlog

Dựa trên Velocity dự báo là 16 SP và Capacity 190 giờ, nhóm tiến hành đánh giá và chọn lựa các PBI đưa vào Sprint Backlog như sau:

| Mã Story | Ưu tiên | SP | Chọn/Chưa chọn | Lý do |
| --- | --- | --- | --- | --- |
| CS01 | 1 | 3 | Chọn | Ưu tiên 1; bước đầu để người dùng tìm trạm. |
| CS02 | 2 | 3 | Chọn | Ưu tiên 2; cần biết giờ còn trống trước khi đặt. |
| CS03 | 3 | 5 | Chọn | Ưu tiên 3; tính năng cốt lõi cho phép người dùng đặt trước vị trí sạc. |
| CS04 | 4 | 5 | Chưa chọn | Chưa chốt quy tắc nghiệp vụ hủy sát giờ sạc, cần Product Owner làm rõ thêm trước khi đưa vào phát triển. |
| Tổng SP đã chọn |  | 11 SP |  | Mức dự báo, không phải cam kết. |

## Task Breakdown cho CS03

User Story CS03 được chia nhỏ thành các Task kỹ thuật để các Developer nhận việc và triển khai:

| STT | Task | Đầu ra | Ước lượng (giờ) |
| --- | --- | --- | --- |
| 1 | Thiết kế API và giao diện chọn trạm, chọn giờ và xe cần sạc cho CS03 | API endpoint hoàn chỉnh và màn hình Frontend tương ứng | 12 |
| 2 | Xây dựng logic kiểm tra trùng lịch và sinh mã xác nhận đặt chỗ | Hệ thống chặn trùng lịch và trả về mã xác nhận hợp lệ | 16 |

## Nhiệm vụ 4: Phân tích Burndown Chart

1. So sánh đường thực tế với đường lý tưởng. Chỉ ra dấu hiệu bất thường giữa Sprint và rủi ro cho Sprint Goal:

Từ ngày 0 đến ngày 7, đường thực tế đi ngang ở mức 11 SP trong khi đường lý tưởng giảm đều đặn, cho thấy nhóm chưa hoàn thành xong PBI nào (vì quy tắc là PBI chỉ được trừ SP khi đã Done). Đến ngày 8, đường thực tế giảm xuống 5 SP (tương ứng CS01 và CS02 hoàn thành). Dấu hiệu bất thường này phản ánh tình trạng dồn việc vào cuối Sprint, tạo rủi ro lớn là không kịp hoàn thành nốt CS03 trước khi Sprint kết thúc, đe dọa trực tiếp đến Sprint Goal.

2. Giả sử nhóm đang ở Daily Scrum ngày 7: đề xuất 1 hành động giúp đạt Sprint Goal:

Nhóm cần tập trung toàn lực hỗ trợ các Developer đang làm dở các Task của CS03, đồng thời chủ động trao đổi ngay với Product Owner để gác lại hoặc tách bớt các yêu cầu phụ chưa thực sự bắt buộc nhằm đảm bảo hoàn thành trọn vẹn phần cốt lõi của Sprint Goal đúng hạn.

---

## 📁 Danh sách tệp tin nộp bài trong Repository
- 📝 `bt2.docx`: Báo cáo tài liệu phân tích nghiệp vụ hoàn chỉnh.
