# Báo cáo cá nhân — NguyenVanHuy-2A202603432

## 1. Thông tin thành viên

- Họ tên: Nguyễn Văn Huy
- MSSV: 2A202603432
- Email: 26ai.huynv6@vinuni.edu.vn
- GitHub: nvhuy-03
- Nhóm: Neon · Lớp: L3A · Repo: https://github.com/lythanhlap/K5-L3A-DAY13-Neon-LaunchEconomics
- Vai trong nhóm: Người gắn nhãn 1, kiêm giữ đồng hồ và theo dõi điều kiện "Xong khi" của từng checkpoint

## 2. Phần việc phụ trách

- CP1: soát code `src/lab13.py` của Cường (chi phí tính cả lần chạy lỗi, chia 1.000 trước khi nhân giá), đối chiếu số với slide/bảng đáp án, ngưỡng lệch ≤ 2%.
- CP1–CP2: hoàn thiện `report/team/bang_chi_phi.md` (bảng A1–A4, B1–B4), viết xếp hạng B2 và câu trả lời B3, B4.
- CP3: gắn nhãn độc lập 20 ca lỗi, chủ file `bang_loi.md`, điền 3 dòng khắc phục (Do người dùng, Hệ thống, Ngữ cảnh).
- CP4–CP5: viết năm câu D2, hoàn thiện 2 dòng rủi ro kinh tế.
- Trước khi nộp: soát checklist `SUBMISSION.md`.

## 3. Đóng góp cụ thể

**Soát code CP1 (A2, A3):**

- Kiểm tử số trong `mo_hinh` ([src/lab13.py](../../src/lab13.py)): `runs` chỉ lọc theo `request_id`, không lọc `status`. Vì vậy token và tool của **mọi** lần chạy, kể cả lần lỗi, đều được cộng. Kết quả: đúng.
- Kiểm thứ tự tính: `tokens_in / 1000 * gia_vao + tokens_out / 1000 * gia_ra`, tức chia 1.000 trước khi nhân giá. Kết quả: đúng.
- Chạy `python lab13.py`: ba phép thử A1 in ĐẠT (1,20 · 1,25 · 1,25).
- Đối chiếu 9 dòng A2 và 4 dòng A3 với bảng đáp án: **lệch 0%** ở mọi số (token 245.585 đ, tool 84.000 đ, tổng 4.373.585 đ, 978 việc thành công, chi phí mỗi việc thành công 4.472 đ [simulated], hoá đơn/yêu cầu 274,7 đ; A3 noi_dia 2.696 đ, hang_nang 8.221 đ, quoc_te 22.515 đ, doi_tac 10.215 đ [simulated]).

**Điền `bang_chi_phi.md`:**

- Điền đủ bảng A1, A2 (9 dòng), A3 (4 dòng), A4 (2 mức khối lượng), B1 (9 kịch bản), B3 (3 giới hạn). Mọi số tính từ cột `_simulated` có nhãn `simulated`.
- Tự kiểm tính tuyến tính B1: "giảm một nửa" bằng đúng nửa mức tăng của "gấp đôi" (5,6 → 2,8; 40,7 → 20,3; 51,8 → 25,9).
- B2: cặp token ×2 + xem lại ×2 ra 6.543 đ (+46,3%), bằng tổng hai tác động riêng. Xếp hạng: 1. số ca làm lại (+51,8%), 2. tỉ lệ xem lại (+40,7%), 3. lương nhân viên (+23,1%) [simulated].
- B3: tính chi phí **cả hệ thống** (cộng 12.000 đ cho mỗi ca không thành công), không chỉ chi phí mỗi việc. Giới hạn 2 lần rẻ nhất cho công ty (6.901.220 đ), khác với giới hạn 1 lần cho chi phí mỗi việc thành công thấp nhất (4.111 đ) [simulated].
- B4: xem lại 100% cho noi_dia + hang_nang ra 11.743 đ = 0,98× của 12.000 đ, hoặc 1,03× nếu dùng phút làm lại thực tế 15,3 phút. Hoà vốn khi mỗi lần xem lại ≤ 5,1 phút [simulated].

**Soát yêu cầu "Xong khi" của B2, B3, B4:**

- Mỗi câu trả lời B2, B3, B4 không quá 3 dòng, đều có số và có nhãn `[simulated]`.
- Đã bổ sung nhãn `simulated` cho các câu B3 và B4 còn thiếu.
- B3 so sánh **chi phí cả hệ thống** (tổng trợ lý + 12.000 đ × số yêu cầu không thành công), không chỉ chi phí mỗi việc thành công.

**CP3 · Gắn nhãn độc lập 20 ca lỗi (người gắn nhãn 1):**

- Gắn nhãn 20 ca trong `docs/Ngay13_Lab13_De_bai_hoc_vien.docx` theo 5 loại Google PAIR, theo nguyên nhân gốc. Không trao đổi với người gắn nhãn 2 (Dũng). Đã ghi vào cột "Nhãn người 1" của `bang_loi.md`.
- Phân bố: Do người dùng 4 ca (1, 6, 9, 14) · Hệ thống 5 ca (2, 7, 8, 15, 20) · Ngữ cảnh 4 ca (3, 10, 16, 18) · Giới hạn hệ thống 4 ca (4, 11, 13, 19) · Ngầm 3 ca (5, 12, 17).
- Các ca phân vân, cần đem ra bàn khi so nhãn:
  - Ca 6 (khách chọn sai mục): gắn Do người dùng, không gắn Hệ thống, vì lỗi gốc là khách chọn sai mục.
  - Ca 8 (dẫn điều 7.2 không có thật): gắn Hệ thống, vì vi phạm thiết kế và có người phát hiện được.
  - Ca 13 (ngoài phạm vi, trả lời chung chung): gắn Giới hạn hệ thống, vì gốc là ngoài phạm vi.
  - Ca 18 (tính đúng, thiếu cách tính): gắn Ngữ cảnh, vì hệ thống làm đúng nhưng khách thấy sai.

**CP3 · Bảng khắc phục 3 ca (Do người dùng, Hệ thống, Ngữ cảnh):**

- Đã điền 3 dòng trong `bang_loi.md`. Mỗi dòng có event đo được, ngưỡng, tần suất và một vai trò phụ trách.
  - Ca 1 · Do người dùng: event `bank_account_rejected`, cảnh báo khi vượt 1% số lệnh hoàn/ngày. Khắc phục bằng kiểm số tài khoản và cho khách xác nhận tên chủ tài khoản. Phụ trách: PM trợ lý hoàn phí.
  - Ca 7 · Hệ thống: báo thành công khi chưa có `ledger_write_ok`. Đối soát mỗi giờ, ngưỡng 0 ca. Chỉ báo "đã hoàn" khi sổ cái xác nhận. Phụ trách: kỹ sư backend phụ trách tích hợp sổ cái.
  - Ca 3 · Ngữ cảnh: event `refund_reopened` với lý do "chưa nhận tiền" dù đã hoàn về ví. Báo cáo theo tuần, ngưỡng 3%. Khắc phục bằng cho khách chọn kênh nhận và ghi rõ trong tin nhắn. Phụ trách: UX writer.
- Chọn ca 7 cho loại Hệ thống vì đây là lỗi nặng nhất: báo khách đã hoàn tiền trong khi tiền chưa đi.

## 4. Bằng chứng

- File: [report/team/bang_chi_phi.md](bang_chi_phi.md). Đầu file có ghi chú đối chiếu, lệch 0% so với đáp án.
- Đầu ra `python lab13.py` khớp từng dòng với bảng đáp án trong `docs/Lab13_Huong_dan_chi_tiet_buoi_chieu.md` (mục A2, A3, A4, B1–B4).
- File: [report/team/bang_loi.md](bang_loi.md): cột "Nhãn người 1" (20 ca), tỉ lệ đồng thuận 18/20 = 90% với người gắn nhãn 2, ba dòng khắc phục ca 1, 7, 3.
- Commit (tác giả `nvhuy-03`):

  | Commit | Nội dung | Gộp vào `main` |
  | --- | --- | --- |
  | `eb7f3fb` | CP1: bảng A1–A4, B1–B4 trong `bang_chi_phi.md`, tạo báo cáo cá nhân | PR #1 |
  | `313227f` | CP2: bổ sung nhãn `simulated` cho B3, B4 | PR #3 |
  | `7c626f6` | CP3: gắn nhãn độc lập 20 ca trong `bang_loi.md` | PR #5 |
  | `d211e79` | CP3: 3 dòng khắc phục (Do người dùng, Hệ thống, Ngữ cảnh) | PR #7 |

## 5. Công cụ AI đã dùng

- **Claude Code** (trong VS Code), dùng để đọc `src/lab13.py`, chạy script, đối chiếu số in ra với bảng đáp án trong tài liệu hướng dẫn, và soạn nháp nội dung `bang_chi_phi.md`.
- CP3: dùng Claude Code để trích 20 ca từ file đề `.docx` và đề xuất nhãn. Mình tự đọc lại từng ca và đối chiếu với định nghĩa 5 loại trước khi giữ nhãn.
- Tự kiểm tra:
  - Đọc lại hai dòng code tính token/tool để xác nhận không lọc theo `status` và có chia 1.000 trước khi nhân giá.
  - So từng con số trong bảng với đầu ra của script và với bảng đáp án.
  - Tự cộng lại các chênh lệch B3: 7.037.585 − 6.901.220 = 136.365 đ; 319 − 234 = 85 ca.
  - Kiểm tính tuyến tính B1.

## 6. Tự đánh giá

- Hoàn thành phần soát số CP1: hai lỗi hay gặp (bỏ lần chạy lỗi, quên chia 1.000) đều không có trong code, mọi số A2, A3 lệch 0% (ngưỡng 2%).
- Bảng chi phí A, B đủ dòng, có nhãn `simulated`, mỗi câu trả lời ≤ 3 dòng và có số.
- Điều học được: chi phí thật nằm ở giờ nhân viên (92,5% tổng chi phí), không phải ở token. Muốn so công bằng với 12.000 đ thì phải tính cả các ca chuyển cho nhân viên làm.
