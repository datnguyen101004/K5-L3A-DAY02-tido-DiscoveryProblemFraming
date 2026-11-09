# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: tido
- Thành viên: xem `TEAM.md` (Phạm Nguyễn Tất Đạt, Nguyễn Ngọc Toàn, Nguyễn Tuấn Quang)
- Candidate problem được chọn (1 câu): Nhóm kỹ sư và Product Manager bị bế tắc 20–30 phút trong các buổi họp kỹ thuật do tranh cãi cảm tính và bảo vệ thiên kiến cá nhân khi chọn giải pháp, dẫn đến lãng phí giờ công và nguy cơ chọn sai kiến trúc hệ thống.
- Quyết định cuối: **Go** (tiến hành xây dựng Proof-of-Concept dạng Copilot bán tự động hỗ trợ trích xuất luận điểm và ma trận trade-off sau phiên tranh luận).

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Phạm Nguyễn Tất Đạt | Khi tranh luận bảo vệ đề xuất kỹ thuật/sản phẩm, muốn có góc nhìn so sánh trade-off khách quan để chọn phương án tối ưu | SWE, PM, Tech Lead | Tranh cãi bế tắc do ai cũng bảo vệ cái tôi/thiên kiến (25'/buổi) | "Nếu AI chen ngang ngắt lời real-time khi mọi người đang nói thì có gây ức chế và ngắt mạch họp không?" (Quang hỏi) |
| 2 | Phạm Nguyễn Tất Đạt | Khi chạy xe theo ca, muốn biết khung giờ và khu vực có tỷ lệ nổ cuốc cao nhất để tối ưu doanh thu | Tài xế Xanh SM | Chờ cuốc vô định 25' giữa các khung giờ thấp điểm | "Dữ liệu định vị và cuốc xe là của nội bộ hãng Xanh SM, làm sao mình lấy được data để kiểm chứng?" (Toàn hỏi) |
| 3 | Phạm Nguyễn Tất Đạt | Khi làm đồ án môn học, muốn có template chuẩn và bot nhắc nhở Linear/Slack để không bỏ bê tiến độ | Sinh viên CNTT | Cấu hình workspace và chia nhỏ task ban đầu mất 60' và nản chí | "Sinh viên ngại dùng tool là do thói quen, liệu có bot hướng dẫn thì các bạn có chịu duy trì không?" (Toàn hỏi) |
| 4 | Nguyễn Ngọc Toàn | Khi Tester hỏi lặp lại về luồng/cấu hình, muốn họ tự tìm được câu trả lời cũ để không ngắt quãng mạch code | Software Engineer (Module Owner) | Dừng việc tra cứu lại code/tài liệu mất 5'/câu (tổng 70-120'/tuần) | "Chỉ có 25–50% câu là câu cũ, vậy nếu viết một trang FAQ Notion chuẩn thì có giải quyết được 80% mà không cần AI không?" (Đạt hỏi) |
| 5 | Nguyễn Ngọc Toàn | Khi cần biết lý do chọn thiết kế cũ, muốn tìm nhanh trong chat/Drive/Jira để không làm phiền người khác | Software Engineer | Mất 5–15' tìm kiếm phân tán qua 3 công cụ khác nhau | "Impact chỉ mất 5–30'/tuần là khá nhỏ, liệu có đáng xây hẳn một hệ thống AI riêng không?" (Đạt hỏi) |
| 6 | Nguyễn Ngọc Toàn | Khi vào project mới, muốn chạy được local ngay trong ngày đầu để bắt tay vào task sớm | SWE mới vào team | Kẹt cấu hình biến môi trường config mất ~2 giờ | "Tần suất vào project mới của 1 dev rất thấp (vài tháng/lần), tổng impact cả năm có đủ lớn không?" (Quang hỏi) |
| 7 | Nguyễn Tuấn Quang | Khi firmware lỗi ngoại vi hoặc FreeRTOS, muốn khoanh vùng nguyên nhân theo từng bước để không lặp lại kiểm tra | Kỹ sư/sinh viên embedded | Gắn debugger, mò mẫm thử nghiệm mất 60–120'/lần debug | "Nhiều lỗi do phần cứng vật lý (hở chân, nhiễu nguồn) AI không đo được, nếu chỉ cần cuốn sổ log debug thì đã giải quyết chưa?" (Đạt hỏi) |
| 8 | Nguyễn Tuấn Quang | Khi chuẩn bị phỏng vấn embedded bằng tiếng Anh, muốn diễn đạt chuẩn thuật ngữ để trả lời mạch lạc | Ứng viên Embedded | Soạn nháp câu trả lời bằng tiếng Anh mất 45'/câu | "Các tool như ChatGPT hay Elsa Speak đã làm việc này rất tốt, điểm khác biệt của nhóm là gì?" (Toàn hỏi) |
| 9 | Nguyễn Tuấn Quang | Khi ứng tuyển vị trí mới, muốn chọn và viết bullet points dự án phù hợp để CV 1 trang trung thực | Ứng viên Embedded | Viết lại bullet points kết quả thực tế mất 40'/bản | "Nếu lập một file 'thư viện bullet mẫu' thì cần gì đến AI phức tạp?" (Đạt hỏi) |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A. Năng suất & Cộng tác nhóm kỹ thuật | #1 (Trade-off cuộc họp), #4 (Tester hỏi lặp lại), #5 (Tìm tài liệu/quyết định cũ) | Vấn đề giao tiếp, chia sẻ ngữ cảnh và ra quyết định giữa các thành viên trong nhóm phát triển phần mềm |
| B. Onboarding & Quy trình cá nhân kỹ sư | #6 (Setup môi trường dev), #7 (Debug firmware nhúng), #9 (Viết bullet CV) | Quy trình thao tác kỹ thuật cá nhân lặp lại, tốn thời gian mò mẫm tra cứu hoặc thử nghiệm |
| C. Học tập & Đời sống ngoài chuyên môn | #2 (Tài xế Xanh SM), #3 (Quản lý đồ án sinh viên), #8 (Luyện phỏng vấn tiếng Anh) | Vấn đề tổ chức cuộc sống và kỹ năng mềm ngoài phạm vi nội bộ nhóm kỹ thuật |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm 60% thời gian lãng phí vào các cuộc tranh luận bế tắc và nâng cao chất lượng quyết định kỹ thuật của team
├── Opportunity A: Giảm thiểu sự chi phối của cái tôi và thiên kiến cá nhân (confirmation bias) khi bảo vệ giải pháp
├── Opportunity B: Chuẩn hóa việc trích xuất và đối chiếu các tiêu chí trade-off (chi phí, độ phức tạp, thời gian) một cách minh bạch
└── Opportunity C: Rút ngắn thời gian lập biên bản và tổng hợp sau các phiên tranh luận kỹ thuật
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:
- *"Xây bot Discord lắng nghe giọng nói rồi ngắt lời cuộc họp"* (Đây là solution công nghệ, không phải opportunity).
- *"Dùng mô hình LLM fine-tune để tự chấm điểm phương án"* (Solution kỹ thuật).
- *"Tạo dashboard hiển thị voting real-time"* (Tính năng giao diện).

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **#1. Phân tích trade-off cuộc họp (Đạt)** | 5 | 4 | 5 | 5 | 4 | 5 | 5 | **33** |
| #4. Trả lời lặp lại cho Tester (Toàn) | 5 | 5 | 4 | 4 | 4 | 4 | 5 | 31 |
| #7. Hỗ trợ debug firmware (Quang) | 4 | 4 | 4 | 3 | 3 | 3 | 4 | 25 |

**Candidate được chọn:** Candidate #1 — Trợ lý phân tích luận điểm và trade-off đa chiều trong các buổi tranh luận kỹ thuật/sản phẩm (Pitch của Đạt).

**Vì sao chọn:**
1. **Pain point rất thật và cấp thiết:** Cả 3 thành viên đều đã trải qua cảm giác bế tắc, tranh cãi kéo dài hàng giờ khi bảo vệ giải pháp kiến trúc trong các đồ án và dự án công ty.
2. **Phát huy đúng giá trị cốt lõi của LLM/Agent:** Xử lý ngôn ngữ tự nhiên, phân tích ngữ nghĩa đa chiều và cân nhắc trade-off là thế mạnh vượt trội của AI mà các giải pháp No-AI (Rule/FAQ/Template) không thể làm được.
3. **Impact lớn:** Tiết kiệm từ 20–30 phút của cả tập thể (4–8 người/buổi), tránh rủi ro chọn sai công nghệ tốn hàng tháng refactor.

**Vì sao loại các candidate còn lại:**
- *Loại #4 (Tester hỏi lặp lại):* Phần lớn câu hỏi lặp lại có thể giải quyết được bằng No-AI (viết tài liệu Wiki/Notion FAQ rõ ràng); nếu dùng AI thì chỉ là RAG thông thường, ít tính đột phá.
- *Loại #7 (Debug firmware):* Quá phụ thuộc vào phần cứng vật lý bên ngoài (dây nối, đo xung, oscilloscope) mà AI không thể tương tác trực tiếp; nguy cơ AI hallucination khi không có đủ context phần cứng.

**Xử lý bất đồng:** Ban đầu Toàn và Quang lo ngại việc xử lý audio real-time tiếng Việt rất dễ lỗi và gây ngắt quãng dòng suy nghĩ của team. Đạt đã thuyết phục và thống nhất điều chỉnh phạm vi: **Không can thiệp ngắt lời real-time bằng giọng nói**, mà chuyển thành **xử lý trên text transcript sau mỗi block tranh luận 15 phút hoặc khi team chủ động yêu cầu (on-demand)**. Cả nhóm đồng thuận 100%.

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---|---|---|
| 1 | Các kỹ sư sẵn sàng chấp nhận một bảng phân tích trade-off do AI gợi ý để làm cơ sở ra quyết định | Value | 5 | 2 | Có (Kiểm chứng trước) |
| 2 | AI có thể trích xuất chính xác các luận điểm kỹ thuật từ văn bản trao đổi mà không bịa đặt hoặc thiên vị người nói nhiều | Feasibility | 5 | 2 | Có (Kiểm chứng trước) |
| 3 | Người tham gia cuộc họp chịu đọc bảng ma trận trade-off tóm tắt thay vì tiếp tục cãi nhau cảm tính | Usability | 4 | 3 | Có |
| 4 | Chi phí gọi API LLM cho mỗi buổi họp 60 phút nằm trong ngưỡng chấp nhận được (< 0.5 USD/buổi) | Viability | 3 | 4 | Không |
| 5 | Team có sẵn công cụ Speech-to-Text để chuyển âm thanh cuộc họp thành văn bản | Feasibility | 4 | 4 | Không |

Giả định nhóm kiểm chứng trong buổi này: **Giả định #1 và #2** (Tính giá trị thực tế của bảng trade-off và khả năng bóc tách khách quan của AI).

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn nhanh 3 đồng nghiệp/sinh viên làm đồ án capstone và phân tích transcript 1 buổi thảo luận kiến trúc thực tế.

Interview snapshot:

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | Tech Lead / Senior Dev nhóm 6 người tại một công ty phần mềm outsource |
| Câu nói đáng nhớ nhất (nguyên văn) | *"Họp chọn giải pháp mệt nhất là ông nào cũng bảo phương án của mình nhanh nhất, nhẹ nhất. Nhưng khi hỏi 'thế nếu scale lên 100k user hoặc team mở rộng thì sao' thì lại im lặng hoặc lảng tránh. Bọn anh toàn mất nửa tiếng chỉ để bắt từng ông thừa nhận nhược điểm của mình."* |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Buổi họp RFC chọn giữa RESTful API truyền thống hay chuyển sang gRPC cho hệ thống microservices nội bộ. Hai bên cãi nhau 45 phút, cuối cùng sếp vào chốt theo kinh nghiệm cũ vì hết giờ. |
| Hiện đang xử lý bằng cách nào (workaround)? | Phải cử 1 người làm "thẩm phán" (facilitator) ngồi ghi bảng trắng hai cột Pros/Cons, nhưng người ghi chép cũng bị cuốn vào tranh luận nên bảng trắng ghi sơ sài. |
| Mất bao lâu, bao lần? | 1–2 lần/tuần, mỗi buổi họp review mất 30–45 phút tranh luận không hồi kết. |
| Insight / opportunity rút ra | Nhu cầu lớn nhất không phải là "ai thắng ai thua", mà là **cần một bên thứ ba trung lập liệt kê sòng phẳng mọi sự đánh đổi (trade-off) theo các chiều: thời gian dev, độ phức tạp hạ tầng, khả năng scale**. |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Phỏng vấn Tech Lead & Dev | 3 người | 3/3 khẳng định việc bảo vệ thiên kiến cá nhân làm cuộc họp kéo dài ít nhất 20 phút; rất hoan nghênh bảng ma trận trade-off độc lập | 1/3 cảnh báo: nếu AI đưa ra kết luận "nên chọn phương án A" sẽ gây tự ái và phản ứng ngược từ phía người ủng hộ phương án B |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**
- **Tuyệt đối không để AI kết luận thay:** AI chỉ sinh bảng so sánh đối chiếu đa chiều (Pros / Cons / Trade-off Matrix) và đặt câu hỏi gợi mở, để quyền quyết định 100% cho con người.
- **Bổ sung ràng buộc ngữ cảnh:** Cho phép nạp context ngắn về ràng buộc dự án (deadline gấp hay không, ngân sách server bao nhiêu) trước khi AI phân tích.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **Otter.ai / Fireflies.ai** | [Otter Insights](https://help.otter.ai/hc/en-us/articles/17332984641047-Otter-Insights-for-Enterprise), [Fireflies API](https://fireflies.ai/api), [Fireflies AI Apps](https://fireflies.ai/blog/fireflies-ai-apps) | Tạo bản chép lời, tóm tắt và ghi lại việc cần làm | Otter Enterprise có các mục quyết định và rủi ro tùy biến. Fireflies cho lấy transcript qua API và tùy biến nội dung tóm tắt. | Chưa thử trên cùng một transcript RFC để xem đầu ra có so sánh đủ các phương án theo ràng buộc kỹ thuật của nhóm hay không. | Tận dụng bản chép lời có sẵn và dùng công cụ hiện có làm mốc so sánh trước khi mở rộng PoC. |
| **Granola.ai** | [Granola](https://www.granola.ai/) | Bổ sung ghi chú cuộc họp từ nội dung đã ghi nhận | Người dùng có thể xem ghi chú đã được bổ sung và dùng chúng để rà lại nội dung buổi họp. | Cần thử xem ghi chú có giữ đủ luận điểm trái chiều để người điều phối đối chiếu hay không. | Cho người điều phối rà lại đầu ra cạnh bản chép lời và ghi chú gốc. |
| **Architecture Decision Records (ADR)** | [ADR](https://adr.github.io/) | Ghi lại bối cảnh, quyết định kiến trúc và hệ quả | Mẫu Markdown giúp lưu quyết định và lý do cùng dự án. | ADR là mẫu tài liệu. Người phụ trách vẫn cần kiểm tra lý do và ghi quyết định thực tế. | Dùng bảng trade-off đã duyệt làm đầu vào cho ADR. Nhóm tự ghi phương án được chọn và lý do. |

**Kết luận research.** PoC tập trung vào bảng so sánh có thể đối chiếu với bản chép lời, gồm phương án, ưu nhược điểm và các đánh đổi theo ràng buộc dự án. Dùng cùng một bản chép lời đã ẩn dữ liệu nhạy cảm để so sánh Copilot với bảng do người điều phối tự điền và, nếu có quyền dùng, mẫu tùy biến của công cụ hiện có. Chấm các đầu ra theo mục 7 để xác định còn phần việc nào cần tự xây.

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ:

```text
HIỆN TẠI — 85 phút/buổi họp RFC/Design Review

[1. Trình bày đề xuất: 20'] 
  → [2. Tranh luận phản biện tự do: 25'] 
  → [3. Bế tắc vì cái tôi / thiên kiến xác nhận: 25'] ← BOTTLENECK CHÍNH
  → [4. Ghi chép biên bản dở dang, thiếu trade-off: 10'] 
  → [5. Chốt quyết định cảm tính hoặc theo người nói to nhất: 5']
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Người đề xuất (Dev/PM) | Slide, tài liệu RFC sơ bộ | Phần trình bày ý tưởng | 20 phút / buổi họp | Trình bày thuận lợi, thường che giấu nhược điểm |
| 2 | Cả nhóm | Câu hỏi phản biện | Tranh luận nhiều chiều | 25 phút / buổi họp | Bắt đầu xuất hiện các quan điểm trái chiều |
| 3 | Cả nhóm | Quan điểm cá nhân | Bế tắc, tranh cãi lòng vòng | **25 phút / buổi họp** | **BOTTLENECK:** Ai cũng muốn phương án mình thắng, không chịu nhận hạn chế |
| 4 | Người ghi chép (Note-taker) | Diễn biến cuộc họp | Biên bản sơ sài, rời rạc | 10 phút / buổi họp | Thường bỏ sót các lý do vì sao bác bỏ một ý tưởng |
| 5 | Tech Lead / Cả team | Cảm xúc mệt mỏi sau tranh cãi | Quyết định cảm tính | 5 phút cuối | Chọn phương án theo người nói to/sếp áp đặt |

**Bottleneck chính:** Bước 3 — Tranh cãi bế tắc kéo dài 20–30 phút mà không đi đến đâu vì thiếu một góc nhìn đối chiếu khách quan và minh bạch.

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

Sơ đồ:

```text
TƯƠNG LAI — 45 phút/buổi họp (Tiết kiệm ~40 phút)

[1. Trình bày đề xuất: 20']                   ← CON NGƯỜI
  → [2. Tranh luận & ghi nhận transcript: 15'] ← CON NGƯỜI + STT Tool
  → [3. Phân loại & sinh Ma trận Trade-off: 2']← AI COPILOT (Rule trích xuất + LLM phân tích)
  → [4. Review ma trận & Biểu quyết: 5']       ← CON NGƯỜI (HITL - Boundary: Con người chốt)
  → [5. Tự động xuất file ADR lưu Git: 3']      ← RULE / SCRIPT AUTOMATION

Phương án quay về: Nếu AI phân tích lệch ngữ cảnh → Facilitator dùng bảng trắng thủ công như cũ.
```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | 5 bước | 5 bước (chuẩn hóa luồng dữ liệu) | Quy trình mạch lạc, rõ ràng |
| Tổng thời gian | 85 phút | 45 phút | **Giảm 47% thời gian họp** |
| Thời gian tranh cãi bế tắc | 25 phút | Dưới 5 phút | Giải quyết ngay bằng ma trận trực quan |
| Số bước thủ công | 5 bước | 2 bước thảo luận người thật | Giảm tải việc ghi chép và tổng hợp |
| Bottleneck chính | Bế tắc bảo vệ thiên kiến (25') | Đọc và xác nhận ma trận (5') | Chuyển từ xung đột sang đánh giá dữ liệu |
| Rủi ro mới phát sinh | Quyết định cảm tính, mất đoàn kết | AI có thể tóm tắt thiếu context ngầm | Xử lý bằng Human-in-the-loop (con người review) |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | Software Engineers, Tech Lead và Product Manager trong các nhóm phát triển sản phẩm kỹ thuật (4–8 người). |
| **Quy trình** | Tham gia các buổi họp Design Review/RFC Review định kỳ: Trình bày đề xuất $\rightarrow$ Tranh luận $\rightarrow$ Bế tắc bảo vệ quan điểm $\rightarrow$ Ghi biên bản $\rightarrow$ Chốt giải pháp. |
| **Bottleneck** | Bước tranh cãi bế tắc kéo dài 20–30 phút/buổi do các thành viên mắc bẫy thiên kiến xác nhận, bảo vệ cái tôi cá nhân thay vì nhìn vào dữ kiện khách quan. |
| **Impact** | Lãng phí 2–4 giờ công (man-hours) của cả nhóm mỗi tuần; nguy cơ chọn sai kiến trúc dẫn đến việc phải đập đi xây lại tốn hàng tuần dev; gây căng thẳng tâm lý nội bộ. |
| **Success Metric** (baseline → target, cách đo) | - Baseline: 25 phút tranh cãi bế tắc/buổi; 0 bảng trade-off có cấu trúc sau họp.<br>- Target: Giảm thời gian bế tắc xuống dưới 8 phút; 100% cuộc họp có bảng ma trận trade-off chuẩn hóa.<br>- Cách đo: Bấm giờ thực tế trong 4 buổi họp liên tiếp và khảo sát mức độ hài lòng về tính minh bạch của quyết định. |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | - AI tuyệt đối không tự đưa ra quyết định chọn phương án nào thay cho nhóm.<br>- AI không ngắt lời khi các thành viên đang tranh luận tự nhiên.<br>- Bắt buộc phải có con người (Tech Lead/Team) kiểm tra và duyệt lại các tiêu chí đánh đổi trước khi biểu quyết. |

Phản biện nhận được (từ AI và các thành viên):
- *Phản biện:* "Metric ban đầu 'hết 100% tranh cãi' là phi lý vì tranh luận kỹ thuật là cần thiết."
- *Đồng ý & Đã sửa:* Nhóm đồng ý và sửa lại thành "cắt giảm thời gian tranh luận bế tắc từ 25' xuống dưới 8'".

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô: **Độ mơ hồ Trung bình — Độ phức tạp Cao**.

Vì sao:
- **Độ mơ hồ Trung bình:** Luồng tranh luận bằng ngôn ngữ tự nhiên có nhiều cách diễn đạt khác nhau, nhưng mục tiêu cuối cùng rất cụ thể: tìm ra ưu điểm, nhược điểm và sự đánh đổi giữa các phương án theo các tiêu chí kỹ thuật rõ ràng (performance, complexity, cost, time-to-market).
- **Độ phức tạp Cao:** Cần khả năng hiểu ngữ cảnh sâu (deep semantic understanding), nhận diện được đâu là sự thật (fact) và đâu là cảm tính (bias), đồng thời tổng hợp từ nhiều ý kiến rời rạc thành bảng ma trận so sánh logic.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | Bắt buộc điền template RFC và bảng Pros/Cons bằng tay trước khi họp | Đủ khi mọi người cực kỳ kỷ luật và khách quan | Người làm thường chỉ ghi ưu điểm của mình, lười điền nhược điểm; không xử lý được tranh cãi phát sinh trong buổi họp | Không |
| **Rule** | Dùng script đếm từ khóa, phân loại câu hỏi/câu khẳng định | Đủ khi dữ liệu đầu vào có cấu trúc cố định | Không hiểu được ngữ nghĩa phản biện, không phân tích được trade-off phức tạp | Không |
| **Workflow** | Chuyển Speech-to-Text $\rightarrow$ Script trích xuất câu $\rightarrow$ Template cố định | Đủ để làm biên bản tóm tắt cuộc họp thông thường | Đầu ra thô cứng, không bóc tách được các cặp trade-off đối lập giữa các giải pháp | Không |
| **Agent / Copilot** | Agent phân tích transcript, bóc tách luận điểm, đối chiếu tiêu chí và sinh ma trận trade-off có con người kiểm duyệt | Đủ cho việc xử lý hội thoại tự do và lập luận đa chiều | Có thể tóm tắt thiếu ý ngầm hoặc hiểu sai thuật ngữ nội bộ (khắc phục bằng HITL) | **CHỌN (Copilot)** |

**Mức chọn:** **AI Copilot (Workflow kết hợp Agent có Human-in-the-loop)**.

**Vì sao không chọn mức đơn giản hơn:** Các mức No-AI và Rule không thể hiểu được ngữ nghĩa của các cuộc tranh luận tự do và không có khả năng suy luận để chỉ ra trade-off logic giữa hai giải pháp công nghệ.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | Trích xuất các phương án được đề xuất (Option A, Option B), danh sách luận điểm ủng hộ/phản đối và sinh Ma trận Trade-off theo 4 trục: Độ phức tạp, Thời gian triển khai, Chi phí vận hành, Khả năng mở rộng. |
| **Judgment** — con người cân nhắc, quyết định gì? | Đánh giá xem bảng trade-off AI đưa ra có phản ánh đúng thực tế dự án không; gán trọng số ưu tiên cho từng tiêu chí và biểu quyết chọn giải pháp cuối cùng. |
| **Action** — hành động cuối cùng là gì, ai làm? | Tech Lead bấm xác nhận quyết định; hệ thống tự động xuất file Architecture Decision Record (ADR) lên kho Git của dự án. |
| **Outcome** — đo kết quả bằng gì? | Giảm thời gian họp tranh luận từ 25' xuống < 8'; 100% cuộc họp có biên bản trade-off; độ hài lòng của team đạt $\ge 4.2/5$. |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | Text transcript buổi thảo luận (từ Google Meet/Zoom/Teams); tóm tắt ngắn về ngữ cảnh dự án (ngân sách, timeline). Dữ liệu này luôn sẵn có trong mỗi buổi họp. |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | Đánh giá 1–5 sao của team về độ chuẩn xác của ma trận; các chỉnh sửa trực tiếp của con người trên ma trận sẽ làm dữ liệu fine-tune prompt. |

### 6.4. Hai câu hỏi của Google PAIR

- **Người dùng muốn được hỗ trợ (augment) hay giao hẳn việc (automate)?**  
  **Augment (Hỗ trợ).** Bằng chứng: Phỏng vấn 3/3 kỹ sư và Tech Lead đều khẳng định họ không bao giờ để một cỗ máy AI quyết định thay kiến trúc hệ thống của họ. Họ chỉ cần AI làm "thư ký khách quan" tổng hợp và mổ xẻ trade-off để họ đưa ra quyết định sáng suốt hơn.
- **AI sai kiểu nào tệ hơn, báo nhầm (False Positive) hay bỏ sót (False Negative)?**  
  **Bỏ sót (False Negative) tệ hơn.** Vì nếu AI bỏ sót một nhược điểm chí mạng (critical risk/trade-off) của một giải pháp (ví dụ: rò rỉ bảo mật hoặc chi phí cloud đột biến), team có thể chọn nhầm giải pháp thảm họa. Thiết kế đã xử lý bằng cách luôn có cột *"Các câu hỏi mở/Rủi ro chưa được làm rõ"* để bắt buộc con người đối chất trước khi biểu quyết.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Software Engineers, Tech Lead và Product Manager trong các nhóm sản phẩm công nghệ (4–8 người). |
| **Quy trình** | Chu trình review giải pháp kỹ thuật: Trình bày đề xuất (20') $\rightarrow$ Tranh luận tự do (15') $\rightarrow$ Sinh ma trận trade-off (2') $\rightarrow$ Con người kiểm duyệt & Biểu quyết (5') $\rightarrow$ Tự động lưu ADR (3'). |
| **Bottleneck** | Tranh cãi bế tắc do thiên kiến cá nhân và thiếu cái nhìn đa chiều về trade-off (trước đây mất 25 phút/buổi). |
| **Impact** | Lãng phí 2–4 man-hours mỗi buổi họp; chọn sai công nghệ dẫn đến nợ kỹ thuật (technical debt) tốn hàng tuần refactor; giảm gắn kết nội bộ. |
| **Success Metric** (baseline → target, cách đo) | - Thời gian tranh luận bế tắc giảm từ 25 phút xuống dưới 8 phút/buổi.<br>- Tỷ lệ tạo biên bản trade-off chuẩn hóa đạt 100% sau buổi họp (so với baseline 0%).<br>- Đo bằng bấm giờ 4 buổi họp thử nghiệm và khảo sát độ tin cậy quyết định đạt $\ge 4.2/5$. |
| **Boundary** | AI không được tự ý chốt quyết định; không can thiệp real-time bằng giọng nói ngắt lời họp; chỉ sinh ma trận khi được yêu cầu; bắt buộc con người xác nhận trước khi lưu ADR. |
| **AI intervention point** | Tại thời điểm kết thúc phiên tranh luận tự do (phút thứ 35 của cuộc họp), AI nhận transcript văn bản và sinh bảng ma trận so sánh trade-off đa chiều. |
| **Mức chọn** | **AI Copilot (Workflow + LLM Agent có Human-in-the-loop)**. |
| **Rủi ro & người kiểm tra** | Rủi ro hiểu sai biệt ngữ kỹ thuật nội bộ; người kiểm tra là Tech Lead và các bên đề xuất. |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| Quy trình | Chưa định rõ thời điểm AI can thiệp | Xác định rõ AI can thiệp ở phút 35 sau tranh luận tự do | Tránh làm phiền dòng tư duy tự nhiên của kỹ sư khi họp |
| AI intervention point | Chưa có | Điểm can thiệp cố định: Text transcript $\rightarrow$ Trade-off matrix | Đảm bảo tính khả thi kỹ thuật, không phụ thuộc audio real-time |
| Mức can thiệp | Ghi chung chung là "Agent" | Xác định chuẩn xác: "AI Copilot có Human-in-the-loop" | Phù hợp nguyên tắc Google PAIR (Augment, không Automate) |

**Tiêu chí đánh giá đầu ra của AI (3 tiêu chí cốt lõi):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | **Tính đầy đủ của Phương án (Completeness)** | Liệt kê đầy đủ 100% các phương án và luận điểm chính đã được phát biểu trong cuộc họp. | Bỏ sót phương án của thành viên hoặc bỏ quên các phản biện quan trọng. |
| 2 | **Tính khách quan & Đối xứng (Objectivity & Symmetry)** | Mỗi phương án đều phải chỉ ra ít nhất 1 ưu điểm và 1 nhược điểm/trade-off rõ ràng dựa trên dữ kiện. | Thiên vị lộ liễu cho 1 phương án; chỉ nêu ưu điểm mà giấu nhược điểm. |
| 3 | **Không ảo giác (Hallucination-free)** | Các luận điểm trong ma trận phải trích xuất đúng từ transcript hoặc suy luận logic từ ràng buộc dự án. | Bịa đặt thêm các con số đo lường hoặc tính năng không hề được đề cập. |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | **Thấp** trong phạm vi PoC | Mục 3.2 có ví dụ buổi họp mất thời gian khi so sánh các phương án. Pilot cần kiểm tra bảng có giúp người tham gia thấy rõ các đánh đổi hay không. |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | **Thấp** trong phạm vi PoC | Người điều phối có thể rà từng dòng trong bảng Markdown. Bấm giờ từ lúc nhận bảng đến lúc duyệt xong để biết công chỉnh sửa thực tế. |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | **Trung bình** | Dùng bản chép lời để giảm phạm vi kỹ thuật. Bản chép lời có thể sai thuật ngữ hoặc thiếu ngữ cảnh, nên cần đối chiếu đầu ra với bản gốc và ràng buộc dự án. |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | **Thấp** với dữ liệu giả lập | Bắt đầu bằng RFC giả lập. Chỉ dùng dữ liệu thật khi được phép và đã xử lý thông tin nhạy cảm. Ghi chi phí thực tế theo lượt chạy trước khi đề xuất triển khai rộng hơn. |

### 8.2. Kết luận

**Quyết định:** **GO**

**Lý do.** Thử nghiệm nhỏ có thể kiểm tra trực tiếp chất lượng bảng và công rà soát. Copilot chỉ xử lý bản chép lời khi được yêu cầu sau phiên tranh luận. Người điều phối kiểm tra đầu ra và nhóm giữ quyền chốt phương án.

**Phạm vi PoC.** Chạy thử trước với một bản chép lời RFC giả lập có ba người thảo luận hai phương án. Workflow nhận bản chép lời và ràng buộc dự án, tóm tắt luận điểm, tạo bảng Markdown rồi chuyển cho người điều phối đối chiếu. Sau khi nhóm quyết định, người phụ trách mới cập nhật ADR. Trong ba buổi pilot, áp dụng tiêu chí ở mục 7, ghi thời gian rà và sửa bảng cho từng buổi, đồng thời hỏi mỗi người đánh giá bảng có phản ánh đúng các đánh đổi chính hay không.

**Ngưỡng dừng.** Sau 3 buổi pilot, dừng nếu tỷ lệ phản hồi đồng tình trên tổng số phản hồi hợp lệ **dưới 60%**, hoặc có bảng mất **hơn 12 phút** để rà và chỉnh sửa. Khi đó, người điều phối quay về điền bảng mẫu Notion. Mục tiêu giảm thời gian bế tắc xuống dưới 8 phút vẫn được theo dõi riêng theo cách đo ở mục 7.

---

## 9. Hạn chế và hướng tiếp theo

- **Hạn chế:**
  - Chưa xử lý được triệt để các ngữ cảnh ngầm (context không nói ra thành lời, chỉ hiểu ngầm trong văn hóa team).
  - Phụ thuộc vào chất lượng của công cụ chuyển đổi giọng nói thành văn bản (Speech-to-Text). Nếu STT sai tên biến hoặc thuật ngữ chuyên ngành, AI có thể phân tích lệch.
- **Hướng tiếp theo:**
  - Bổ sung tính năng cho phép nạp tài liệu thiết kế (PRD/RFC draft) làm ngữ cảnh nền tảng trước cuộc họp.
  - Tích hợp bot trực tiếp vào kênh Slack/Discord của team để sau cuộc họp bot tự động push bản draft ADR cho các thành viên react biểu quyết.

---

## 10. Tài liệu tham khảo

- Lean UX Framework: Jeff Gothelf & Josh Seiden.
- Google People + AI Research (PAIR) Guidebook: https://pair.withgoogle.com/
- Teresa Torres, *Continuous Discovery Habits* (Opportunity Solution Tree).
- Rob Fitzpatrick, *The Mom Test: How to talk to customers & learn if your business is a good idea when everyone is lying to you*.
- Michael Nygard, *Documenting Architecture Decisions (ADR)*: https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions
- Thị trường công cụ AI Meeting: Otter.ai, Fireflies.ai, Granola.ai.
