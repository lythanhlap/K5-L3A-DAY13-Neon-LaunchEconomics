# Team

## Thông tin nhóm

- Tên nhóm: Neon
- Lớp: L3A
- Repo nhóm: `K5-L3A-DAY13-Neon-LaunchEconomics` (xem [SUBMISSION.md](SUBMISSION.md))
- URL repo, nhánh nộp, commit chốt: https://github.com/lythanhlap/K5-L3A-DAY13-Neon-LaunchEconomics · nhánh `main` · commit chốt:

## Thành viên

| STT | Họ tên | MSSV | Email | GitHub | Vai trò |
| --: | ------ | ---- | ----- | ------ | ------- |
|   1 | Lý Thành Lập |  2A202603414    |       |      | Người kiểm số |
|   2 | Nguyễn Tiến Cường |  2A202603425    | cuongdelldz@gmail.com | cuong-sadboi | Người viết code |
|   3 | Nguyễn Văn Huy |  2A202603432    |nvhuy2582003@gmail.com | nvhuy-03 | Người gắn nhãn 1 |
|   4 | Phạm Công Dũng |   2A202603428   |       |        | Người gắn nhãn 2, kiêm giữ hồ sơ |

Bốn vai của lab:

- **Người viết code:** viết và chạy `src/lab13.py`.
- **Người kiểm số:** tính tay một con số để đối chiếu, điền bảng.
- **Người gắn nhãn 1:** đọc đề, theo dõi điều kiện "Xong khi"; gắn nhãn 20 ca độc lập ở CP3.
- **Người gắn nhãn 2, kiêm giữ hồ sơ:** điền `report/team/ho_so_launch_v0.md` từ đầu buổi; gắn nhãn 20 ca độc lập ở CP3.

## Phân công theo checkpoint

### Nguyên tắc

- **Đổi người viết code sau giải lao (15:35):** Lập viết code, Cường kiểm số. Nhờ vậy cả hai đều tự tay tính được chi phí.
- **Huy và Dũng không bàn về 20 ca lỗi trước CP3.** Hai bộ nhãn phải độc lập.
- **Mỗi file có một chủ file.** Chủ file chịu trách nhiệm file đúng tên, đủ mục và có nhãn `simulated`. Người khác có thể viết vào, chủ file soát lần cuối.
- **Huy giữ đồng hồ.** Hết giờ checkpoint mà chưa "Xong khi", Huy báo cả nhóm để quyết định cắt bớt hay làm tiếp.

### Chủ file

| File | Chủ file | Điểm |
| --- | --- | --- |
| `src/lab13.py` | Cường (đến 15:20), Lập (từ 15:35) | C1, C2, C4 |
| `report/team/bang_chi_phi.md` | Lập | C1 (20), C2 (15) |
| `report/team/bang_loi.md` | Huy | C3 (10) |
| `report/team/pilot_plan.yaml` | Cường | C4 (15), C8 (10) |
| `report/team/chi_so.md` | Lập | C5 (10) |
| `report/team/ho_so_launch_v0.md` | Dũng | C5, C6 (10), C7 (10) |
| `report/team/phieu_cham.md` | Dũng | Duyệt chéo |
| `report/team/group_report.md` | Lập | |
| `report/team/MSSV_HoTen.md` (bản của từng người) | Mỗi người tự viết | |

### 14:00–14:10 · Chuẩn bị

| Người | Việc | Xong khi |
| --- | --- | --- |
| Cường | Cài venv trong `src/`, chạy `python lab13.py` | Lệnh in `NotImplementedError` (đúng, chưa viết hàm) |
| Lập | Cài venv trên máy mình; mở `docs/du_lieu_va_cong_thuc.md` | Đọc được hai CSV với `keep_default_na=False` |
| Huy | Đọc `CHECKPOINTS.md`, ghi "Xong khi" của 5 CP ra giấy; đọc định nghĩa 5 loại Google PAIR (chưa đọc 20 ca) | Có danh sách "Xong khi" |
| Dũng | Mở `ho_so_launch_v0.md`, dựng khung 7 mục với cột số, trạng thái, người phụ trách | Khung 7 mục có sẵn |

### CP1 · A · Chi phí mỗi việc thành công (14:10–14:53, C1 = 20 điểm)

| Người | Việc | Ghi vào | Xong khi |
| --- | --- | --- | --- |
| Cường | A1: ba hàm ở `TODO CP1` (10 phút). A2: `mo_hinh(runs, reqs, …)` (20 phút). A3: gọi lại cho từng `loai`. A4: cộng 40 triệu đ/tháng cho `noi_dia` + `hang_nang` | `src/lab13.py` | In "Ba phép thử đáp án biết trước: ĐẠT" (1,20 · 1,25 · 1,25) |
| Lập | Tính tay độc lập hoá đơn token + tool chia số yêu cầu, và số việc thành công. So với số Cường in ra. Điền bảng A2 (9 dòng), A3 (4 dòng), A4 | `bang_chi_phi.md` | Số tay khớp số code; hai dòng xem lại, làm lại có nhãn `simulated` |
| Huy | Kiểm Cường không quên: tử số tính cả lần chạy lỗi, chia 1.000 trước khi nhân giá. Đối chiếu slide đáp án, lệch ≤ 2% | (soát) | Mọi số A2, A3 lệch ≤ 2% |
| Dũng | Viết 3 câu trả lời A2, A3 (≤ 3 dòng, có số). Ghi mục 1 (chi phí mỗi việc thành công) và mục 3 (so với 12.000 đ) vào hồ sơ | `bang_chi_phi.md`, `ho_so_launch_v0.md` | Mục 1, 3 có số, trạng thái "Giả lập", người phụ trách |

### CP2 · B · Độ nhạy (14:53–15:20, C2 = 15 điểm)

| Người | Việc | Ghi vào | Xong khi |
| --- | --- | --- | --- |
| Cường | Ở `TODO CP2`: gọi `mo_hinh` cho 9 kịch bản B1, cặp B2, giới hạn 1/2/3 lần chạy B3, xem lại 100% B4 | `src/lab13.py` | Code in đủ số của B1–B4 |
| Lập | Điền bảng B1 (9 dòng) và B3. Tự kiểm: "giảm một nửa" giảm đúng bằng nửa mức tăng của "gấp đôi". Tính tay B4 | `bang_chi_phi.md` | Bảng B1 đủ 9 dòng; tự kiểm tuyến tính đúng |
| Huy | Viết xếp hạng 3 yếu tố (B2) và câu trả lời B3, B4. B3 phải tính chi phí cả hệ thống, không chỉ chi phí mỗi việc | `bang_chi_phi.md` | Mỗi câu ≤ 3 dòng, có số, có nhãn `simulated` |
| Dũng | Ghi mục 2 (ba yếu tố nhạy nhất) vào hồ sơ. Nháp 2 dòng rủi ro kinh tế từ bảng B1 cho E2 | `ho_so_launch_v0.md`, `chi_so.md` | Mục 2 có số; có nháp 2 dòng rủi ro |

**15:20–15:35 · Giải lao.** Huy và Dũng không bàn về 20 ca lỗi.

### CP3 · C · Bảng lỗi (15:35–16:08, C3 = 10 điểm)

Từ đây Lập viết code, Cường kiểm số.

| Người | Việc | Ghi vào | Xong khi |
| --- | --- | --- | --- |
| Huy, Dũng | 8 phút: ngồi tách nhau, mỗi người gắn nhãn độc lập 20 ca trong `docs/Ngay13_Lab13_De_bai_hoc_vien.docx`. 3 phút: so nhãn, tính đồng thuận = số ca trùng ÷ 20. 5 phút: thống nhất ca lệch, mỗi ca một câu quy tắc | `bang_loi.md` | Hai bộ nhãn gốc giữ nguyên; đồng thuận ≥ 16/20 |
| Huy | 14 phút: điền bảng khắc phục 3 ca (Do người dùng, Hệ thống, Ngữ cảnh) | `bang_loi.md` | Mỗi dòng có event, ngưỡng, tần suất, một vai trò phụ trách |
| Dũng | 14 phút: điền bảng khắc phục 2 ca (Giới hạn hệ thống, Ngầm). Ghi mục 5 vào hồ sơ | `bang_loi.md`, `ho_so_launch_v0.md` | Đủ 5 loại; mục 5 có tỉ lệ đồng thuận |
| Lập | Hoàn thiện phần CP2 còn thiếu. Chuẩn bị `TODO CP4`: hàm cỡ mẫu, tính `reqs.mo_lai_trong_7_ngay.mean()` | `src/lab13.py` | Có tỉ lệ mở lại 7 ngày |
| Cường | Soát `bang_chi_phi.md`: nhãn `simulated`, mỗi câu ≤ 3 dòng. Đọc trước phần D1 trong `docs/Lab13_Huong_dan_chi_tiet_buoi_chieu.md` | `bang_chi_phi.md` | File A, B sạch, sẵn sàng chấm |

### CP4 · D · Pilot plan (16:08–16:36, C4 = 15 điểm, C8 = 10 điểm)

| Người | Việc | Ghi vào | Xong khi |
| --- | --- | --- | --- |
| Lập | D1 a–e ở `TODO CP4`: theo yêu cầu, theo nhân viên (m = 75), 20 người mỗi nhóm, 6 depot mỗi nhóm, chênh 6 điểm | `src/lab13.py` | Code in đủ 5 số D1 |
| Cường | Tính tay đối chiếu DE = 1 + (m − 1) × ICC và cỡ mẫu hiệu dụng. Ghi D1, D2 vào chú thích đầu file. Chọn cách chia, ghi đánh đổi (power ở 5 điểm) | `pilot_plan.yaml` | Cách chia có ≥ 20 cụm mỗi nhóm hoặc ghi rõ đánh đổi |
| Huy | D2: năm câu "tách được tác động", mỗi câu một dòng | `pilot_plan.yaml` | Đủ 5 câu |
| Dũng | D3: ít nhất 3 luật dừng (an toàn, chi phí, mức dùng), đủ 4 vế NẾU – TRONG – THÌ – KHÔNG THÌ, người dừng là một vai trò. Luật an toàn dùng tỉ lệ mở lại Lập tính. Ghi mục 6 vào hồ sơ | `pilot_plan.yaml`, `ho_so_launch_v0.md` | 3 luật đủ 4 vế; mục 6 có số |
| Cường | Chạy `yaml.safe_load` và lệnh tìm `?` ngoài chú thích (xem `CHECKPOINTS.md`) | (soát) | Đọc được, không còn `?` |

### CP5 · E · Chỉ số, rủi ro, hồ sơ (16:36–17:00, C5 = 10 điểm)

| Người | Việc | Ghi vào | Xong khi |
| --- | --- | --- | --- |
| Lập | E1: tính thử 3 chỉ số (chính, dùng, an toàn). Đề xuất thêm 1 chỉ số dùng, 1 chỉ số an toàn | `chi_so.md` | 3 chỉ số có số, viết "chỉ số trong đợt chạy thử là…" |
| Cường | Liệt kê ít nhất 6 event có `trace_id`. Kiểm mỗi chỉ số tính được từ danh sách event | `chi_so.md` | Mỗi chỉ số trỏ tới event dùng để tính |
| Huy | E2: hoàn thiện ít nhất 2 dòng rủi ro kinh tế từ nháp của Dũng, mỗi dòng có số từ bảng độ nhạy và một vai trò phụ trách | `chi_so.md` | 2 dòng rủi ro có số `simulated` |
| Dũng | E3: điền đủ 7 mục hồ sơ (mục 4 chỉ số, mục 7 rủi ro). Mỗi mục có số, trạng thái, người phụ trách. Dòng cuối: Go, Go có điều kiện hoặc No-go, nêu cả con số bất lợi. Chạy `grep -rni production report/team` | `ho_so_launch_v0.md` | 7 mục đủ; grep không in gì |

### 17:00–17:45 · Duyệt chéo Gate 2a (C6, C7, C8 = 30 điểm)

| Giờ | Lập | Cường | Huy | Dũng |
| --- | --- | --- | --- | --- |
| 17:00–17:10 | Soát số trong hồ sơ khớp `bang_chi_phi.md` | Soát `pilot_plan.yaml` khớp mục 6 | Soát nhãn `simulated` toàn bộ hồ sơ | Gửi hồ sơ cho nhóm hội đồng |
| 17:10–17:25 | Chấm C6 cho nhóm n + 1 | Chấm C7 | Chấm C8, viết một câu hỏi | Tổng hợp quyết định, lý do vào `phieu_cham.md` |
| 17:25–17:40 | Trả lời câu hỏi về số chi phí | Trả lời câu hỏi về pilot | Ghi lại câu hỏi và nhận xét | Trình bày hồ sơ 1 phút |

### 17:45–18:00 · Đóng gói và nộp

| Người | Việc |
| --- | --- |
| Lập | Điền `group_report.md`, commit, push, ghi commit chốt vào `TEAM.md` |
| Cường | Clone sạch, chạy `cd src && python3 lab13.py` trên một máy khác, ba phép thử A1 in ĐẠT |
| Huy | Soát checklist trong `SUBMISSION.md` |
| Dũng | Soát sáu file hồ sơ đúng tên trong `report/team/`, không còn `?`, không có "production" |
| Cả 4 người | Tự viết file `report/team/MSSV_HoTen.md` của mình, tự nộp link repo nhóm trên LMS trước 23h59 |

## Cá nhân

Mỗi thành viên đồng thời tạo một báo cáo riêng trong `report/` theo dạng:

```text
report/team/MSSV_HoTen.md
```

Ví dụ: `report/team/20241234_NguyenVanAn.md`.

## LyThanhLap-2A202603414

### Phần việc phụ trách

- Người kiểm số (14:00–15:20), người viết code (từ 15:35).
- Chủ file `bang_chi_phi.md`, `chi_so.md`, `group_report.md`.
- CP1–CP2: tính tay đối chiếu, điền bảng A2, A3, A4, B1, B3.
- CP4–CP5: viết code D1 và 3 chỉ số E1.
- Commit, push bản cuối.

### Đóng góp cụ thể

- CP1–CP2: kiểm số độc lập A1–A4 và B1–B4 bằng script riêng, không gọi `mo_hinh`. Mọi số khớp `src/lab13.py`, lệch dưới 0,01%. Tự kiểm tuyến tính B1: tỉ số tăng ÷ giảm = 2,000 ở cả ba cặp.
- CP4: viết `co_mau`, `he_so_thiet_ke`, `m_toi_thieu`, `in_bang_d1` và `in_ti_le_mo_lai` trong `src/lab13.py`. Kết quả: 1.251; DE 2,48 → 3.103 mỗi nhóm; tối đa 1.000; tối đa 300; m ≥ 299 (DE 6,96); power 0,64 ở 5 điểm; tỉ lệ mở lại 4,25% và 3,97% trong phạm vi.
- CP5: viết `in_bang_e1` và tính thử 3 chỉ số (82,83% · 27,12% · 4,25%). Điền E1, 11 event và phần kiểm tra chéo trong `chi_so.md`.
- Soạn nháp `pilot_plan.yaml` và mục 4, 6, 7 cùng dòng đề xuất của `ho_so_launch_v0.md` để chủ file (Cường, Dũng) soát. Điền `group_report.md`.

### Bằng chứng

- Commit `6558362` (bảng chi phí phần A), `333975a` (CP2 B1, B3).
- `src/lab13.py`: các hàm D1 và E1; `python lab13.py` in đủ A1 → E1.
- `report/team/bang_chi_phi.md`: bảng tự kiểm tuyến tính và ghi chú "Kiểm số độc lập".
- `report/team/chi_so.md`, `report/team/pilot_plan.yaml`, `report/team/group_report.md`.

## NguyenTienCuong-2A202603425

### Phần việc phụ trách

- Người viết code (14:00–15:20), người kiểm số (từ 15:35).
- Chủ file `src/lab13.py` đến giải lao, chủ file `pilot_plan.yaml`.
- CP1–CP2: viết ba hàm A1, `mo_hinh`, A3, A4 và các kịch bản B1–B4.
- CP4–CP5: tính tay đối chiếu D1, chọn cách chia; liệt kê 6 event có `trace_id`.
- Chạy lại `lab13.py` trên một máy khác trước khi nộp.

### Đóng góp cụ thể

- Chuẩn bị & CP1–CP2 (`src/lab13.py`, commit `aa93465`): cài đặt `src/.venv`, viết 3 hàm A1 đạt 100% (`1,20 · 1,25 · 1,25`), viết `mo_hinh()` cộng mọi lần chạy kể cả lỗi (đọc CSV với `keep_default_na=False`), triển khai A3 (`noi_dia` `0,22×`, `hang_nang` `0,69×`, `doi_tac` `0,85×`, `quoc_te` `1,88×` kèm tỉ lệ `ok` theo lần thử), A4 (cố định 40 triệu đ/tháng cho `noi_dia` + `hang_nang`: `4.599 đ = 0,38×` ở 45.000 yc/tháng, `5.784 đ = 0,48×` ở 22.500 yc/tháng), 9 kịch bản B1, cặp tuyến tính B2 (`6.543 đ`, `+46,3%`, top 3: làm lại, xem lại, lương NV), chi phí cả hệ thống B3 (2 lần rẻ nhất `6.901.220 đ`) và kịch bản xem lại 100% B4 ở cả 2 mức phút làm lại (`9,0` phút → `11.743 đ = 0,98×`; `15,3` phút → `12.415 đ = 1,03×`, hoà vốn ≤ `4,8–5,1` phút) (`simulated`).
- CP3–CP5 (vai Người kiểm số & Chủ file `pilot_plan.yaml`): đối chiếu `bang_chi_phi.md` khớp 0% với `src/lab13.py`, đủ nhãn `simulated`; chạy kiểm chứng toàn bộ `src/lab13.py` bản cuối từ A1 đến E1; tính tay đối chiếu D1 câu e (`m ≥ 299`, `DE = 6,96`), soát `pilot_plan.yaml` (`yaml.safe_load` hợp lệ, không còn `?` ngoài chú thích, đủ 3 luật dừng 4 vế) và đối chiếu 11 event + kiểm tra chéo trong `chi_so.md`; kiểm tra không có từ cấm trong `report/team/`.

### Bằng chứng

- Commit `aa93465` (`feat(lab13): implement CP1 (A1-A4) and CP2 (B1-B4) in src/lab13.py`).
- Báo cáo cá nhân: [report/team/2A202603425_NguyenTienCuong.md](report/team/2A202603425_NguyenTienCuong.md)
- Code & chạy kiểm chứng A1–E1: [src/lab13.py](src/lab13.py)
- Kế hoạch pilot đã soát: [report/team/pilot_plan.yaml](report/team/pilot_plan.yaml)

## NguyenVanHuy-2A202603432

### Phần việc phụ trách

- Người gắn nhãn 1, giữ đồng hồ và theo dõi "Xong khi" của từng checkpoint.
- Chủ file `bang_loi.md`.
- CP1–CP2: đối chiếu slide đáp án; viết xếp hạng B2 và câu trả lời B3, B4.
- CP3: gắn nhãn độc lập 20 ca, điền 3 dòng khắc phục.
- CP4–CP5: viết năm câu D2; hoàn thiện 2 dòng rủi ro kinh tế.
- Soát checklist `SUBMISSION.md` trước khi nộp.

### Đóng góp cụ thể

- CP1: soát `src/lab13.py`, xác nhận tử số tính cả lần chạy lỗi và chia 1.000 trước khi nhân giá. Đối chiếu đáp án: mọi số A2, A3 lệch 0% (ngưỡng 2%).
- CP1–CP2: điền `bang_chi_phi.md` (A1–A4, B1–B4). Viết xếp hạng B2 (làm lại +51,8% · xem lại +40,7% · lương +23,1%). Viết B3 theo chi phí cả hệ thống (giới hạn 2 lần rẻ nhất, 6.901.220 đ) và B4 (xem lại 100%: 0,98–1,03× của 12.000 đ). Tất cả là số `simulated`.
- CP3: gắn nhãn độc lập 20 ca (người gắn nhãn 1), đồng thuận với Dũng 18/20 = 90%. Điền 3 dòng khắc phục: ca 1 Do người dùng, ca 7 Hệ thống, ca 3 Ngữ cảnh.

### Bằng chứng

- File: `report/team/bang_chi_phi.md`, `report/team/bang_loi.md` (cột "Nhãn người 1" và 3 dòng khắc phục đầu), `report/team/2A202603432_NguyenVanHuy.md`.
- Commit: `eb7f3fb` (CP1), `313227f` (CP2), `7c626f6` (gắn nhãn 20 ca), `d211e79` (bảng khắc phục). Gộp vào `main` qua PR #1, #3, #5, #7.

## PhamCongDung-2A202603428

### Phần việc phụ trách

- Người gắn nhãn 2, kiêm giữ hồ sơ.
- Chủ file `ho_so_launch_v0.md`, `phieu_cham.md`.
- CP1–CP2: viết câu trả lời A2, A3; ghi mục 1, 2, 3 hồ sơ; nháp 2 dòng rủi ro.
- CP3: gắn nhãn độc lập 20 ca, điền 2 dòng khắc phục, ghi mục 5.
- CP4–CP5: viết ít nhất 3 luật dừng; điền đủ 7 mục hồ sơ và dòng đề xuất.
- Gửi hồ sơ cho hội đồng, trình bày lúc duyệt chéo.

### Đóng góp cụ thể

- CP1: Viết các câu trả lời phân tích A2 (so sánh 4.472 đ gấp 16,3× hoá đơn 274,7 đ; tỉ trọng làm lại 51,8%, xem lại 40,7%; chi phí cả hệ thống 5.865 đ = 0,49× của 12.000 đ), A3 (loại `quoc_te` 22.515 đ = 1,88× vì chạy lại 3 lần tỉ lệ ok giảm 30,0% → 11,4% → 2,2%; loại `doi_tac` 0,85×) và A4 (cộng cố định 40 triệu đ/tháng cho `noi_dia` + `hang_nang`: 4.599 đ = 0,38× ở 45.000 yc/tháng; 5.784 đ = 0,48× ở 22.500 yc/tháng) trong `report/team/bang_chi_phi.md`. Dựng khung 7 mục và điền Mục 1, Mục 3 vào `report/team/ho_so_launch_v0.md`.
- CP2: Điền hoàn chỉnh Mục 2 (Ba yếu tố nhạy nhất: 1. Số ca làm lại +51,8% · 2. Tỉ lệ xem lại +40,7% · 3. Lương nhân viên +23,1%; kiểm chứng cộng tuyến tính cặp token ×2 + xem lại ×2 = +46,3%) và cập nhật giới hạn 2 lần chạy (chi phí hệ thống rẻ nhất 6.901.220 đ) vào `report/team/ho_so_launch_v0.md`. Soạn 3 dòng rủi ro kinh tế (làm lại ×2 lên 6.787 đ; xem lại 100% kéo dài lên 11.743 đ = 0,98× hoặc 12.415 đ = 1,03×; khối lượng giảm một nửa làm cố định/việc tăng gấp đôi) trong `report/team/chi_so.md` (mục E2).
- CP3: Gắn nhãn độc lập 20 ca lỗi (Người gắn nhãn 2), đối chiếu với Huy đạt đồng thuận 18/20 ca (90%), thống nhất và viết quy tắc phân biệt nguyên nhân gốc cho 2 ca lệch (Ca 6 → Do người dùng; Ca 13 → Giới hạn hệ thống); điền phương án phát hiện và khắc phục cho Ca 4 (Giới hạn hệ thống) và Ca 17 (Ngầm) trong `report/team/bang_loi.md`; cập nhật Mục 5 vào `report/team/ho_so_launch_v0.md`.

### Bằng chứng

- Báo cáo cá nhân: [report/team/2A202603428_PhamCongDung.md](report/team/2A202603428_PhamCongDung.md)
- Hồ sơ launch v0 (Mục 1, 2, 3): [report/team/ho_so_launch_v0.md](report/team/ho_so_launch_v0.md)
- Câu trả lời phân tích A2, A3, A4: [report/team/bang_chi_phi.md](report/team/bang_chi_phi.md)
- Bảng rủi ro kinh tế E2: [report/team/chi_so.md](report/team/chi_so.md)
