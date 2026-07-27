# 01 — Individual Problem Scan

| #  | Lăng kính          | Problem quan sát được                                              | Ai chịu ảnh hưởng?                             | Dấu hiệu thật                                   |
| -- | ------------------ | ------------------------------------------------------------------ | ---------------------------------------------- | ----------------------------------------------- |
| 1  | Tốn thời gian      | Review video Driver Monitoring để tìm đoạn tài xế mất tập trung    | QA Engineer, AI Engineer                       | Mất 30–60 phút chỉ để tìm vài sự kiện           |
| 2  | Tốn thời gian      | Phân tích nguyên nhân disengagement phải mở đồng thời log và video | Robotics Engineer, Autonomous Vehicle Engineer | Debug một sự cố mất 20–60 phút                  |
| 3  | Lặp lại            | Ghi timestamp và mô tả thủ công cho từng sự kiện trong video       | QA, Data Annotator                             | Lặp lại hàng chục lần mỗi video                 |
| 4  | AI có thể tốt hơn  | Chưa có công cụ tự động tóm tắt diễn biến sự cố từ log + video     | Kỹ sư AI, Team Leader                          | Phải tự đọc log và xem video rồi viết báo cáo   |
| 5  | AI có thể tốt hơn  | Không có timeline tự động hiển thị các sự kiện quan trọng          | Tester, QA                                     | Phải tua video nhiều lần để đối chiếu           |
| 6 | AI có thể tốt hơn  | Không có công cụ tự động sinh Incident Report sau khi chạy thử     | Team Leader, Project Manager                   | Báo cáo viết thủ công, nội dung không đồng nhất |

Vì sao phần scan này mạnh
- Có scan rộng trước khi hội tụ.
- Có nhiều lăng kính khác nhau (tốn thời gian, lặp lại, AI có thể làm tốt hơn).
- Mỗi problem đều xác định rõ người chịu ảnh hưởng và dấu hiệu thực tế.
- Các vấn đề đều xuất phát từ quy trình review và phân tích sự cố trong lĩnh vực Robotics/Autonomous Driving, thay vì bắt đầu từ ý tưởng xây dựng một công cụ AI.

## Top 3

| Rank  | Problem                                                    | Vì sao chọn                                                                                                | Điều còn chưa chắc                                                                  |
| ----- | ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| **1** | Phân tích nguyên nhân disengagement từ log và video        | Pain rõ ràng, xảy ra sau mỗi lần test, mất nhiều thời gian và phù hợp để dùng VLM phân tích đa phương thức | Cần kiểm chứng độ chính xác của AI khi suy luận nguyên nhân sự cố                   |
| **2** | Review video Driver Monitoring để tìm tài xế mất tập trung | Công việc lặp lại, tốn thời gian, dễ bỏ sót sự kiện; AI có thể tự động phát hiện và đánh dấu               | Hiệu quả phụ thuộc vào chất lượng video và khả năng nhận diện của mô hình           |
| **3** | Tự động tạo Incident Report sau khi chạy thử               | Báo cáo hiện viết thủ công, mất thời gian và thiếu nhất quán; AI có thể tạo báo cáo chuẩn hóa              | Cần xác định mức độ chi tiết và độ tin cậy của báo cáo AI trước khi sử dụng thực tế |


## Problem Card #1 — Phân tích sự cố disengagement

**Problem 1 câu:**  
Sau mỗi lần chạy thử xe tự hành, kỹ sư phải mất 20–60 phút để đối chiếu log và video nhằm xác định nguyên nhân disengagement, khiến quá trình debug chậm và dễ bỏ sót thông tin.
**Actor:**  
Robotics Engineer / Autonomous Vehicle Engineer chịu trách nhiệm phân tích sự cố sau mỗi buổi chạy thử.

**Thời điểm / bối cảnh:**  
Ngay sau mỗi lần test xe hoặc khi phát hiện một sự kiện disengagement cần phân tích.

**Current workflow:**

```text
1. Mở video ghi hình buổi chạy
2. Mở log (ROS/CAN/System log)
3. Đối chiếu timestamp giữa log và video
4. Tìm đoạn xảy ra disengagement
5. Xem lại video nhiều lần để xác định nguyên nhân
6. Đọc log trước và sau sự kiện
7. Viết Incident Report và chia sẻ với nhóm
```

**Bottleneck:**  
Bước 5–6: phải xem đi xem lại video và đọc log để hiểu nguyên nhân sự cố, mất nhiều thời gian và phụ thuộc vào kinh nghiệm của kỹ sư.

**Impact:**  
Mỗi sự cố mất khoảng 20–60 phút để phân tích. Với nhiều lần chạy thử trong tuần, tổng thời gian dành cho việc review và debug rất lớn, đồng thời làm chậm quá trình cải thiện hệ thống.

**Success metric:**  
Giảm thời gian phân tích từ 20–60 phút xuống dưới 10 phút, đồng thời vẫn xác định đúng nguyên nhân và không làm tăng số lần phải phân tích lại.

**Non-AI alternative:**  
Đồng bộ timestamp giữa log và video hoặc sử dụng template Incident Report giúp giảm thao tác thủ công, nhưng vẫn phải đọc log và xem video để suy luận nguyên nhân.

**AI hypothesis:**  
AI sử dụng VLM kết hợp log để tự động:

- đồng bộ log và video,
- phát hiện các sự kiện quan trọng,
- tóm tắt diễn biến,
- gợi ý nguyên nhân,
- tạo Incident Report nháp để kỹ sư kiểm tra trước khi lưu.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 35–60 phút

[1 Mở video: 3']
→ [2 Mở log: 2']
→ [3 Đồng bộ timestamp: 10']
→ [4 Tìm sự kiện: 10']
→ [5 Phân tích log + video: 20']  <-- bottleneck
→ [6 Viết Incident Report: 10'] 
```

### Draft future workflow

```text
FUTURE STATE — 8–12 phút

[1 Upload log + video: 1']
→ [2 AI đồng bộ timestamp: <1']
→ [3 AI phát hiện sự kiện: 1']
→ [4 AI tóm tắt & gợi ý nguyên nhân: 2']
→ [5 Engineer review & chỉnh sửa: 6']  <-- human boundary
→ [6 Xuất Incident Report: 1']

Fallback: Nếu AI không chắc chắn hoặc confidence thấp,
Engineer sẽ tự xem lại video và log.
```

## Problem Card #2 — Tự động tạo Incident Report

**Problem 1 câu:**  
Sau khi hoàn thành phân tích sự cố, kỹ sư vẫn phải viết Incident Report thủ công từ log và video, khiến báo cáo mất thời gian và thiếu tính nhất quán giữa các thành viên.
**Actor:**  
Robotics Engineer, Team Leader hoặc Project Manager chịu trách nhiệm tổng hợp kết quả sau mỗi buổi chạy thử.
**Thời điểm / bối cảnh:**  
Sau khi phân tích xong một sự cố hoặc kết thúc một buổi thử nghiệm xe tự hành.
**Current workflow:**

```text
1. Mở ghi chú phân tích
2. Xem lại log và video
3. Viết mô tả sự cố
4. Ghi nguyên nhân
5. Ghi ảnh hưởng
6. Đề xuất hướng xử lý
7. Gửi Incident Report cho nhóm
```

**Bottleneck:**  
Bước 3–6: kỹ sư phải tổng hợp thông tin từ nhiều nguồn và diễn đạt lại bằng tay, dễ thiếu thông tin hoặc không thống nhất giữa các báo cáo.
**Impact:**  
Mỗi Incident Report mất khoảng 15–20 phút để hoàn thành. Với nhiều sự cố mỗi tuần, tổng thời gian dành cho việc viết báo cáo khá lớn và chất lượng báo cáo phụ thuộc vào từng người.
**Success metric:**  
Giảm thời gian tạo báo cáo xuống dưới 5 phút, đồng thời đảm bảo đầy đủ các mục quan trọng và hạn chế việc phải chỉnh sửa nhiều.
**Non-AI alternative:**  
Sử dụng template Incident Report chuẩn để giảm thời gian định dạng, nhưng nội dung vẫn phải viết thủ công.
**AI hypothesis:**  
AI sử dụng thông tin từ log, video và kết quả phân tích để:

- sinh Incident Report nháp,
- tóm tắt diễn biến,
- liệt kê nguyên nhân và ảnh hưởng,
- đề xuất các bước xử lý tiếp theo,
- để kỹ sư kiểm tra trước khi phát hành.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 15–20 phút

[1 Thu thập thông tin: 5']
→ [2 Viết mô tả: 7']  <-- bottleneck
→ [3 Ghi nguyên nhân & ảnh hưởng: 5']
→ [4 Review và gửi: 3']
```

### Draft future workflow

```text
FUTURE STATE — 3–5 phút

[1 AI nhận log + video: 1']
→ [2 AI tạo Incident Report nháp: 1']
→ [3 Engineer review & chỉnh sửa: 2']  <-- human boundary
→ [4 Xuất PDF/Markdown và gửi: 1']

Fallback: Nếu báo cáo AI chưa đầy đủ,
Engineer chỉnh sửa hoặc viết bổ sung trước khi gửi.
```

## Problem Card #3 — Review video Driver Monitoring

**Problem 1 câu:**  
QA Engineer phải xem lại toàn bộ video Driver Monitoring để tìm các đoạn tài xế mất tập trung, ngủ gật hoặc nhìn khỏi đường, khiến quá trình review mất nhiều thời gian và dễ bỏ sót sự kiện.
**Actor:**  
QA Engineer / AI Engineer chịu trách nhiệm kiểm tra và xác nhận các sự kiện Driver Monitoring.
**Thời điểm / bối cảnh:**  
Sau mỗi buổi thu thập dữ liệu hoặc khi cần đánh giá chất lượng mô hình Driver Monitoring.
**Current workflow:**

```text
1. Mở video Driver Monitoring
2. Xem video từ đầu
3. Quan sát hành vi tài xế
4. Khi phát hiện sự kiện, ghi timestamp
5. Ghi mô tả hành vi
6. Tiếp tục xem cho đến hết video
7. Xuất danh sách sự kiện
```

**Bottleneck:**  
Bước 2–5: phải xem liên tục toàn bộ video để phát hiện sự kiện. Phần lớn thời gian chỉ là xem những đoạn không có gì xảy ra.
**Impact:**  
Mỗi video mất khoảng 30–60 phút để review. Khi số lượng video lớn, QA phải dành nhiều giờ chỉ để tìm các sự kiện cần đánh giá.
**Success metric:**  
Giảm thời gian review từ 30–60 phút xuống dưới 10 phút, đồng thời vẫn phát hiện được hầu hết các sự kiện quan trọng.
**Non-AI alternative:**  
Tăng tốc độ phát video hoặc chia nhỏ video để nhiều người cùng review. Tuy nhiên vẫn cần con người xem toàn bộ video.
**AI hypothesis:**  
AI sử dụng VLM để:

- phát hiện các hành vi mất tập trung,
- tự động đánh dấu timestamp,
- tạo timeline sự kiện,
- cho phép QA chỉ review các đoạn AI đã đánh dấu.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 30–60 phút

[1 Mở video: 1']
→ [2 Xem toàn bộ video: 35']
→ [3 Ghi timestamp: 10']  <-- bottleneck
→ [4 Ghi mô tả: 8']
→ [5 Xuất kết quả: 3']
```

### Draft future workflow

```text
FUTURE STATE — 6–10 phút

[1 Upload video: 1']
→ [2 AI phát hiện sự kiện: 2']
→ [3 AI tạo timeline: 1']
→ [4 QA review các đoạn được đánh dấu: 5']  <-- human boundary
→ [5 Xuất kết quả: 1']

Fallback: Nếu AI bỏ sót hoặc confidence thấp,
QA sẽ xem lại toàn bộ video.
```
