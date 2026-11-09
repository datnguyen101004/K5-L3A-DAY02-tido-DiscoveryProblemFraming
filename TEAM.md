# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: tido
- Candidate problem nhóm chọn (1 câu): Nhóm kỹ sư và Product Manager bị bế tắc 20–30 phút trong các buổi họp kỹ thuật do tranh cãi cảm tính và bảo vệ thiên kiến cá nhân khi chọn giải pháp, dẫn đến lãng phí giờ công và nguy cơ chọn sai kiến trúc hệ thống.
- Quyết định cuối (Go / Not Yet / No-Go): Go

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Phạm Nguyễn Tất Đạt | 2A202603401 | Nhóm trưởng, Pitch candidate chính, Thiết kế quy trình & Problem Statement | datnguyen101004 |
| 2 | Nguyễn Ngọc Toàn | 2A202603405 | Phản biện chính, Phụ trách Kiểm chứng (Assumption & Interview) | jpack1 |
| 3 | Nguyễn Tuấn Quang | 202603392 | Phụ trách Research giải pháp thị trường, Đánh giá rủi ro & Tiêu chí Eval | |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Phạm Nguyễn Tất Đạt | Nguyễn Ngọc Toàn, Nguyễn Tuấn Quang | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | Nguyễn Ngọc Toàn | Phạm Nguyễn Tất Đạt, Nguyễn Tuấn Quang | Assumption map, interview snapshot |
| CP4 — Research | Nguyễn Tuấn Quang | Phạm Nguyễn Tất Đạt, Nguyễn Ngọc Toàn | Bảng research đối thủ có link |
| CP5 — Quy trình trước/sau | Phạm Nguyễn Tất Đạt | Nguyễn Ngọc Toàn, Nguyễn Tuấn Quang | Sơ đồ quy trình As-Is / To-Be + bảng before/after |
| CP5 — Problem Statement v0 | Phạm Nguyễn Tất Đạt | Nguyễn Ngọc Toàn, Nguyễn Tuấn Quang | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | Nguyễn Ngọc Toàn | Phạm Nguyễn Tất Đạt, Nguyễn Tuấn Quang | Ma trận mơ hồ/phức tạp, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | Nguyễn Tuấn Quang | Phạm Nguyễn Tất Đạt, Nguyễn Ngọc Toàn | 4 rủi ro + Quyết định Go/Not Yet/No-Go |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### PhamNguyenTatDat-2A202603401

**Phần việc phụ trách:**

- Pitch Problem Card #1 và bảo vệ thành công đề tài của mình làm đề tài chung cho nhóm.
- Điều phối phiên hội tụ nhóm (CP3): phân loại cluster, vẽ cây OST và chủ trì chấm điểm ma trận shortlist.
- Thiết kế sơ đồ quy trình As-Is và To-Be (CP5), xác định điểm nghẽn và ranh giới can thiệp (Boundary).
- Soạn thảo Problem Statement v0 và hoàn thiện Problem Statement v1 chuẩn Lean UX & Google PAIR.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đóng góp trực tiếp vào các mục 1, 2, 4, 5, 7 trong `group_report.md`.
- Đề xuất thay đổi kiến trúc can thiệp: chuyển từ "ngắt lời bằng giọng nói real-time" sang "xử lý text transcript sau phiên tranh luận", giúp giải quyết lo ngại lớn nhất của nhóm về tính khả thi.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- Bảng Pitch & Bảng chấm điểm Shortlist mục 2 trong `report/team/group_report.md`.
- Sơ đồ quy trình Before/After mục 4 và Bảng Problem Statement v0/v1 mục 5 và 7 trong `report/team/group_report.md`.
- Báo cáo cá nhân `report/individual/2A202603401_PhamNguyenTatDat.md`.

**Điều mình học được từ phần nhóm:**

- Nhận ra sức mạnh của việc phản biện đa chiều: các câu hỏi hoài nghi của Toàn và Quang đã giúp mình gọt giũa bài toán từ một ý tưởng viển vông (AI ngắt lời real-time) thành một quy trình Copilot có tính khả thi cực kỳ cao.
- Thấu hiểu sâu sắc nguyên tắc Human-in-the-loop: trong các quyết định kỹ thuật quan trọng, AI chỉ nên đóng vai trò cung cấp góc nhìn đối chiếu minh bạch (Augment), tuyệt đối không được tước quyền quyết định của con người (Automate).

### NguyenNgocToan-2A202603405

**Phần việc phụ trách:**

- Người chính: CP4 — Kiểm chứng (Assumption Map, phỏng vấn, interview snapshot).
- Người chính: CP6 — Mức can thiệp AI và Problem Statement v1 (ma trận mơ hồ/phức tạp, so sánh 4 mức, AI Canvas, câu hỏi PAIR, tiêu chí đánh giá).
- Hỗ trợ: CP3 hội tụ nhóm; CP4 research; CP5 quy trình trước/sau và Problem Statement v0; CP6 quyết định.
- Vai trò trong nhóm: người phản biện chính.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Pitch 3 Problem Card (#4 Tester hỏi lặp lại, #5 Tìm tài liệu/quyết định cũ, #6 Setup môi trường); card #4 vào shortlist, xếp thứ 2 (31 điểm).
- Đặt câu hỏi phản biện cho 3 candidate của bạn khác (#2 Xanh SM, #3 quản lý đồ án, #8 phỏng vấn tiếng Anh); cùng Quang phản biện ý tưởng AI ngắt lời real-time của card #1, dẫn tới việc nhóm chuyển sang xử lý transcript sau phiên tranh luận.
- Lập Assumption Map 5 giả định và phỏng vấn 3 người (1 Tech Lead, 2 đồng nghiệp/sinh viên làm đồ án capstone); ghi lại tín hiệu phản bác "AI kết luận thay sẽ gây tự ái", từ đó nhóm thêm boundary AI không được kết luận thay.
- Phân tích mức can thiệp AI và viết Problem Statement v1 cùng tiêu chí đánh giá đầu ra.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- Bảng Pitch dòng #2–#8 và mục "Xử lý bất đồng" (mục 2) trong `report/team/group_report.md`.
- Assumption Map, interview snapshot và bảng tổng hợp kiểm chứng (mục 3.1, 3.2) trong `report/team/group_report.md`.
- Mức can thiệp AI (mục 6) và Problem Statement v1 + tiêu chí đánh giá (mục 7) trong `report/team/group_report.md`.
- Báo cáo cá nhân `report/individual/2A202603405_NguyenNgocToan.md` (commit `ad78ae0`).

**Điều mình học được từ phần nhóm:**

- __
