# Báo cáo cá nhân — 2A202603392_NguyenTuanQuang

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên:Nguyễn Tuấn Quang
- MSSV:2A202603392
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm:tido
- Link repo nhóm:https://github.com/datnguyen101004/K5-L3A-DAY02-tido-DiscoveryProblemFraming.git

---

## 2. Scan problem (CP1)    

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại, tốn thời gian | Khi firmware lỗi ở UART, I2C, SPI, ADC hoặc FreeRTOS, tôi muốn khoanh vùng nguyên nhân theo từng bước, để không lặp lại các phép kiểm tra đã làm. | Tôi và người cùng làm dự án firmware | Ước tính 3–6 giờ/lần, 2–3 lần/tuần; bước kiểm tra phần cứng và thêm log thường lặp lại. |
| 2 | Lặp lại | Khi ứng tuyển vị trí Embedded Firmware mới, tôi muốn chọn và diễn đạt kinh nghiệm phù hợp, để CV một trang rõ kết quả và trung thực. | Tôi; người tuyển dụng | Ước tính 1–2 giờ/bản, 3–5 bản/tháng; gần như viết lại mô tả dự án mỗi lần. |
| 3 | Tốn thời gian | Khi chuẩn bị phỏng vấn embedded bằng tiếng Anh, tôi muốn diễn đạt chính xác dự án và thuật ngữ kỹ thuật, để trả lời mạch lạc. | Tôi; người phỏng vấn | Ước tính ôn 1–2 giờ/ngày; thường viết lại câu trả lời cho từng dự án. |
| 4 | Cần đọc, tổng hợp nhiều thông tin | Khi viết báo cáo đồ án, tôi muốn nối thuật toán, sơ đồ khối và kết quả đo thành lời giải thích rõ ràng, để người đọc đánh giá được hệ thống. | Tôi; giảng viên | Ước tính 4–8 giờ/chương, theo từng đợt đồ án. |
| 5 | Tốn thời gian | Khi hoàn thành một vòng thiết kế PCB, tôi muốn phát hiện lỗi footprint, nguồn và routing, để tránh phải sửa và layout lại. | Tôi; người cùng làm PCB | Ước tính 6–10 giờ/vòng, 1–2 vòng/dự án. |
| 6 | Cần đọc, tổng hợp nhiều thông tin | Khi cấu hình ngoại vi vi điều khiển, tôi muốn tìm đúng thông tin thanh ghi, timing và errata, để kiểm tra cấu hình trước khi debug tiếp. | Tôi; người cùng làm firmware | Ước tính 1–3 giờ/lần, 2–3 lần/tuần; tài liệu có thể dài hàng trăm trang. |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Tôi tự liệt kê sáu vấn đề từ nhật ký công việc; AI hỗ trợ chuyển ghi chú thành Job Story, không gợi ý thêm vấn đề mới. Thời gian và tần suất đều là ước tính ban đầu, cần kiểm lại bằng ghi chép ở các lần làm tiếp theo.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Debug firmware | Xảy ra thường xuyên, tốn nhiều thời gian và có các bước kiểm tra quan sát được. | Chưa đo thời gian thực tế từng bước và số vòng kiểm tra lặp lại. |
| 2 | Ôn phỏng vấn embedded bằng tiếng Anh | Quy trình lặp lại hằng ngày; bước viết câu trả lời cho mỗi dự án khá rõ. | Chưa biết viết hay luyện nói ảnh hưởng nhiều hơn tới chất lượng trả lời. |
| 3 | Viết CV và mô tả dự án | Lặp lại theo mỗi vị trí ứng tuyển; bước viết bullet chiếm nhiều thời gian nhất. | Chưa biết tái sử dụng được bao nhiêu mà vẫn phù hợp và trung thực. |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi firmware lỗi ở UART, I2C, SPI, ADC hoặc FreeRTOS, tôi muốn khoanh vùng nguyên nhân theo từng bước, để không lặp lại các phép kiểm tra đã làm. |
| Actor | Tôi, sinh viên phát triển firmware cho dự án embedded. |
| Thời điểm / bối cảnh | Khi ngoại vi không hoạt động, ADC nhiễu hoặc tác vụ FreeRTOS treo. |
| Quy trình hiện tại (3–7 bước) | 1. Tái hiện lỗi → 2. Kiểm tra phần cứng → 3. Thêm log hoặc dùng debugger → 4. Đối chiếu datasheet/errata → 5. Sửa, nạp lại và kiểm thử. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2–3 thường phải lặp; riêng bước 3 ước tính 60–120 phút cho một lượt. |
| Impact (nếu không giải thì sao) | Một ca debug ước tính 3–6 giờ; bỏ sót phép kiểm tra cơ bản có thể khiến tôi sửa sai hướng. |
| Success metric (baseline → target) | Tổng thời gian tạm tính 3–6 giờ/ca. Ghi số lần phải làm lại một phép kiểm tra vì chưa lưu kết quả ở ít nhất 3 ca để lập baseline. Mục tiêu thử nghiệm là giảm ít nhất 1 lần kiểm tra lặp lại mỗi ca, tính trung bình trên 3 ca tương tự có dùng checklist và sổ log. |
| Phương án không dùng AI | Checklist theo loại lỗi và nhật ký các phép đo đã làm. |
| Giả thuyết về AI (nếu có) | AI phản biện giả thuyết nguyên nhân dựa trên triệu chứng và log; mọi gợi ý phải được kiểm bằng phép đo. |
| Cảm nhận nhanh | Chưa biết; thử checklist và nhật ký trước. |

Quy trình nháp hiện tại:

```text
[Tái hiện lỗi: 20–30'] → [Kiểm tra phần cứng: 30–60']
→ [Thêm log / debugger: 60–120'] ← BƯỚC TỐN NHIỀU THỜI GIAN
→ [Đối chiếu datasheet / errata: 30–60'] → [Sửa, nạp lại, kiểm thử: khoảng 30']
Bước 2–3 có thể lặp nhiều vòng; các mốc trên là ước tính cho một lượt.
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi chuẩn bị phỏng vấn embedded bằng tiếng Anh, tôi muốn diễn đạt chính xác dự án và thuật ngữ kỹ thuật, để trả lời mạch lạc. |
| Actor | Tôi, ứng viên vị trí Embedded Firmware. |
| Thời điểm / bối cảnh | Khi ôn các câu hỏi về dự án ESP32 air purifier, S32K144 CAN và kiến thức embedded. |
| Quy trình hiện tại (3–7 bước) | 1. Chọn chủ đề → 2. Viết câu trả lời tiếng Anh → 3. Kiểm tra ý và thuật ngữ → 4. Luyện nói, ghi âm, nghe lại → 5. Sửa ngữ pháp và phát âm. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2: thường viết lại từ đầu, ước tính 30–40 phút/chủ đề. |
| Impact (nếu không giải thì sao) | Tôi ôn khoảng 1–2 giờ/ngày; thời gian viết lại làm giảm thời gian luyện nói. |
| Success metric (baseline → target) | Baseline tạm tính 30–40 phút viết/chủ đề; thử giảm xuống dưới 20 phút bằng bộ ý tái sử dụng, đồng thời vẫn giải thích được khi không nhìn bản viết. Đo bằng đồng hồ và ghi âm. |
| Phương án không dùng AI | Ngân hàng ý, thuật ngữ và ví dụ dự án; cấu trúc câu trả lời thống nhất. |
| Giả thuyết về AI (nếu có) | AI đặt câu hỏi tiếp nối hoặc góp ý cách diễn đạt; tôi tự kiểm tra nội dung kỹ thuật. |
| Cảm nhận nhanh | Chưa biết; thử bộ ý và cấu trúc trả lời trước. |

Quy trình nháp hiện tại:

```text
[Chọn dự án / chủ đề: 10'] → [Viết câu trả lời tiếng Anh: 30–40'] ← BOTTLENECK
→ [Kiểm tra ý và thuật ngữ: 15'] → [Luyện nói, ghi âm, nghe lại: 20–30']
→ [Sửa ngữ pháp, phát âm: 15']
Các mốc thời gian là ước tính.
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi ứng tuyển vị trí Embedded Firmware mới, tôi muốn chọn và diễn đạt kinh nghiệm phù hợp, để CV một trang rõ kết quả và trung thực. |
| Actor | Tôi, ứng viên vị trí Embedded Firmware. |
| Thời điểm / bối cảnh | Mỗi khi đọc mô tả công việc mới và chuẩn bị CV tương ứng. |
| Quy trình hiện tại (3–7 bước) | 1. Đọc mô tả công việc → 2. Chọn dự án phù hợp → 3. Viết lại bullet theo kết quả có thật → 4. Cắt gọn một trang, kiểm tra khả năng đọc và tính trung thực. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: viết lại bullet, ước tính 40 phút/bản. |
| Impact (nếu không giải thì sao) | Một bản CV ước tính 1–2 giờ; thường làm 3–5 bản/tháng. |
| Success metric (baseline → target) | Baseline tạm tính 40 phút viết bullet/bản; thử giảm xuống dưới 25 phút bằng thư viện bullet đã kiểm chứng. Đo trên 3 lần ứng tuyển tiếp theo. |
| Phương án không dùng AI | Thư viện bullet theo dự án, kèm bằng chứng cho số liệu; checklist CV một trang. |
| Giả thuyết về AI (nếu có) | AI góp ý cách diễn đạt ngắn, rõ; không tự thêm kỹ năng hay kết quả chưa có. |
| Cảm nhận nhanh | No AI hoặc Workflow; chưa chốt trước khi thử thư viện bullet. |

Quy trình nháp hiện tại:

```text
[Đọc mô tả công việc: 15'] → [Chọn dự án: 15']
→ [Viết lại bullet: 40'] ← BOTTLENECK
→ [Cắt gọn, kiểm tra khả năng đọc và tính trung thực: 20']
Các mốc thời gian là ước tính.
```

### Card muốn pitch nhất

- Card số: 1 — Debug firmware.
- Vì sao: Xuất hiện nhiều lần mỗi tuần, có quy trình quan sát được và có thể bắt đầu bằng checklist cùng nhật ký debug.
- Câu hỏi muốn nhóm phản biện: Bước gây mất thời gian nhất là dùng debugger, hay là việc tôi phải quay lại các phép kiểm tra vì chưa ghi rõ mình đã thử gì?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Thời gian 3–6 giờ/ca và thời gian từng bước đều là ước tính; nhiều vòng lặp khiến không thể cộng thời gian một lượt thành tổng thời gian chắc chắn. | Đồng ý | Ghi rõ baseline tạm tính và đề xuất theo dõi ít nhất ba ca debug. |
| “Debug firmware” gồm nhiều loại lỗi, quá rộng cho một buổi lab. | Đồng ý | Khi pitch, đề xuất nhóm thu hẹp vào một loại lỗi nếu chọn card này. |
| Checklist và nhật ký có thể giảm kiểm tra lặp lại trước khi cần AI. | Đồng ý | Giữ phương án không dùng AI và chưa chốt mức can thiệp. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Trình bày ba card: debug firmware, ôn phỏng vấn embedded bằng tiếng Anh và viết CV. | Cả ba được ghi trong bảng pitch của báo cáo nhóm; card debug firmware được đưa vào thảo luận. |
| Phản biện bài của bạn khác | Theo bảng pitch nhóm, tôi hỏi Đạt: “Nếu AI chen ngang ngắt lời real-time khi mọi người đang nói thì có gây ức chế và ngắt mạch họp không?”; hỏi Toàn: “Tần suất vào project mới của một dev thấp, tổng impact cả năm có đủ lớn không?” | Câu hỏi thứ nhất đặt vấn đề về trải nghiệm họp và boundary; câu thứ hai yêu cầu kiểm tra impact theo tần suất thực tế. |
| Nhận phản biện | Đạt hỏi liệu sổ log đã đủ để xử lý việc kiểm tra lặp lại khi nhiều lỗi đến từ phần cứng. Toàn hỏi bài ôn phỏng vấn khác gì so với công cụ có sẵn. Đạt cũng hỏi liệu thư viện bullet mẫu đã đủ cho bài viết CV. | Card debug ưu tiên thử checklist và sổ log. Card phỏng vấn có phương án tái sử dụng bộ ý và thuật ngữ. Card CV có phương án thử thư viện bullet và checklist trước khi cân nhắc AI. |
| Gom cluster / cây OST | Được phân công hỗ trợ CP3: xem các candidate theo actor, pain và outcome để góp ý khi nhóm gom cluster và dựng OST. | Phần nhóm do Đạt phụ trách chính; kết quả chính thức nằm ở mục 2 báo cáo nhóm. |
| Chọn candidate problem | Hỗ trợ CP3 bằng cách đối chiếu card của mình với candidate của Đạt và Toàn theo bottleneck, bằng chứng và tính vừa sức lab. | Nhóm chọn candidate về bế tắc khi so sánh phương án trong họp kỹ thuật; không chọn ba card embedded của tôi. |
| Kiểm chứng / research | Phụ trách CP4 Research: đối chiếu Otter.ai, Fireflies.ai, Granola.ai và mẫu ADR; kiểm tài liệu chính thức về transcript, tóm tắt, action items và tùy biến. | Nhóm chọn tận dụng transcript có sẵn, tập trung PoC vào bảng trade-off và định dạng ADR. Khả năng công cụ hiện có xử lý trade-off vẫn cần thử trực tiếp. |
| Quy trình nhóm | Được phân công hỗ trợ CP5: rà soát quy trình trước/sau, nhất là bước lấy transcript, lập bảng trade-off và người kiểm tra. | Đạt phụ trách sơ đồ chính; báo cáo nhóm giữ quyết định cuối cho con người và có phương án quay về. |
| Problem Statement | Được phân công hỗ trợ CP5 Problem Statement v0 và CP6 v1: đối chiếu actor, bottleneck, metric và boundary với phần research. | Đạt phụ trách v0, Toàn phụ trách v1; bản nhóm bổ sung điểm AI can thiệp và người kiểm tra. |
| Mức can thiệp AI | Được phân công hỗ trợ CP6: xem xét No AI, Rule, Workflow và Agent cùng các tiêu chí eval. | Toàn phụ trách chính; phương án nhóm là Copilot/Workflow có người duyệt trước quyết định. |
| Quyết định | Phụ trách CP6 Quyết định: tổng hợp bốn rủi ro Value, Usability, Feasibility, Viability và đề xuất ngưỡng dừng cho pilot. | Báo cáo nhóm chốt Go với PoC xử lý transcript và người kiểm tra. Dừng sau 3 buổi pilot nếu mức đồng tình với bảng trade-off dưới 60% hoặc thời gian sửa vượt 12 phút; quay về facilitator và bảng mẫu. Các mức rủi ro và ước tính chi phí trong báo cáo nhóm cần được kiểm chứng khi pilot. |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Nhờ AI chuyển sáu việc tôi đã ghi trong nhật ký thành Job Story. | Giúp mô tả tình huống, động cơ và kết quả mong muốn theo đúng mẫu. | Các mốc thời gian trong nhật ký chỉ là ước tính; AI không thể biến chúng thành số đo đã kiểm chứng. | Tôi giữ nhãn “ước tính”, không thêm vấn đề hay bằng chứng ngoài nhật ký. |
| CP2 Problem Card | Nhờ AI sắp xếp ba việc tôi ưu tiên thành Problem Card và phản biện card debug firmware. | Chỉ ra phạm vi “debug firmware” còn rộng, thời gian từng bước chưa được đo và checklist có thể là phương án đơn giản hơn. | AI chưa có log thực tế của các ca debug nên chưa xác nhận được bottleneck hay target theo phút. | Tôi giữ mức can thiệp ở “Chưa biết” và đề xuất ghi thời gian của ít nhất ba ca trước khi chốt target. |
| CP4 Research | Dùng AI hỗ trợ xác định các công cụ họp cần đối chiếu; sau đó kiểm tài liệu chính thức của Otter.ai và Fireflies.ai. | Giúp lập danh sách chức năng cần so sánh: transcript, summary, action items và tùy biến. | Nhận định “các công cụ chỉ tóm tắt, không hỗ trợ quyết định” quá tuyệt đối: Otter có mục quyết định và insight tùy biến; Fireflies có summary tùy biến. | Chỉ ghi chức năng có nguồn xác nhận; giữ khả năng phân tích trade-off chuyên sâu là giả định cần thử, không khẳng định khoảng trống thị trường. |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | Dùng AI để phản biện bốn rủi ro và ngưỡng dừng của PoC xử lý transcript. | Nhắc kiểm tra phương án facilitator và bảng tiêu chí, cùng bước người duyệt đầu ra. | AI không có kết quả pilot để xác nhận mức rủi ro thấp hay chi phí ước tính trong báo cáo nhóm. | Ghi rõ quyết định Go là quyết định của nhóm và giữ ngưỡng dừng đo được: dưới 60% đồng tình hoặc sửa quá 12 phút sau 3 buổi. |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**



**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Khi nghe Toàn trình bày chuyện mất khoảng hai giờ để cấu hình một dự án mới, tôi hỏi một người thực sự gặp việc đó bao nhiêu lần trong năm. Hai giờ nghe có vẻ nhiều, nhưng nếu cả nhóm chỉ gặp vài lần thì mức ưu tiên có thể khác. Câu hỏi đó cũng áp dụng được cho card debug firmware của tôi. Tôi cần xem cả thời gian mỗi ca lẫn số ca phải quay lại kiểm tra cùng một bước.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Nhóm tôi đã bị "solution-first" ngay từ những phút đầu tiên khi thảo luận. Vừa nêu ra vấn đề tranh luận trong cuộc họp, gần như ngay lập tức cả nhóm đều nhảy vào hào hứng bàn về việc: "Mình sẽ dùng mô hình LLM nào? Dùng Whisper để nhận diện giọng nói hay dùng Claude để phân tích? Sẽ làm con bot Discord hay app riêng?". Chúng tôi đã cuốn vào giải pháp công nghệ suốt gần 15 phút mà quên mất việc đào sâu vào nguyên nhân gốc rễ: Tại sao mọi người lại bế tắc khi tranh luận? Bản chất là do thiếu thông tin hay do cái tôi cá nhân? Rất may, sau khi xem lại câu hỏi hướng dẫn trong worksheet về việc "Nếu không có AI thì giải quyết thế nào", nhóm đã kịp thời dừng lại. Chúng tôi tự chất vấn nhau: "Nếu chỉ dùng một facilitator người thật hoặc một bảng tính Excel liệt kê pros/cons thì đã giải quyết được bao nhiêu phần trăm vấn đề?". Nhờ câu hỏi này, nhóm đã kéo nhau trở lại thực tế, tập trung định nghĩa đúng quy trình As-Is và điểm nghẽn trước khi quay lại bàn về giải pháp AI.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Đạt hỏi tôi liệu một cuốn sổ log debug có đủ để giảm việc kiểm tra lặp lại không. Ví dụ, nếu tôi đã đo nguồn và kiểm tra pull-up thì ghi rõ kết quả có thể giúp lần sau biết nên kiểm tra tiếp ở đâu. Trong card hiện tại, tôi để mức can thiệp là “Chưa biết” và ưu tiên thử checklist cùng nhật ký debug. Tôi cần ghi lại vài ca thực tế để biết cách đó có giúp tiết kiệm thời gian không.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Ở phần research, nhận định ban đầu rằng các công cụ họp chỉ làm biên bản là quá rộng. Tài liệu của Otter có nhắc đến việc ghi nhận quyết định và tùy biến nội dung theo mẫu. Từ đó, câu hỏi cụ thể hơn là liệu bảng tạo từ bản chép lời có nêu đúng các đánh đổi kỹ thuật của từng phương án và có đủ căn cứ để người điều phối kiểm lại hay không. Muốn trả lời, nhóm cần thử trên cùng một bản chép lời.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Với phần việc Quyết định của tôi, chỗ khó là xác định thế nào thì tính là bế tắc. Hai người còn bất đồng vì đang đưa ra lý do mới thì cuộc tranh luận vẫn có ích. Nếu cả hai chỉ lặp lại ý cũ và nhóm chưa tiến gần hơn tới quyết định, đó mới là khoảng thời gian cần đo. Nhóm cần thống nhất cách ghi thời điểm bắt đầu và kết thúc thì mục tiêu từ 25 phút xuống dưới 8 phút mới so sánh được.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Tôi sẽ đề nghị thử cùng một bản chép lời theo hai cách: để người điều phối tự điền bảng mẫu và để người điều phối sửa bảng AI tạo. Tôi sẽ bấm giờ cả hai, rồi xem mỗi bảng có bỏ sót điểm đánh đổi nào ảnh hưởng đến quyết định không. Như vậy nhóm có dữ liệu để xem ngưỡng 12 phút chỉnh sửa có hợp lý và việc dùng AI có giảm công cho người điều phối hay không.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Trong các buổi họp bàn về đề xuất kỹ thuật hoặc sản phẩm, nhóm dễ mất thời gian khi mọi người bảo vệ phương án của mình mà chưa có tiêu chí chung để so sánh. Quy trình hiện tại là trình bày, phản biện rồi chốt phương án, trong đó bước so sánh ưu và nhược điểm có thể bế tắc khoảng 20–30 phút. Nhóm đặt mục tiêu giảm thời gian bế tắc xuống dưới 8 phút và có bảng trade-off theo mẫu sau mỗi buổi họp thử. Giải pháp là một AI Copilot chạy theo Workflow bán tự động, dùng bản chép lời để tóm tắt các luận điểm và tạo bảng trade-off khi được yêu cầu sau mỗi phiên tranh luận. Người điều phối đối chiếu và chỉnh bảng, còn các thành viên giữ quyền chốt phương án. Nhóm quyết định Go để thử một PoC xử lý văn bản trong phạm vi nhỏ. Sau ba buổi thử, nếu tỷ lệ đồng tình với bảng dưới 60% hoặc thời gian chỉnh sửa vượt 12 phút, nhóm quay về cách dùng bảng mẫu do người điều phối tự điền.

---

## 7. Tài liệu tham khảo

- [Otter.ai Help — Conversation Page Overview](https://help.otter.ai/hc/en-us/articles/5093228433687-Conversation-Page-Overview): transcript, summary và action items.
- [Otter.ai Help — Insights for Enterprise](https://help.otter.ai/hc/en-us/articles/17332984641047-Otter-Insights-for-Enterprise): quyết định, rủi ro và mục insight tùy biến; tính năng thuộc gói Enterprise.
- [Fireflies.ai — API](https://fireflies.ai/api): transcript, summary, action items và truy vấn dữ liệu cuộc họp.
- [Fireflies.ai — AI Apps](https://fireflies.ai/blog/fireflies-ai-apps): tùy biến phần tóm tắt cuộc họp.
