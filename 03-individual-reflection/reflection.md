# 03 — Individual Reflection Example

## Đóng góp của Minh trong nhóm

| Hoạt động               | Tôi đã làm gì?                                                                                             | Kết quả                                                                  |
| ----------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Scan cá nhân            | Đề xuất 6 problems liên quan Driver Monitoring và Autonomous Driving                                       | Nhóm có nhiều candidate xoay quanh phân tích sự cố và review video       |
| Pitch                   | Pitch bài toán phân tích nguyên nhân disengagement từ log + video                                          | Được chọn làm Problem #1 của nhóm                                        |
| Challenge               | Đề xuất thu hẹp phạm vi, chỉ tập trung vào Incident Lens thay vì làm hệ thống Driver Monitoring hoàn chỉnh | Scope phù hợp với thời gian của lab                                      |
| Workflow                | Xây dựng current workflow và future workflow cho quá trình phân tích sự cố                                 | Nhóm dùng để xác định bottleneck và human boundary                       |
| Research                | Tìm hiểu các hướng sử dụng VLM, LLM và cách kết hợp log với video trong phân tích sự cố                    | Nhóm thống nhất hướng dùng AI hỗ trợ phân tích thay vì tự động hoàn toàn |
| Rule / Workflow / Agent | Đề xuất bài toán thuộc nhóm Workflow với human-in-the-loop                                                 | Nhóm thống nhất AI chỉ hỗ trợ, kỹ sư vẫn là người xác nhận kết quả       |


## Bảng dùng AI trong reflection

| Phase             | Tôi dùng AI để làm gì?                                      | AI hữu ích ở đâu?                                | AI sai/hời hợt ở đâu?                        | Tôi sửa gì                                               |
| ----------------- | ----------------------------------------------------------- | ------------------------------------------------ | -------------------------------------------- | -------------------------------------------------------- |
| Scan              | Gợi ý thêm các problems trong Robotics và Driver Monitoring | Giúp mở rộng góc nhìn và tìm thêm candidate      | Một số ý quá rộng hoặc thiên về giải pháp AI | Chỉ giữ các problem có actor, workflow và pain rõ ràng   |
| Workflow          | Nhờ AI mô tả current workflow và future workflow            | Nhanh hơn khi xác định bottleneck                | AI đôi lúc bỏ qua bước QA review             | Thêm human boundary vào workflow                         |
| Research          | Tìm hiểu các hướng kết hợp VLM và LLM                       | Hiểu thêm cách xử lý video và log đa phương thức | Một số gợi ý chưa phù hợp với phạm vi lab    | Chỉ giữ những giải pháp có thể demo trong thời gian ngắn |
| Problem Statement | Nhờ AI phản biện Problem Card và Success Metric             | Giúp viết problem rõ hơn và bổ sung metric       | AI có xu hướng đề xuất tự động hóa hoàn toàn | Điều chỉnh về hướng AI hỗ trợ kỹ sư thay vì thay thế     |


## Bài học

- Một problem tốt phải xuất phát từ pain thật, có actor, workflow và cách đo hiệu quả rõ ràng.
- Việc vẽ current workflow giúp xác định chính xác bottleneck trước khi nghĩ đến giải pháp AI.
- Không phải bài toán nào cũng nên xây Agent; với Incident Lens, mô hình Workflow có human-in-the-loop phù hợp hơn vì kết quả phân tích vẫn cần kỹ sư xác nhận.
- AI hữu ích trong việc brainstorm, phản biện và hoàn thiện ý tưởng, nhưng vẫn cần kiểm chứng bằng kiến thức domain và mục tiêu của nhóm.

Nếu làm lại:

```text
Tôi sẽ phỏng vấn thêm QA Engineer hoặc Robotics Engineer để kiểm chứng thời gian phân tích sự cố và quy trình hiện tại, thay vì chỉ dựa trên giả định và trải nghiệm của nhóm. Điều này sẽ giúp Problem Statement và Success Metric có cơ sở thực tế hơn.
```

---

