# Group Report — Day 02

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|---:|---|---|---|
| 1 | Nguyễn Khánh Toàn | 2A202601843 | |
| 2 | Hồ Văn Thi | 2A20261907 | |
| 3 | Trần Duy Trường | 2A202601247 | |
| 4 | Lê Bình Nguyên | 2A202601659 | |
| 5 | Nguyễn Thế Khôi | 2A202601439 | |
| 6 | Lê Nguyễn Phi Trường | 2A202601541 | |
| 7 | Nguyễn Thiên Lộc | 2A202601479 | |
| 8 | Nguyễn Quang Huy | 2A202601165 | Nhóm trưởng |
| 9 | Nguyễn Anh Quân | 2A202601251 | |
| 10 | Lê Tiến Đạt | 2A202601263 | |
| 11 | Phạm Văn Thắng | 2A202601359 | |
| 12 | Bùi Đặng Quốc An |2A202601799| |

## Phase 3 — Group Convergence: từ candidates về 1 candidate problem


### Bước 3.1 — Trình bày candidates ưu tiên

| # | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh |
|---|---|---|---|---|
| 1 | Kiểm tra tính đầy đủ trước khi nộp bài | Sinh viên | Đối chiếu yêu cầu rải ở worksheet, README, thông báo và các file nộp (20–30 phút) | Workflow hẹp; cần kiểm tra checklist/rule có đủ trước. |
| 2 | **Tra cứu nội quy mất nhiều thời gian** | CSKH và Ban quản lý tòa nhà | Tìm và đối chiếu nhiều PDF/Word/thông báo để xác định thông tin, phiên bản đúng (3–10 phút/câu hỏi) | Actor, baseline và rủi ro trả lời sai đều rõ. |
| 3 | Đọc tài liệu dài trước khi bắt đầu task | Người làm task | Đọc và tổng hợp tài liệu dài để hiểu đủ bối cảnh trước khi làm | Pain quen thuộc nhưng metric chất lượng “hiểu đủ” còn mơ hồ. |
| 4 | Tổng hợp weekly report | AI Intern | Tìm lại code, research, POC rời rạc rồi chuyển thành report (3–5 giờ/tuần) | Workflow rõ, nhưng phạm vi phụ thuộc nguồn dữ liệu và format từng nơi. |
| 5 | Leader tổng hợp và chuẩn hóa báo cáo nhóm | Leader nhóm sinh viên | Ghép nội dung và sửa định dạng không đồng nhất từ các thành viên | Có pain thật, nhưng chuẩn đầu ra và mức chất lượng cần thống nhất. |
| 6 | Nhập dữ liệu từ PDF/Excel mẫu vào web form | Fresher, QA, Team lead | Đọc–gõ từng trường thủ công, dễ thiếu trường/sai định dạng (khoảng 2 giờ/ngày) | Metric tốt nhưng cần quyền truy cập web form và kiểm soát dữ liệu. |
| 7 | Đánh giá rủi ro đạo văn code | Sinh viên ngành kỹ thuật | Tự review theo cảm tính trước khi nộp, không biết mức trùng lặp thực tế | Hậu quả cao nhưng dễ tạo kỳ vọng sai hoặc khuyến khích né kiểm tra đạo văn. |
| 8 | Sinh test cases từ Feature Specification/User Story | QA/Tester | Suy luận edge/error cases (khoảng 90 phút/feature) | Metric rõ; cần QA review bắt buộc vì sai sót có thể lọt lỗi. |
| 9 | Tối ưu luồng ticket onboarding | Học viên mới, Admin/BTC | Ticket thiếu dữ liệu, ticket trùng và nhiều vòng hỏi lại/xử lý thủ công | Impact cao nhưng có phần nên xử lý bằng validation rule trước. |
| 10 | Phân tích sự cố disengagement | Robotics/AV Engineer | Đối chiếu log với video để xác định nguyên nhân (20–60 phút/sự cố) | Domain và dữ liệu phức tạp, khó kiểm chứng trong scope lab. |
| 11 | AI Voice Examiner hỗ trợ trả bài đầu giờ | Giáo viên, học sinh THCS/THPT | Kiểm tra truyền thống chỉ chạm 1–2 học sinh trong 10–15 phút | Reach lớn nhưng cần thiết bị, chính sách lớp học và đánh giá sư phạm. |
| 12 | Tìm lại câu trả lời hoặc quyết định cũ trong Discord server lớp | Sinh viên, TA | Discord search không hiểu ngữ cảnh; phải đoán channel, keyword, time range rồi cuộn thread thủ công (10–15 phút/lần) | Workflow và metric rõ; có thể trả kết quả kèm link message gốc để người dùng tự xác nhận. |

### Bước 3.2 — Gom trùng / cluster

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| A. Tra cứu và hiểu tài liệu | Tra cứu nội quy; tìm quyết định/deadline và câu trả lời kỹ thuật trong Discord; đọc tài liệu dài; tìm tài liệu/data owner; chuyển worksheet thành checklist | Người dùng phải tự tìm, đọc và đối chiếu thông tin nằm rải rác trước khi trả lời hoặc thực hiện task | Candidate được chọn nằm trong cluster này, nhưng scope hẹp hơn: chỉ trả lời dựa trên nội quy đã phê duyệt. |
| B. Tổng hợp và chuẩn hóa đầu ra | Weekly report; tổng hợp báo cáo nhóm; tổng hợp feedback nhiều nguồn; incident report | Gom nhiều mảnh thông tin thành một đầu ra có cấu trúc | Thường cần AI hỗ trợ viết/tóm tắt, nhưng metric chất lượng đầu ra khó chốt nhanh. |
| C. Kiểm tra, chất lượng và nhập liệu | Kiểm tra bài nộp; rủi ro đạo văn code; sinh test cases; nhập PDF/Excel vào form; QA reject/rework | Phát hiện thiếu/sai trước khi gây rework | Nhiều phần có thể giải bằng rule, checklist hoặc template trước khi dùng AI. |
| D. Vận hành theo sự kiện/chuyên môn | Ticket onboarding; phân tích disengagement; voice examiner; các card về quy trình/tác vụ chuyên ngành | Có tần suất hoặc impact cao nhưng phụ thuộc hệ thống, dữ liệu và quyền truy cập chuyên biệt | Rủi ro scope lớn hơn một buổi lab. |

### Bước 3.3 — Shortlist

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|---|---|---|
| **Tra cứu nội quy mất nhiều thời gian** | Có actor cụ thể (CSKH/BQL), workflow 7 bước, bottleneck xác định được, baseline 3–10 phút/câu và metric mục tiêu dưới 30 giây. Có thể vẽ before/after rõ, so sánh FAQ/search thường với AI retrieval, và giữ người thật kiểm tra trước khi trả lời. | Cần xác định nguồn nào là bản chính thức, cách xử lý tài liệu mâu thuẫn/cũ, và kiểm chứng thực tế số câu hỏi cùng thời gian tra cứu. |
| Tìm lại quyết định và deadline trong Discord | Cùng cluster tìm kiếm thông tin; report bổ sung ghi nhận 10–15 phút/lần, 3–4 lần/tuần; TA còn nhận 5–6 câu hỏi lặp lại mỗi buổi lab. Workflow có metric rõ và có thể trả kết quả kèm link message gốc để người dùng tự xác nhận. | Nguồn thay đổi nhanh, quyết định có thể nằm ở nhiều thread; dễ trượt sang search toàn bộ Discord và có rủi ro quyền truy cập. |
| Đọc tài liệu dài trước khi bắt đầu task | Bottleneck đọc hiểu rõ, có thể thử AI tóm tắt và trích xuất action items. | “Hiểu đủ” và chất lượng tóm tắt khó đo; dễ bỏ sót ngữ cảnh quan trọng, nên chưa có success metric mạnh bằng candidate nội quy. |

### Bước 3.4 — Score để đồng thuận

Chấm 1–5. Điểm nhằm làm rõ trade-off; không phải bằng chứng validation.

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh Rule / Workflow / Agent được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Tra cứu nội quy mất nhiều thời gian** | 5 | 5 | 4 | 5 | 5 | 5 | 5 | **34** |
| Tìm lại quyết định và deadline trong Discord | 4 | 4 | 4 | 4 | 5 | 4 | 4 | **29** |
| Đọc tài liệu dài trước khi bắt đầu task | 4 | 4 | 3 | 3 | 5 | 4 | 4 | **27** |

**Candidate nhóm chọn:**

```text
Tra cứu nội quy mất nhiều thời gian.
```

**Vì sao chọn:**

- Pain nằm ở một bước cụ thể: tìm và đối chiếu nội quy phân tán trước khi CSKH/BQL trả lời cư dân.
- Có baseline để kiểm chứng ở Phase 4: 3–10 phút/câu hỏi; tác động gồm phản hồi chậm, câu trả lời thiếu/sai và quá tải khi câu hỏi lặp lại.
- Ranh giới an toàn có thể xác định sớm: chỉ dùng knowledge base đã phê duyệt, luôn hiển thị trích dẫn, và chuyển BQL khi không tìm được nguồn hoặc độ tin cậy thấp.
- Có phương án không dùng AI đáng so sánh (FAQ chuẩn, chuẩn hóa tên/phiên bản tài liệu, search tài liệu), vì vậy nhóm không mặc định chọn agent.
- Scope đủ nhỏ để làm rõ problem → workflow → metric → boundary trong phần còn lại của lab.

**Vì sao không chọn các candidate còn lại:**

- Các bài tổng hợp/đọc tài liệu có workflow hữu ích, nhưng metric chất lượng đầu ra và phạm vi nguồn dữ liệu còn mơ hồ hơn.
- Các bài nhập liệu, ticket onboarding và kiểm tra bài nộp có phần lớn bottleneck có thể được giảm ngay bằng form validation, checklist hoặc rule; cần chứng minh phần AI còn lại thực sự cần thiết.
- Các bài QA test case, AV disengagement, voice examiner và đạo văn code đòi hỏi domain knowledge, dữ liệu, quyền truy cập hoặc guardrail chuyên biệt vượt scope kiểm chứng nhanh của lab.

**Nếu có disagreement, nhóm xử lý thế nào:**

Nhóm dùng bảng score để tách hai việc: chọn candidate có thể đào sâu hôm nay và đánh giá mức hấp dẫn dài hạn của từng ý tưởng. Điểm chưa có evidence bị ghi là giả định, không được bù bằng độ “ngầu” của AI. Với candidate nội quy, nhóm thống nhất chỉ chuyển sang Phase 4 sau khi kiểm tra được tần suất câu hỏi, nguồn nội quy chuẩn và cách xử lý khi tài liệu mâu thuẫn; nếu các điều này không có, nhóm sẽ hạ giải pháp về FAQ + search chuẩn thay vì xây AI/RAG.

## Phase 4 — Quick Validation + Research giải pháp

### Bước 4.1 — Quick validation

Nhóm thực hiện validation nhanh bằng 3 kịch bản/phỏng vấn do nhóm cung cấp, đại diện cho CSKH mới, CSKH lâu năm và Supervisor. Đây là tín hiệu định tính theo vai trò; nhóm vẫn cần log/ticket thật để định lượng tần suất và baseline toàn bộ vận hành.

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| CSKH mới (<6 tháng), câu hỏi phí sạc xe điện qua Zalo | 1 người / 1 tình huống | Mở 3 file PDF/Word, tìm “xe điện”, không biết bản nào hiệu lực rồi phải hỏi Trưởng nhóm. Mất 8–10 phút, trong đó 3–5 phút chờ xác nhận. | Một tình huống không cho biết tần suất theo chủ đề; mức phí có thể là thông tin nhạy cảm cần kiểm tra nguồn tuyệt đối. | Ưu tiên chức năng chỉ rõ **file có hiệu lực, phiên bản, trang/điều khoản**; không chỉ trả lời bằng văn bản tự do. |
| CSKH lâu năm (>2 năm), câu hỏi thi công cuối tuần qua Hotline | 1 người / 1 tình huống | Nhân viên nhớ quy định cũ nhưng phải tìm thông báo điều chỉnh mới; dùng Notepad/Excel cá nhân làm workaround. Mất 3–5 phút và phải hẹn gọi lại. | Note cá nhân giúp nhanh nhưng tạo “nguồn sự thật” không chính thức; chưa biết tỷ lệ cập nhật bị bỏ sót. | Corpus phải gom cả quy chế gốc và thông báo điều chỉnh; kết quả hiển thị ngắn gọn, có link/citation để CSKH skim khi đang gọi. |
| Supervisor CSKH, khiếu nại về phí phạt nước | 1 người / 1 sự cố | Nhân viên đã dùng file quy định năm 2024; Supervisor phải đối chiếu phụ lục, họp chấn chỉnh và xin lỗi cư dân. Xử lý hậu quả mất nửa ngày. | Đây là một sự cố nghiêm trọng, không cho biết tỷ lệ xảy ra; nhãn `[OLD_K_DUNG]` và file ghim vẫn có thể bị bỏ qua. | Bổ sung version control: owner, ngày hiệu lực, trạng thái active/archived và audit trail; AI chỉ truy xuất tài liệu active. |
| Desk research về sản phẩm CSKH có knowledge base | 3 nguồn chính thức | Zendesk yêu cầu AI agent có knowledge source để tạo generative reply; các sản phẩm khác cũng hỗ trợ dùng PDF/tài liệu nội bộ và chuyển hội thoại cho người thật. Điều này xác nhận workflow “tra cứu tri thức → trả lời có căn cứ → escalation” là khả thi. | Đây là bằng chứng về **giải pháp trên thị trường**, không xác nhận pain hay nhu cầu trả tiền của BQL/cư dân tại case này. Tài liệu ngoài nguồn chính thức có thể đồng bộ chậm. | Thu hẹp scope pilot: trợ lý cho CSKH tra cứu nội quy đã phê duyệt, chưa mở chatbot tự trả lời cư dân. |

**Insight sau quick validation:**

```text
Pain không chỉ là “search chậm”. CSKH mới không biết file nào có hiệu lực;
CSKH lâu năm dễ dùng knowledge cá nhân cũ; Supervisor chịu hậu quả khi version control thất bại.

Vì vậy, bài toán được thu hẹp thành: giúp CSKH xác định và trích đúng nội quy/ thông báo
đang có hiệu lực trước khi trả lời — không phải chatbot trả lời tự do từ toàn bộ file cũ và mới.
```

**Validation cần làm trước khi coi là Go:**

- Lấy mẫu log/ticket 1 tuần (đã ẩn dữ liệu cá nhân): đếm số câu hỏi về nội quy, tỷ lệ lặp lại, thời gian phản hồi và số ca phải hỏi Supervisor.
- Kiểm tra với người sở hữu nội quy: tài liệu nào là nguồn chuẩn, ai phê duyệt cập nhật, quy tắc ưu tiên khi hai tài liệu mâu thuẫn và cách archive file cũ.
- Test 10–20 câu hỏi lịch sử với corpus mẫu: kiểm citation, phiên bản/ngày hiệu lực và tỷ lệ CSKH phải sửa bản nháp.

**Câu hỏi dùng cho interview/poll:** Lần gần nhất bạn phải tra nội quy là khi nào? Bạn mở những nguồn nào? Bước nào tốn thời gian nhất? Câu trả lời có từng bị sửa/đính chính không? Nếu công cụ chỉ trả lời từ nguồn chính thức và kèm trích dẫn, bạn có dùng trước khi gửi cho cư dân không?

### Bước 4.2 — Research giải pháp đã có

| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Zendesk AI agents — Knowledge sources | [Zendesk documentation](https://support.zendesk.com/hc/en-us/articles/8357749301658-Connecting-knowledge-sources-to-power-generative-replies-in-advanced-AI-agents) | Kết nối help center hoặc nguồn tri thức ngoài để AI agent tạo câu trả lời. | Cho thấy knowledge source là điều kiện nền tảng; có thể kết nối nhiều nguồn và tôn trọng quyền xem nội dung hạn chế. | Zendesk cảnh báo quá nhiều nguồn có thể làm giảm độ chính xác/tăng độ trễ; nội dung ngoài được tìm theo lần đồng bộ gần nhất (thường 24 giờ). | Không nạp mọi PDF/Word ngay lập tức. Pilot chỉ dùng bộ nội quy đã duyệt, có owner và ngày hiệu lực rõ ràng. |
| Azure AI Search — RAG | [Microsoft Learn](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview) | Ground câu trả lời LLM bằng nội dung riêng của tổ chức; hỗ trợ theo dõi citation/provenance và permission metadata. | Citation giúp CSKH kiểm tra lại điều khoản trước khi gửi; permission-aware knowledge base phù hợp với tài liệu nội bộ. | RAG vẫn gặp khó khi câu hỏi mơ hồ và dữ liệu nằm ở nhiều nguồn; retrieval sai sẽ dẫn tới câu trả lời sai dù văn phong có vẻ thuyết phục. | Bắt buộc hiển thị điều/khoản và tên phiên bản tài liệu; AI không được suy đoán ngoài đoạn đã truy xuất. |
| Intercom Fin — Knowledge sources & human handoff | [Knowledge sources](https://www.intercom.com/help/en/articles/9440354-knowledge-sources-to-power-ai-agents-and-self-serve-support), [human handoff](https://www.intercom.com/help/en/articles/7120684-fin-ai-agent-explained) | Dùng bài viết, PDF, website và nguồn nội bộ làm knowledge source; cấu hình chuyển hội thoại cho nhân viên khi cần. | Mô hình vận hành rõ: quản lý nguồn tri thức, kiểm tra cách câu trả lời được tạo, và escalation sang người thật. | Nội dung đồng bộ từ nguồn ngoài có thể cập nhật theo chu kỳ; câu trả lời sai vẫn có thể xảy ra nếu nguồn thiếu/cũ. | Đặt HITL ở pilot: CSKH review rồi mới gửi; chuyển BQL khi không có nguồn, có xung đột, hoặc câu hỏi liên quan ngoại lệ/chính sách mới. |

**Research takeaway:**

```text
Các giải pháp hiện có không bắt đầu bằng một agent tự hành. Pattern lặp lại là: knowledge source được quản trị → truy xuất nội dung liên quan → câu trả lời có căn cứ/citation → người thật hoặc workflow nhận ca ngoại lệ.

Vì vậy, bài toán nhóm không phải “xây chatbot trả lời mọi thứ”. Scope tiếp theo là thử một trợ lý tra cứu cho CSKH trên một knowledge base nội quy đã phê duyệt, có citation và escalation. FAQ/search chuẩn vẫn là phương án baseline để so sánh.
```

## Phase 5 — Workflow + Problem Statement

### Bước 5.1 — Current workflow bản nhóm

```text
CURRENT STATE — khoảng 3–10 phút/câu hỏi (từ 3 kịch bản; cần đo lại bằng log)

[1 Cư dân gửi câu hỏi qua hotline/Zalo/app]
→ [2 CSKH xác định chủ đề cần tra: ~30s]
→ [3 CSKH mở thư mục, tìm qua PDF/Word/thông báo: 2–5']  <-- bottleneck
→ [4 CSKH đối chiếu điều khoản/phiên bản: 1–3']            <-- bottleneck
→ [5 CSKH tự soạn câu trả lời: ~1']
→ [6 CSKH gửi câu trả lời cho cư dân]

Handoff: Cư dân → CSKH; nếu nguồn mâu thuẫn/không tìm thấy → BQL xác minh.
```

| Bước | Actor | Input | Output | Thời gian/tần suất | Ghi chú |
|---|---|---|---|---|---|
| 1 | Cư dân / CSKH | Câu hỏi qua hotline, Zalo hoặc app | Nội dung cần trả lời | Mỗi khi phát sinh câu hỏi | Có thể dùng cách diễn đạt không trùng tên điều khoản. |
| 2 | CSKH | Câu hỏi | Chủ đề/keyword để tra | Khoảng 30 giây | Phụ thuộc kinh nghiệm của người trực. |
| 3 | CSKH | Thư mục PDF, Word, thông báo | Các đoạn tài liệu có vẻ liên quan | 2–5 phút/câu | Bottleneck: tài liệu phân tán, tên file/thuật ngữ khác nhau. |
| 4 | CSKH / BQL | Các điều khoản tìm được | Điều khoản và phiên bản có hiệu lực | 1–3 phút/câu; BQL khi ngoại lệ | Bottleneck: có thể có tài liệu cũ hoặc mâu thuẫn. |
| 5 | CSKH | Điều khoản đã xác minh | Bản trả lời cho cư dân | Khoảng 1 phút | Dễ diễn đạt thiếu căn cứ nếu không lưu nguồn. |
| 6 | CSKH | Bản trả lời | Cư dân nhận phản hồi | Ngay sau bước 5 | Không có log/citation chuẩn để review lại. |

**Bottleneck chính:**

```text
Tìm đúng đoạn nội quy và xác định bản có hiệu lực giữa nhiều tài liệu rời rạc.
Đây là nguyên nhân kéo dài thời gian tra cứu và làm câu trả lời có nguy cơ thiếu hoặc sai.
```

### Bước 5.2 — Future workflow bản nhóm

```text
FUTURE STATE — mục tiêu pilot: đo được thời gian tra cứu dưới 30 giây;
tổng thời gian phụ thuộc vào CSKH review, không tự động gửi cho cư dân.

[1 Cư dân gửi câu hỏi]
→ [2 Rule: xác định tòa nhà/chủ đề và chỉ cho phép knowledge base đã duyệt]
→ [3 Retrieval: tìm đoạn nội quy + phiên bản + ngày hiệu lực]
→ [4 AI tạo bản nháp câu trả lời kèm citation]
→ [5 CSKH kiểm đoạn trích, chỉnh sửa và quyết định gửi]  <-- human boundary
      ├── Có nguồn rõ, đúng phiên bản → [6 CSKH gửi]
      └── Không có nguồn / nguồn mâu thuẫn / ngoại lệ → [7 Chuyển BQL]

Fallback: dùng FAQ/search tài liệu chuẩn; CSKH/BQL tự tra và trả lời như workflow hiện tại.
```

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Số bước chính | 6 | 6–7 | Không giảm bước bằng mọi giá; thay bước tìm thủ công bằng retrieval có kiểm soát. |
| Thời gian tra cứu nội quy | 3–10 phút/câu (từ 3 kịch bản) | Dưới 30 giây trong pilot | Cần đo trên tập câu hỏi thực tế; không tính thời gian BQL xử lý ngoại lệ. |
| Tổng thời gian phản hồi | Chưa có baseline được đo | Đo riêng theo loại câu hỏi | CSKH review là bước bắt buộc, nên không hứa hẹn tự động dưới 30 giây end-to-end. |
| Bước thủ công | 6/6 | CSKH review, gửi và xử lý ngoại lệ | Con người giữ quyền quyết định câu trả lời cuối. |
| Bottleneck chính | Tìm/đối chiếu tài liệu | Review citation và xử lý ngoại lệ | Đây là bottleneck chấp nhận được để kiểm soát chất lượng. |
| Risk mới | Tài liệu cũ hoặc khó tìm | Retrieval nhầm, AI diễn đạt quá nguồn, lộ nội dung nội bộ | Giảm bằng corpus đã duyệt, citation, phân quyền, HITL và fallback. |

### Bước 5.3 — Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Nhân viên CSKH là người tra cứu và soạn phản hồi; BQL là người xác minh ca ngoại lệ; cư dân là người nhận phản hồi. |
| **Workflow** | Nhận câu hỏi → xác định chủ đề → tìm qua PDF/Word/thông báo → đối chiếu phiên bản → soạn câu trả lời → gửi. |
| **Bottleneck** | CSKH mất thời gian nhất ở bước tìm đúng tài liệu và kiểm tra phiên bản có hiệu lực giữa nhiều nguồn phân tán. |
| **Impact** | Ba kịch bản cho thấy 3–10 phút/câu tùy kinh nghiệm và một sự cố dùng file cũ có thể khiến Supervisor mất nửa ngày xử lý. Cần log để xác định tần suất và quy mô thực. |
| **Success Metric** | Trong pilot: (1) đo thời gian tra cứu; mục tiêu dưới 30 giây cho câu có nguồn rõ; (2) ít nhất 95% bản nháp có citation đúng; (3) 0 câu trả lời được gửi nếu không có nguồn/citation. Các ngưỡng cần xác nhận lại sau khi có log. |
| **Boundary** | Không tự gửi cho cư dân; không trả lời ngoài knowledge base đã phê duyệt; không tự chọn tài liệu khi có xung đột; không xử lý thanh toán, booking, đăng ký thẻ xe hoặc quyết định chính sách. |

## Phase 6 — Rule / Workflow / Agent + Decision

### Bước 6.0 — Ma trận độ phù hợp với AI

**Bài toán nằm ở ô: độ mơ hồ thấp, độ phức tạp cao.**

Nội dung nội quy có đáp án phải bám tài liệu chính thức nên độ mơ hồ của **nguồn sự thật** thấp. Tuy vậy, câu hỏi của cư dân có thể diễn đạt tự do, tài liệu có nhiều loại/phiên bản và có nhánh escalation; do đó workflow có nhiều bước nối tiếp. AI không cần tự lập kế hoạch hay tự thực hiện hành động bên ngoài hệ thống.

### Bước 6.1 — So sánh Rule / Workflow / Agent

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | FAQ được duyệt, quy ước tên file/phiên bản, metadata tòa nhà–ngày hiệu lực, form phân loại chủ đề và rule chuyển BQL. | Đủ cho câu hỏi phổ biến, wording dự đoán được và một nguồn nội quy rõ ràng. | Không bao phủ tốt câu hỏi diễn đạt đa dạng hoặc cần tổng hợp nhiều đoạn; FAQ nhanh lỗi thời nếu không có owner cập nhật. | Dùng làm nền tảng, không đủ cho toàn bộ pain. |
| **Workflow** | Rule lọc corpus → retrieval đoạn liên quan → AI tạo draft kèm citation → CSKH review/gửi hoặc BQL xử lý ngoại lệ. | Đủ khi đường đi ổn định, mỗi bước có input/output rõ và AI chỉ hỗ trợ hiểu/diễn đạt ngôn ngữ. | Retrieval/citation nhầm, tài liệu cũ, AI diễn đạt vượt nguồn hoặc lộ nội dung hạn chế. | **Chọn cho pilot.** |
| **Agent** | Agent tự quyết định tìm thêm nguồn, hỏi lại, thay đổi quy trình và trả lời trực tiếp/triage nhiều kênh. | Chỉ cân nhắc khi đã có knowledge governance tốt và nhiều luồng thay đổi động thực sự cần tự lập kế hoạch. | Permission/rủi ro cao; khó audit, có thể tự chọn sai nguồn hoặc hành động quá scope. | Không chọn. |

**Mức chọn:**

```text
Workflow, với Rule là điều kiện bắt buộc cho knowledge base và escalation.
```

**Vì sao chọn:**

- Vấn đề chính là truy xuất và diễn đạt từ nguồn cố định, không phải lập kế hoạch động.
- Workflow giữ được citation, phân quyền, CSKH review và fallback ở từng điểm kiểm soát.
- Rule xử lý được phần metadata/FAQ/escalation rõ ràng; AI chỉ dùng ở phần hiểu câu hỏi và tạo bản nháp có căn cứ.

**Vì sao không chọn mức đơn giản hơn:**

FAQ và search theo keyword có thể giải một phần câu hỏi lặp lại, nhưng chưa xử lý ổn định cách cư dân diễn đạt khác với tên điều khoản hoặc việc cần gom vài đoạn liên quan. Nhóm chỉ giữ Workflow ở scope hẹp và sẽ hạ về FAQ/search nếu pilot không chứng minh được lợi ích.

### Bước 6.2 — Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | CSKH tra cứu và review; BQL là owner xác minh ngoại lệ; cư dân nhận phản hồi. |
| **Workflow** | Cư dân hỏi → CSKH nhận → rule xác định corpus đã duyệt → retrieval đoạn nội quy/phiên bản → AI draft kèm citation → CSKH kiểm và gửi, hoặc chuyển BQL. |
| **Bottleneck** | Tìm đúng nội quy có hiệu lực và đối chiếu nhiều nguồn trước khi soạn câu trả lời. |
| **Impact** | Ba kịch bản cho thấy tra cứu mất 3–10 phút/câu và version sai có thể dẫn đến khiếu nại/rework nửa ngày; chưa có log xác nhận tần suất hoặc tỷ lệ sai. |
| **Success Metric** | Pilot đo: thời gian tra cứu dưới 30 giây cho câu có nguồn rõ; ≥95% bản nháp dẫn đúng điều khoản/phiên bản; 0 câu tự gửi hoặc trả lời không có citation. |
| **Boundary** | Chỉ dùng corpus nội quy đã duyệt và đúng quyền; không tự gửi, không suy luận ngoài nguồn, không tự xử lý chính sách/booking/thanh toán/đăng ký thẻ xe. |
| **AI intervention point** | Sau khi rule chọn corpus phù hợp và trước khi CSKH gửi phản hồi. |
| **Mức chọn** | Workflow: rule quản trị nguồn và escalation; retrieval + AI tạo draft; CSKH/BQL kiểm soát cuối. |
| **Rủi ro & người thật kiểm tra** | Risk: truy xuất nhầm, nguồn cũ/mâu thuẫn, hallucination, lộ nội dung. CSKH kiểm citation và nội dung trước khi gửi; BQL quyết định khi không có nguồn, nguồn xung đột hoặc thuộc ngoại lệ. |

### Bước 6.3 — Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
|---|---|---|
| Actor và workflow đã rõ chưa? | Yes | Actor, handoff và bottleneck đã được mô tả cụ thể. |
| Baseline và success metric đã đo được chưa? | Not Yet | Đã có 3 kịch bản theo vai trò cho baseline 3–10 phút/câu, nhưng chưa có log/ticket để định lượng tần suất và đo pilot. |
| Có data/input đủ dùng chưa? | Not Yet | Chưa xác định corpus chính thức, owner, phiên bản, quyền truy cập và quy tắc ưu tiên tài liệu. |
| Nếu AI sai, hậu quả có chấp nhận được không? | Yes, có điều kiện | Chỉ chấp nhận khi không tự gửi, luôn có citation, CSKH review và BQL nhận ca ngoại lệ. |
| Có người review/owner vận hành không? | Not Yet | Vai trò CSKH/BQL đã xác định, nhưng cần người thật được chỉ định để duyệt corpus và vận hành pilot. |
| Có cách non-AI đơn giản hơn không? | Yes | FAQ, metadata phiên bản và search chuẩn là baseline bắt buộc để so sánh. |

**Decision:**

```text
Not Yet — sẵn sàng thiết kế pilot Workflow, chưa sẵn sàng triển khai hoặc mở chatbot trực tiếp cho cư dân.
```

**Lý do:**

Problem, workflow và boundary đã đủ rõ để không chọn Agent. Ba kịch bản xác nhận pain ở cả CSKH mới, CSKH lâu năm và Supervisor; tuy nhiên knowledge governance chưa được xác minh bằng corpus/log vận hành. Triển khai AI trước khi biết tài liệu nào có hiệu lực, ai duyệt cập nhật và ai chịu trách nhiệm ca sai sẽ làm tăng rủi ro hơn là giảm thời gian tra cứu.

**Nếu Go sau validation, pilot nhỏ nhất là:**

```text
Một tòa nhà, một corpus nội quy đã được BQL duyệt, 20–30 câu hỏi lịch sử đã ẩn dữ liệu cá nhân.
CSKH dùng trợ lý ở chế độ draft + citation trong 1 tuần; không tự gửi cho cư dân.
Đo thời gian tra cứu, tỷ lệ citation đúng, tỷ lệ CSKH phải viết lại và số ca escalation.
So sánh cùng tập câu hỏi với FAQ/search chuẩn.
```

**Nếu Not Yet, cần validate gì trước:**

```text
1. Lấy mẫu log/ticket 1 tuần để xác nhận tần suất, thời gian, loại câu hỏi và số ca phải hỏi Supervisor.
2. Lập danh mục tài liệu: owner, ngày hiệu lực, phiên bản, quyền truy cập, trạng thái active/archived và quy tắc xử lý mâu thuẫn.
3. Chốt người chịu trách nhiệm review citation, xử lý escalation, dừng pilot khi có trả lời sai và test 10–20 câu hỏi lịch sử trước khi dùng thật.
```
