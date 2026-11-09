# Báo cáo cá nhân — 202603392_NguyenTuanQuang

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên:Nguyễn Tuấn Quang
- MSSV:202603392
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
| Success metric (baseline → target) | Baseline tạm tính 3–6 giờ/ca. Ghi thời gian và số lần lặp của ít nhất 3 ca trước khi chốt target theo phút; mục tiêu ban đầu là giảm số phép kiểm tra lặp lại. |
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
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | | | | |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
