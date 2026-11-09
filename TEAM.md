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
| 2 | Nguyễn Ngọc Toàn | 2A202603405 | Phản biện chính, Phụ trách Kiểm chứng (Assumption & Interview) | |
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

### NguyenTuanQuang-202603392

**Phần việc phụ trách:**

- Phụ trách chính CP4 Research và CP6 Quyết định.
- Hỗ trợ CP3 Hội tụ nhóm, CP4 Kiểm chứng, CP5 Quy trình và Problem Statement v0, CP6 Mức can thiệp và Problem Statement v1.

**Đóng góp cụ thể:**

- Đối chiếu Otter.ai, Fireflies.ai, Granola và mẫu ADR. Đề xuất tận dụng bản chép lời có sẵn và so sánh đầu ra Copilot với bảng do người điều phối tự điền.
- Tổng hợp bốn rủi ro, ghi rõ phạm vi Go cho PoC và cách đo ngưỡng dừng sau ba buổi pilot.
- Phản biện phương án AI chen ngang cuộc họp và đặt câu hỏi về tần suất gặp vấn đề onboarding ở CP3.

**Bằng chứng:**

- [Báo cáo nhóm](report/team/group_report.md), mục 2.1 về pitch, mục 3.3 về research và mục 8 về quyết định.
- [Báo cáo cá nhân](report/individual/202603392_NguyenTuanQuang.md), mục 4 và 5.

**Điều mình học được từ phần nhóm:**

- Khi đánh giá một công cụ họp, cần thử trên cùng một bản chép lời để xem bảng so sánh có đủ căn cứ và người điều phối mất bao lâu để kiểm tra.
