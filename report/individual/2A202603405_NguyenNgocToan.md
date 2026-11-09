# Báo cáo cá nhân — 2A202603405_NguyenNgocToan

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Ngọc Toàn
- MSSV: 2A202603405
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: tido
- Link repo nhóm: https://github.com/datnguyen101004/K5-L3A-DAY02-tido-DiscoveryProblemFraming/tree/main

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

> Số liệu là ước lượng của tôi theo trí nhớ (chưa bấm giờ). Sẽ đo lại khi kiểm chứng ở CP4.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Pain từ người khác · Tốn thời gian | Khi tôi hoặc một thành viên mới bắt đầu làm một project mới, tôi muốn chạy được project ở máy local ngay trong ngày đầu, để bắt tay vào task sớm mà không phải hỏi đi hỏi lại người cũ | SWE mới vào team hoặc đổi project; người cũ bị hỏi | Lần vào project gần nhất: khoảng nửa ngày (~4 giờ) từ lúc clone tới khi chạy được; kẹt nhiều nhất ở cấu hình biến môi trường/config (~2 giờ), phải hỏi người cũ giá trị config |
| 2 | Cần đọc, tổng hợp nhiều thông tin | Khi cần biết vì sao team chọn thiết kế hoặc cấu hình hiện tại, hoặc cần đúng bản tài liệu mới nhất, tôi muốn tìm ra nhanh trong chat, Drive và Jira, để không phải hỏi lại hoặc làm theo bản cũ | SWE; đồng nghiệp bị hỏi lại | 5–15 phút/lần, 1–2 lần/tuần (khoảng 5–30 phút/tuần); phải tìm ở 3 nơi: chat (Slack/Teams/Zalo), Google Drive/OneDrive, Jira/email |
| 3 | Lặp lại · Cần đọc, tổng hợp nhiều thông tin | Khi deadline bài tập và lab được thông báo rải rác trên LMS, email và Discord/Zalo, tôi muốn thấy mọi hạn nộp của tuần ở một chỗ, để không trễ hạn hoặc phải làm gấp sát giờ | Tôi và các bạn cùng lớp | Phải dò 3 nguồn; 0 lần trễ hoặc suýt trễ trong 1 tháng qua (**tín hiệu phản bác**: pain hiện tại nhỏ) |
| 4 | Lặp lại · Pain từ người khác | Khi đồng nghiệp mới, tester, PO hoặc khách hàng hỏi về cách dùng, cấu hình hay quy trình của phần hệ thống tôi phụ trách, tôi muốn họ tự tìm được câu trả lời đúng, để tôi không bị cắt ngang khi đang code | Tôi; người hỏi phải chờ câu trả lời | 6–10 câu/tuần, nhiều nhất từ Tester/QA; 25–50% là câu tôi đã từng trả lời; 5–15 phút/câu (khoảng 30–150 phút/tuần) |
| 5 | Lặp lại · Tốn thời gian | Khi tôi mở PR cho một task đã xong, tôi muốn có người review sớm, để merge kịp sprint và không phải chuyển qua lại giữa task cũ và task mới | Tôi, reviewer, tiến độ sprint | Thường có review đầu tiên trong vòng 4 giờ (**tín hiệu phản bác**: team review nhanh, pain nhỏ) |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Cả 5 ý trên được chọn từ danh sách khoảng 15 vấn đề do tôi và AI (Claude) gợi ý theo 3 bối cảnh: học tập, văn phòng và Software Engineer. Tôi chỉ giữ những ý tôi đã trực tiếp gặp; số liệu ở cột "Dấu hiệu thật" là ước lượng của tôi.
- Bỏ ý "Tìm lại thông báo hoặc link cũ trong kênh chat lớp" vì trùng pattern với #2 (tìm lại thông tin cũ trong kênh chat). Thay bằng #5 "PR chờ review".
- Sau khi ước lượng số liệu, #3 (0 lần trễ) và #5 (review dưới 4 giờ) cho thấy pain nhỏ, nên không đưa vào top 3.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Tester hỏi lặp lại (#4) | Pain lớn nhất trong 5 ý (30–150 phút/tuần), lặp lại hằng tuần, 25–50% câu là câu cũ; có độ mơ hồ nên so sánh được cả 4 mức can thiệp | Tỉ lệ câu trùng mới là ước lượng; câu hỏi mới (50–75%) FAQ không giải được |
| 2 | Tìm tài liệu hoặc quyết định cũ (#2) | Phải tìm ở 3 nơi (chat, Drive, Jira); nhiều người trong ngành gặp nên dễ kiểm chứng | Impact nhỏ (5–30 phút/tuần); có thể chỉ cần quy ước lưu tài liệu |
| 3 | Setup môi trường project mới (#1) | Bottleneck rất cụ thể (config ~2 giờ); quy trình vẽ được ngay | Tần suất thấp (chỉ khi vào project mới), nên tổng impact phụ thuộc số người mới mỗi năm |

### Problem Card #1 — Tester hỏi lặp lại

| Trường | Nội dung |
|---|---|
| Job Story | Khi Tester/QA hỏi về luồng nghiệp vụ, dữ liệu test hoặc cấu hình của phần hệ thống tôi phụ trách, tôi muốn họ tự tìm được câu trả lời đúng cho những câu đã từng được hỏi, để tôi không bị cắt ngang khi đang code |
| Actor | Software Engineer phụ trách một module, người hay được Tester/QA hỏi (đã thu hẹp từ 4 nhóm người hỏi xuống nhóm hỏi nhiều nhất) |
| Thời điểm / bối cảnh | Trong giờ làm, câu hỏi đến qua chat vào bất kỳ lúc nào, thường khi tester đang test tính năng của tôi |
| Quy trình hiện tại (3–7 bước) | 1. Nhận câu hỏi qua chat · 2. Dừng việc đang code, đọc câu hỏi · 3. Nhớ lại hoặc tra lại code/tài liệu · 4. Soạn câu trả lời · 5. Quay lại task, lấy lại mạch làm việc |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3, tra lại code/tài liệu để trả lời đúng: khoảng 5 phút/câu (trên tổng khoảng 12 phút/câu) |
| Impact (nếu không giải thì sao) | 6–10 câu/tuần × khoảng 12 phút ≈ 70–120 phút/tuần bị cắt ngang; trong đó 25–50% là câu cũ (khoảng 2–5 câu, 25–60 phút/tuần) |
| Success metric (baseline → target) | Số câu hỏi lặp lại từ 2–5 câu/tuần xuống còn tối đa 1 câu/tuần. Đo bằng đếm tin nhắn và đánh dấu câu trùng trong 2 tuần trước và 2 tuần sau thay đổi |
| Phương án không dùng AI | Viết FAQ cho các câu tester hay hỏi lại, ghim trong kênh team; quy ước tester hỏi trong kênh chung thay vì nhắn riêng, để câu trả lời cũ tìm lại được |
| Giả thuyết về AI (nếu có) | Trả lời câu hỏi của tester dựa trên FAQ và tài liệu, có dẫn nguồn; câu nào không có trong tài liệu thì chuyển cho tôi |
| Cảm nhận nhanh | Rule (FAQ) trước; Workflow nếu câu hỏi quá đa dạng |

Quy trình nháp hiện tại (khoảng 12 phút/câu):

```text
[1 Nhận câu hỏi: 1'] → [2 Dừng việc, đọc câu hỏi: 1'] → [3 Tra code/tài liệu: 5'] ← BOTTLENECK
→ [4 Soạn trả lời: 2'] → [5 Quay lại task, lấy lại mạch: 3']
```

### Problem Card #2 — Tìm tài liệu hoặc quyết định cũ

| Trường | Nội dung |
|---|---|
| Job Story | Khi cần biết vì sao team chọn thiết kế hoặc cấu hình hiện tại, hoặc cần đúng bản tài liệu mới nhất, tôi muốn tìm ra nhanh trong chat, Drive và Jira, để không phải hỏi lại hoặc làm theo bản cũ |
| Actor | Software Engineer cần tra lại quyết định thiết kế, cấu hình hoặc bản spec mới nhất |
| Thời điểm / bối cảnh | Khi bắt đầu task chạm vào phần code cũ, hoặc khi người khác hỏi "vì sao hệ thống làm vậy" |
| Quy trình hiện tại (3–7 bước) | 1. Nhớ mơ hồ, đoán nơi lưu · 2. Tìm từ khóa trong chat · 3. Lục Drive/Jira, so phiên bản · 4. Hỏi đồng nghiệp nếu không thấy · 5. Xác nhận đúng bản mới nhất |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3, lục Drive/Jira và so phiên bản: khoảng 5 phút/lần (trên tổng khoảng 12 phút/lần) |
| Impact (nếu không giải thì sao) | 1–2 lần/tuần × khoảng 12 phút ≈ 12–24 phút/tuần; rủi ro làm theo spec hoặc cấu hình cũ |
| Success metric (baseline → target) | Thời gian tìm từ 5–15 phút/lần xuống dưới 5 phút/lần. Đo bằng ghi lại mỗi lần tìm trong 2 tuần |
| Phương án không dùng AI | Quy ước gắn link tài liệu chính vào ticket Jira; ghi quyết định thiết kế ngắn (ADR) ngay trong repo; ghim link spec mới nhất trong kênh team |
| Giả thuyết về AI (nếu có) | Tìm chung trên chat, Drive và Jira rồi tóm tắt kèm link nguồn. Chưa chắc cần, vì tần suất thấp |
| Cảm nhận nhanh | No AI / Rule |

Quy trình nháp hiện tại (khoảng 12 phút/lần):

```text
[1 Nhớ mơ hồ, đoán nơi lưu: 1'] → [2 Tìm từ khóa trong chat: 3'] → [3 Lục Drive/Jira, so phiên bản: 5'] ← BOTTLENECK
→ [4 Hỏi đồng nghiệp nếu không thấy: 2'] → [5 Xác nhận đúng bản mới nhất: 1']
```

### Problem Card #3 — Setup môi trường project mới

| Trường | Nội dung |
|---|---|
| Job Story | Khi tôi hoặc một thành viên mới bắt đầu làm một project mới, tôi muốn chạy được project ở máy local ngay trong ngày đầu, để bắt tay vào task sớm mà không phải hỏi đi hỏi lại người cũ |
| Actor | Software Engineer mới vào team hoặc chuyển sang repo khác |
| Thời điểm / bối cảnh | Ngày đầu vào project; lần gần nhất mất khoảng nửa ngày |
| Quy trình hiện tại (3–7 bước) | 1. Clone repo · 2. Đọc README · 3. Cài runtime và dependency · 4. Cấu hình biến môi trường/config · 5. Hỏi người cũ giá trị config · 6. Chạy được app và test |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4, cấu hình biến môi trường/config: khoảng 120 phút, vì không có sẵn giá trị config đúng |
| Impact (nếu không giải thì sao) | Khoảng 240 phút (nửa ngày) cho mỗi lần vào project mới; người cũ mất khoảng 40 phút hỗ trợ |
| Success metric (baseline → target) | Thời gian từ lúc clone tới khi chạy được: từ khoảng 240 phút xuống dưới 60 phút. Đo bằng bấm giờ ở lần setup tiếp theo |
| Phương án không dùng AI | File `.env.example` có giá trị mặc định; script setup một lệnh hoặc docker-compose/devcontainer; cập nhật README mỗi khi đổi config |
| Giả thuyết về AI (nếu có) | Không cần AI: các bước có đúng/sai rõ ràng, script và tài liệu đã đủ |
| Cảm nhận nhanh | No AI |

Quy trình nháp hiện tại (khoảng 240 phút):

```text
[1 Clone: 5'] → [2 Đọc README: 15'] → [3 Cài runtime + dependency: 40']
→ [4 Cấu hình env/config: 120'] ← BOTTLENECK → [5 Hỏi người cũ giá trị config: 40'] → [6 Chạy được app + test: 20']
```

### Card muốn pitch nhất

- Card số: 1 (Tester hỏi lặp lại)
- Vì sao: Pain lớn nhất trong 5 ý (30–150 phút/tuần), lặp lại hằng tuần, và đủ mơ hồ để nhóm so sánh No AI / Rule / Workflow / Agent.
- Câu hỏi muốn nhóm phản biện: Chỉ 25–50% câu hỏi là câu cũ. Một trang FAQ có đủ không, hay phần câu hỏi mới mới là phần tốn thời gian thật?

### AI đã phản biện card thế nào

AI (Claude) đóng vai "PM hoài nghi" theo prompt trong worksheet.

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Card câu hỏi lặp lại: người hỏi gộp 4 nhóm (dev mới, tester, PO, khách hàng) có loại câu hỏi khác nhau; actor quá rộng | Đồng ý | Thu hẹp người hỏi xuống Tester/QA, nhóm hỏi nhiều nhất |
| Card câu hỏi lặp lại: bottleneck thật có thể là bước 5 (mất mạch sau khi bị cắt ngang), không phải bước 3 tra cứu | Không đồng ý | Giữ bước 3: theo ước lượng của tôi, tra cứu khoảng 5 phút, lấy lại mạch khoảng 3 phút |
| Card câu hỏi lặp lại: chưa biết bao nhiêu % câu hỏi là trùng lặp; nếu tỉ lệ thấp thì FAQ không giúp nhiều | Đồng ý | Ước lượng 25–50% câu trùng; đổi success metric sang đo số câu trùng, và đưa câu này thành câu hỏi phản biện cho nhóm |
| Card PR chờ review: bottleneck là thời gian chờ, nên giả thuyết "AI review sơ bộ" không đánh vào đúng bước nghẽn | Đồng ý | Khi ước lượng thấy PR thường được review dưới 4 giờ, pain nhỏ, nên bỏ card khỏi top 3 và thay bằng "Tìm tài liệu cũ" |
| Card setup: tần suất thấp, cần nhân với số lần vào project mới mới thấy impact thật | Đồng ý | Ghi rõ ở cột "Điều còn chưa chắc" của top 3; impact tính theo mỗi lần vào project |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch 3 card: #4 Tester hỏi lặp lại (card chính), #5 Tìm tài liệu/quyết định cũ, #6 Setup môi trường project mới | Card #4 vào shortlist, xếp thứ 2 với 31 điểm (sau card #1 của Đạt, 33 điểm) |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: (1) Hỏi Đạt về card Xanh SM: "Dữ liệu định vị và cuốc xe là của nội bộ hãng, làm sao mình lấy được data để kiểm chứng?" (2) Hỏi Đạt về card đồ án: "Sinh viên ngại dùng tool là do thói quen, có bot hướng dẫn thì các bạn có chịu duy trì không?" (3) Hỏi Quang về card phỏng vấn tiếng Anh: "ChatGPT hay Elsa Speak đã làm việc này rất tốt, điểm khác biệt là gì?" | Cả 3 candidate này đều không vào shortlist; câu hỏi (1) chỉ ra rủi ro Feasibility (không tiếp cận được dữ liệu), câu (3) chỉ ra đã có giải pháp sẵn trên thị trường |
| Nhận phản biện | Câu hỏi tôi nhận được: (1) Đạt hỏi card #4: "Chỉ 25–50% câu là câu cũ, viết một trang FAQ Notion chuẩn thì có giải quyết được 80% mà không cần AI không?" (2) Đạt hỏi card #5: "Impact chỉ 5–30 phút/tuần, có đáng xây hệ thống AI riêng không?" (3) Quang hỏi card #6: "Tần suất vào project mới rất thấp, tổng impact cả năm có đủ lớn không?" | Tôi đã sửa gì: Chấp nhận phản biện (1): phần câu hỏi lặp lại của card #4 giải được bằng No AI (FAQ), nên đồng ý để nhóm loại card #4 khỏi lựa chọn cuối. Phản biện (2), (3) trùng với điểm "Điều còn chưa chắc" tôi đã ghi ở CP2, nên không đề xuất #5, #6 vào shortlist |
| Gom cluster / cây OST | Hỗ trợ Đạt (người chính, cùng Quang) ở CP3: xếp 3 card của tôi vào cluster (#4, #5 vào cluster A "Năng suất & cộng tác nhóm kỹ thuật"; #6 vào cluster B "Onboarding & quy trình cá nhân") | Cluster A chứa candidate được chọn (#1) |
| Chọn candidate problem | Cùng nhóm chấm điểm shortlist 3 candidate (#1, #4, #7); cùng Quang phản biện ý tưởng ban đầu của card #1 (AI xử lý audio real-time, ngắt lời cuộc họp) | Nhóm đổi phạm vi: không can thiệp real-time bằng giọng nói, chỉ xử lý transcript sau mỗi block tranh luận 15 phút hoặc khi team yêu cầu (mục "Xử lý bất đồng") |
| Kiểm chứng / research | **Kiểm chứng (người chính CP4, Đạt và Quang hỗ trợ):** lập Assumption Map (5 giả định, chọn #1 và #2 để kiểm trước) và phỏng vấn 3 người (1 Tech Lead, 2 đồng nghiệp/sinh viên làm đồ án capstone). **Research (hỗ trợ Quang):** tham gia phần research giải pháp đã có | Kiểm chứng: ghi được tín hiệu phản bác (1/3 cảnh báo AI kết luận "nên chọn A" sẽ gây tự ái) → nhóm sửa problem: AI không được kết luận thay, chỉ sinh ma trận đối chiếu. Research: bảng 3 nguồn (Otter/Fireflies, Granola, ADR pattern) → nhóm không tự làm Speech-to-Text mà tận dụng transcript có sẵn, đầu ra theo chuẩn ADR |
| Quy trình nhóm | Hỗ trợ Đạt (người chính) ở CP5: sơ đồ quy trình As-Is / To-Be và bảng before/after | Quy trình hiện tại 5 bước, 85 phút, bottleneck ở bước tranh luận bế tắc (25 phút); quy trình tương lai 45 phút, có bước con người duyệt ma trận và phương án quay về (facilitator dùng bảng trắng thủ công) |
| Problem Statement | Hỗ trợ Đạt (người chính) viết Problem Statement v0; người chính viết Problem Statement v1 (CP6) | v0: metric 25 phút → dưới 8 phút, đo bằng bấm giờ 4 buổi họp; boundary: AI không chốt quyết định, không ngắt lời, con người duyệt trước khi biểu quyết. v1 thêm AI intervention point (phút 35, sau tranh luận tự do), mức chọn và người kiểm tra |
| Mức can thiệp AI | Người chính CP6 (Đạt và Quang hỗ trợ): ma trận độ mơ hồ × độ phức tạp, bảng so sánh 4 mức, AI Canvas, 2 câu hỏi PAIR và tiêu chí đánh giá | Nhóm chọn AI Copilot có con người duyệt (Human-in-the-loop); 3 tiêu chí đánh giá: đầy đủ, đối xứng, không ảo giác |
| Quyết định | Hỗ trợ Quang (người chính) đánh giá 4 rủi ro và ra quyết định | Quyết định Go, pilot trên transcript 1 buổi họp giả lập; ngưỡng dừng: đồng tình dưới 60% hoặc review quá 12 phút → quay về facilitator + template |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Gợi ý khoảng 15 vấn đề theo 3 bối cảnh (học tập, văn phòng, Software Engineer) và tìm số liệu ngành (Stack Overflow 2024, Atlassian DevEx 2025, Microsoft Work Trend Index 2023) | Gợi ý được vấn đề sát công việc SWE, kèm link nguồn | Có 1 số liệu (16% flaky test ở Google) AI không kiểm được nguồn gốc; 2 ý gợi ý (tìm tài liệu cũ, tìm thông báo lớp) trùng pattern | Thay ý "tìm thông báo lớp" bằng "PR chờ review"; không dùng số liệu chưa kiểm được |
| CP2 Problem Card | Soạn khung Problem Card và quy trình nháp; hỏi trắc nghiệm để tôi ước lượng số liệu; đề xuất cách chia số phút cho từng bước dựa trên tổng thời gian tôi ước lượng (tôi xác nhận khớp); đóng vai "PM hoài nghi" | Chỉ ra actor card #1 quá rộng; nhận ra PR được review dưới 4 giờ là tín hiệu phản bác | Ban đầu xếp "PR chờ review" vào top 3 trước khi có số liệu; khi có số liệu thì pain nhỏ | Thu hẹp actor card #1 xuống Tester/QA; thay card PR bằng "Tìm tài liệu cũ"; không đồng ý đổi bottleneck card #1 sang bước 5 |
| CP4 Research | (Kiểm chứng) Nhờ AI rà Assumption Map và phần phỏng vấn | Chỉ ra số người phỏng vấn ghi lệch nhau (2 và 3), chỉ có 1 snapshot cho 3 buổi; lời khen ("hoan nghênh") không phải bằng chứng theo The Mom Test; giả định #2 (AI trích xuất chính xác) không kiểm được bằng phỏng vấn; thiếu giả định Viability về việc công ty có cho gửi transcript họp lên API bên ngoài | Khi viết lại câu tổng hợp phỏng vấn, AI dùng cách diễn đạt khẳng định quá mức so với ghi chép ("kể lại lần họp gần nhất") và phải tự sửa lại; AI không biết nội dung các buổi phỏng vấn nên không điền được snapshot #2, #3 | Hoàn tác các sửa đổi AI làm trực tiếp trên group report; giữ nguyên nội dung phỏng vấn nhóm đã ghi |
| CP5 Quy trình | Nhờ AI đọc lại quy trình trước/sau và Problem Statement v0 của nhóm | Chỉ ra các chỗ không khớp: target thời gian bế tắc "dưới 5 phút" (before/after) và "dưới 8 phút" (v0); số bước thủ công ghi 2 nhưng sơ đồ có 3 bước con người làm; tổng thời gian 85 và 90 phút giữa các file; bottleneck mô tả cảm xúc chứ chưa phải một bước | AI chỉ đọc file, không biết bối cảnh thảo luận thật của nhóm | Không sửa: phần quy trình do Đạt và Quang phụ trách, giữ nguyên bản nhóm đã chốt |
| CP5–6 Problem Statement | Nhờ AI chỉ ra lỗ hổng Problem Statement v1 và tiêu chí đánh giá | Impact ghi "mỗi tuần" (v0) và "mỗi buổi" (v1) mâu thuẫn; tiêu chí 2 (mỗi phương án phải có nhược điểm) mâu thuẫn tiêu chí 3 (không bịa); "suy luận logic" là kẽ hở cho bịa đặt; chỉ số hài lòng ≥ 4.2/5 không có baseline | AI sửa thẳng vào group_report thay vì chỉ phản biện, trái RULES.md (CP5–6 chỉ dùng AI để phản biện) | Hoàn tác các sửa đổi AI làm trực tiếp; giữ bản Problem Statement v1 và 3 tiêu chí đánh giá nhóm đã chốt |
| CP6 Mức can thiệp / quyết định | Nhờ AI phản biện mức can thiệp và 4 rủi ro | Chỉ ra thiết kế (các bước cố định, AI làm 1 bước) theo định nghĩa của đề là Workflow chứ không phải Agent; ma trận đang xếp "hiểu ngữ nghĩa" vào độ phức tạp thay vì độ mơ hồ; Value và Viability đang chấm lạc quan khi mới có 3 người phỏng vấn và chưa biết quy định công ty về dữ liệu họp | AI chỉ dựa vào định nghĩa trong tài liệu và nội dung file, không biết các lý do nhóm đã thảo luận khi chọn mức Copilot | Giữ mức Copilot có Human-in-the-loop nhóm đã chốt, không đổi sang Workflow |
| CP7 Reflection | Nhờ AI (Claude) đọc group report, TEAM.md và báo cáo cá nhân để soạn nháp 6.1–6.7 từ các sự kiện đã ghi | Gom lại các lần phản biện, đổi ý và kết quả kiểm chứng nằm rải rác ở nhiều mục; tóm tắt chuỗi problem → quyết định | AI chỉ biết nội dung đã ghi trong file, không biết cảm nhận thật của tôi | Tự rà và sửa từng câu theo trải nghiệm của mình; tập giải thích lại 6.7 bằng lời của mình |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5).

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Cả 3 card của tôi đều là pain của một người: tôi bị tester hỏi, tôi tìm tài liệu, tôi setup project. Card trade-off cuộc họp của Đạt thì khác. Mỗi phút bế tắc ở đó nhân với 4–8 người trong phòng họp, nên cùng khoảng 25 phút nhưng impact lớn hơn nhiều. Tôi rút ra là khi tính impact phải tính tất cả những người cùng mất thời gian, không chỉ người kể pain. Nghe các card còn lại, tôi cũng thấy hai lý do làm một problem yếu đi dù pain có thật. Thứ nhất là không lấy được dữ liệu để kiểm chứng, như card tài xế Xanh SM (dữ liệu nằm ở hãng). Thứ hai là đã có công cụ làm tốt việc đó, như card luyện phỏng vấn tiếng Anh (ChatGPT, Elsa Speak). Card debug firmware của Quang cho tôi thấy thêm một giới hạn: nếu nguyên nhân nằm ở phần cứng vật lý thì AI không đo được, và càng dễ đoán sai.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Có. Ở card #1, ý tưởng ban đầu là AI nghe audio real-time và chen vào khi cuộc họp bế tắc. Nhóm đã nghĩ tới cách AI can thiệp trước khi biết người họp thật sự cần gì. Quang hỏi liệu AI ngắt lời có làm mọi người ức chế không, còn tôi lo xử lý audio tiếng Việt real-time rất dễ sai. Nhóm đổi sang xử lý transcript sau mỗi block tranh luận 15 phút hoặc khi team yêu cầu. Khi vẽ cây OST, nhóm cũng phải gạch ba nhánh thực chất là giải pháp: bot Discord nghe giọng nói, fine-tune LLM để chấm điểm phương án, dashboard voting. Bản thân tôi cũng từng như vậy ở CP2: card tester hỏi lặp lại có sẵn giả thuyết "AI trả lời dựa trên FAQ", trong khi chính FAQ đã giải được phần câu cũ.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Có. Lúc pitch card #4, Đạt hỏi tôi: "Chỉ 25–50% câu là câu cũ, vậy viết một trang FAQ Notion chuẩn thì có giải quyết được 80% mà không cần AI không?". Tôi chấp nhận, vì câu này trùng đúng điểm tôi chưa chắc từ CP2. Phần câu lặp lại giải được bằng No AI, còn phần câu mới thì AI cũng chỉ là RAG thông thường. Vì vậy tôi đồng ý để nhóm loại card của mình, dù nó xếp thứ hai với 31 điểm. Ngược lại, có lần tôi không đổi ý: AI cho rằng bottleneck của card này là bước lấy lại mạch làm việc, nhưng tôi giữ bước tra cứu vì theo ước lượng của tôi bước đó tốn thời gian hơn.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Có hai điều. Thứ nhất, người phỏng vấn không cần AI chỉ ra "ai đúng". Họ cần một bên trung lập liệt kê sòng phẳng trade-off của từng phương án, và 1/3 người cảnh báo rằng nếu AI kết luận "nên chọn A" thì phe ủng hộ B sẽ tự ái. Vì vậy nhóm thêm boundary: AI không được kết luận thay con người. Thứ hai, họ đã có cách tự xử lý: cử một người làm facilitator ghi Pros/Cons lên bảng trắng. Cách này hỏng vì chính người ghi cũng bị cuốn vào tranh luận. Như vậy đối thủ thật của giải pháp là một người facilitator chứ không phải không có gì. Ở phần research, tôi thấy Otter và Fireflies đã chuyển giọng nói thành văn bản tốt, nên nhóm không cần tự làm phần này.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Khó nhất là làm cho metric đo được và các con số khớp nhau. "Thời gian bế tắc" khó bấm giờ vì không rõ lúc nào tranh luận có ích chuyển thành bế tắc, và baseline 25 phút vẫn là ước lượng. Khi nhờ AI rà lại, tôi thấy nhiều chỗ chưa khớp. Target là "dưới 5 phút" ở bảng before/after nhưng "dưới 8 phút" ở v0. Impact ghi "mỗi tuần" ở v0 nhưng "mỗi buổi" ở v1. Bottleneck đang tả cảm xúc ("cái tôi") hơn là một bước trong quy trình. Tiêu chí "mỗi phương án phải có nhược điểm" cũng có thể đẩy AI bịa nhược điểm, trái với tiêu chí "không ảo giác".

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Là người chính phụ trách kiểm chứng, tôi sẽ ghi snapshot cho cả 3 buổi phỏng vấn thay vì một buổi. Tôi sẽ hỏi nhiều hơn về hành vi đã xảy ra theo The Mom Test, vì câu "rất hoan nghênh" chỉ là lời khen, chưa phải bằng chứng. Giả định #2 (AI trích xuất đúng, không thiên vị) không kiểm được bằng phỏng vấn. Tôi sẽ đề xuất chạy thử prompt trên một transcript thật trước khi chốt Go. Tôi cũng sẽ phản biện mạnh hơn ở hai điểm. Thứ nhất là mức can thiệp: thiết kế hiện tại có các bước cố định và AI làm một bước, nên theo định nghĩa thì gần với Workflow hơn Agent, trong khi nguyên tắc là chọn mức đơn giản nhất đủ dùng. Thứ hai là rủi ro Value và Viability đang được chấm "Thấp" khi mới hỏi 3 người và chưa biết công ty có cho gửi transcript họp lên API bên ngoài không.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Problem của nhóm là các buổi họp chọn giải pháp kỹ thuật (Design/RFC Review) của team 4–8 người hay bị bế tắc, vì mỗi người bảo vệ phương án của mình mà không ai chịu nói ra nhược điểm. Buổi họp hiện tại có 5 bước: trình bày, tranh luận, bế tắc, ghi biên bản, chốt. Bottleneck là bước bế tắc, mất khoảng 25 phút mỗi buổi, và cuối cùng thường chốt theo người nói to nhất hoặc theo sếp. Metric là giảm thời gian bế tắc từ 25 phút xuống dưới 8 phút và 100% buổi họp có bảng trade-off. Nhóm đo bằng bấm giờ 4 buổi họp. Boundary là AI không được chọn phương án thay team, không ngắt lời khi đang họp, và con người phải duyệt bảng trade-off trước khi biểu quyết và lưu ADR. Nhóm chọn mức Copilot có con người duyệt: AI chỉ nhận transcript sau phần tranh luận rồi lập ma trận trade-off cho các phương án. Template Pros/Cons (No AI) hay script đếm từ khóa (Rule) không hiểu được nội dung tranh luận nên không đủ dùng. Quyết định là Go với pilot trên transcript của một buổi họp giả lập. Nhóm sẽ dừng và quay về facilitator cùng template nếu dưới 60% kỹ sư đồng tình với bảng hoặc việc sửa bảng mất quá 12 phút.

---

## 7. Tài liệu tham khảo

- Stack Overflow Developer Survey 2024 — Professional Developers: https://survey.stackoverflow.co/2024/professional-developers (61% developer mất hơn 30 phút/ngày tìm câu trả lời; 53% cho rằng chờ câu trả lời làm gián đoạn công việc)
- Atlassian, State of Developer Experience 2025: https://www.atlassian.com/blog/developer/developer-experience-report-2025 (tìm thông tin là trở ngại số 1)
- Microsoft Work Trend Index 2023, "Will AI Fix Work?": https://www.microsoft.com/en-us/worklab/work-trend-index/will-ai-fix-work
- Rob Fitzpatrick, *The Mom Test* — dùng cho câu hỏi phỏng vấn CP4.
- Intercom, Jobs-to-be-Done (Job Story) — dùng cho CP1.
- Anthropic, *Building Effective Agents* — định nghĩa Workflow và Agent dùng ở CP6: https://www.anthropic.com/engineering/building-effective-agents
