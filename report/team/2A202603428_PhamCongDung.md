# Báo cáo cá nhân — PhamCongDung-2A202603428

## 1. Thông tin thành viên

- Họ tên: Phạm Công Dũng
- MSSV: 2A202603428
- Lớp: L3A · Nhóm: Neon
- Vai trong nhóm: Người gắn nhãn 2, kiêm giữ hồ sơ (`report/team/ho_so_launch_v0.md`, `report/team/phieu_cham.md`)

## 2. Phần việc phụ trách

- **Chuẩn bị (14:00–14:10):** Mở `report/team/ho_so_launch_v0.md`, dựng khung 7 mục với các cột: Con số chính, Trạng thái, Người phụ trách.
- **CP1 (Nhiệm vụ A):** Viết 3 câu trả lời phân tích cho A2, A3, A4 (mỗi câu ≤ 3 dòng, có con số cụ thể và nhãn `simulated`) trong `report/team/bang_chi_phi.md`. Ghi Mục 1 (Chi phí mỗi việc thành công) và Mục 3 (So với nhân viên tự làm 12.000 đ) vào `report/team/ho_so_launch_v0.md`.
- **CP2 (Nhiệm vụ B):** Ghi Mục 2 (Ba yếu tố nhạy nhất) vào `report/team/ho_so_launch_v0.md`; soạn nháp các dòng rủi ro kinh tế từ bảng độ nhạy B1/B4 vào `report/team/chi_so.md` (mục E2).
- **CP3 (Nhiệm vụ C):** Gắn nhãn độc lập 20 ca lỗi theo 5 loại Google PAIR, đối chiếu đồng thuận với Huy, điền 2 dòng khắc phục (Giới hạn hệ thống, Ngầm) trong `report/team/bang_loi.md` và cập nhật Mục 5 hồ sơ.
- **CP4–CP5 (Nhiệm vụ D, E & Duyệt chéo):** Viết 3 luật dừng (NẾU – TRONG – THÌ – KHÔNG THÌ) vào `report/team/pilot_plan.yaml`, hoàn thiện đủ 7 mục + dòng đề xuất trong `report/team/ho_so_launch_v0.md`, kiểm tra không chứa từ cấm và tổng hợp `report/team/phieu_cham.md`.

## 3. Đóng góp cụ thể

**Tại CP1 (Nhiệm vụ A — Mô hình chi phí mỗi việc thành công):**

- **Viết câu trả lời A2 trong `report/team/bang_chi_phi.md`:**
  - Chỉ ra chi phí mỗi việc thành công là **4.472 đ** (`simulated`), gấp **16,3 lần** hoá đơn token + tool chia số yêu cầu (**274,7 đ**).
  - Xác định khoản chiếm tỉ trọng lớn nhất là **làm lại (51,8% = 2.264.000 đ)** và **xem lại (40,7% = 1.780.000 đ)**; tổng giờ nhân viên chiếm **92,5%** tổng chi phí (`simulated`).
  - Nêu phép so sánh công bằng với baseline 12.000 đ của nhân viên: khi cộng thêm 222 ca không thành công (`148 chuyen_nhan_vien + 74 lam_lai`) × 12.000 đ, chi phí cả hệ thống là **5.865 đ/yêu cầu = 0,49×** của 12.000 đ (`simulated`).
- **Viết câu trả lời A3 & A4 trong `report/team/bang_chi_phi.md`:**
  - Phân tích bảng tách theo loại yêu cầu: kết luận loại **`quoc_te`** không đáng để trợ lý xử lý vì tỉ lệ thành công chỉ **27,3%**, chi phí **22.515 đ = 1,88×** của 12.000 đ (`simulated`). Giải thích việc cho chạy lại tới 3 lần không giúp ích vì tỉ lệ `status == 'ok'` của `quoc_te` giảm mạnh qua từng lần thử (lần 1: **30,0%**, lần 2: **11,4%**, lần 3: **2,2%**) do lỗi lặp lại trên cùng yêu cầu. Đề xuất loại cả `quoc_te` và `doi_tac` (**10.215 đ = 0,85×**, có điều khoản riêng) khỏi phạm vi pilot.
  - Phân tích chi phí cố định 40 triệu đ/tháng trên phạm vi `noi_dia` + `hang_nang` (biến đổi **3.414 đ/việc**, 900/1.200 việc thành công): ở quy mô 45.000 yêu cầu/tháng (33.750 việc thành công), cố định là **1.185 đ/việc** → tổng **4.599 đ = 0,38×** (`simulated`); ở một nửa khối lượng (22.500 yêu cầu/tháng), cố định tăng gấp đôi lên **2.370 đ/việc** → tổng **5.784 đ = 0,48×** (`simulated`).
- **Cập nhật `report/team/ho_so_launch_v0.md` (Mục 1, Mục 3):**
  - Điền Mục 1 (Chi phí mỗi việc thành công: 4.472 đ toàn mẫu; 3.414 đ biến đổi và 4.599 đ có cố định cho phạm vi pilot, trạng thái `Giả lập`, phụ trách: `PM trợ lý hoàn phí`).
  - Điền Mục 3 (So với nhân viên tự làm 12.000 đ: cả hệ thống 5.865 đ = 0,49×; thu hẹp phạm vi pilot về `noi_dia` 0,22× và `hang_nang` 0,69×, trạng thái `Giả lập`, phụ trách: `Giám đốc vận hành LogiX-VN`).

**Tại CP2 (Nhiệm vụ B — Bảng độ nhạy & Nháp rủi ro kinh tế):**

- **Ghi Mục 2 (Ba yếu tố nhạy nhất) vào `report/team/ho_so_launch_v0.md`:**
  - Tổng hợp từ bảng độ nhạy B1 & B2: Xếp hạng 3 yếu tố làm chi phí mỗi việc thành công thay đổi mạnh nhất là **1. Số ca làm lại** (gấp đôi → **6.787 đ, +51,8%**, giảm một nửa → **3.315 đ, −25,9%** `simulated`) · **2. Tỉ lệ xem lại** (gấp đôi → **6.292 đ, +40,7%**, giảm một nửa → **3.562 đ, −20,3%** `simulated`) · **3. Lương nhân viên** (tăng 25% → **5.506 đ, +23,1%** `simulated`).
  - Đối chiếu kịch bản đổi cặp B2 (Giá token ×2 + Tỉ lệ xem lại ×2 → **6.543 đ, +46,3%** `simulated`, bằng đúng tổng hai tác động riêng `+5,6% + 40,7%` do mô hình cộng tuyến tính) và kịch bản giới hạn chạy lại B3 (giới hạn **2 lần chạy** giúp tổng chi phí cả hệ thống rẻ nhất cho công ty ở mức **6.901.220 đ** `simulated`, tiết kiệm 136.365 đ so với 3 lần và 548.561 đ so với 1 lần).
  - Gán trạng thái `Giả lập` và người phụ trách là `PM trợ lý hoàn phí`.
- **Soạn nháp bảng Rủi ro kinh tế (cho mục E2) trong `report/team/chi_so.md` từ số liệu bảng độ nhạy B1 & B4:**
  - **Rủi ro 1 (Số ca làm lại tăng gấp đôi):** Tác động làm chi phí mỗi việc thành công tăng **+51,8%** (từ 4.472 đ lên **6.787 đ**, `simulated`). Dấu hiệu theo dõi: tỉ lệ làm lại theo tuần > 7% (so với 4,9% trong đợt chạy thử ở phạm vi `noi_dia` + `hang_nang`). Hành động: thu hẹp pilot về `noi_dia` và rà soát 20 trace làm lại gần nhất. Phụ trách: `PM trợ lý hoàn phí`.
  - **Rủi ro 2 (Phải xem lại 100% kéo dài — từ kết quả B4):** Tác động làm chi phí trong phạm vi `noi_dia` + `hang_nang` tăng lên **11.743 đ = 0,98×** của 12.000 đ (hoặc **12.415 đ = 1,03×** nếu dùng phút làm lại thực tế 15,3 phút/ca trong dữ liệu, `simulated`), mất toàn bộ lợi thế tiết kiệm. Dấu hiệu theo dõi: % yêu cầu được xem lại vẫn > 50% cuối bước rollout 0,25 hoặc thời gian xem lại > 4,8 phút/ca. Hành động: giảm tỉ lệ xem lại theo bậc khi tỉ lệ `sua` + `bo` < 15%. Phụ trách: `Trưởng nhóm CSKH`.
  - **Rủi ro 3 (Khối lượng thấp hơn dự kiến — từ kết quả A4):** Chi phí cố định 40 triệu đ/tháng làm cộng thêm **+1.185 đ/việc** ở 45.000 yc/tháng (**4.599 đ = 0,38×**, `simulated`) và tăng gấp đôi lên **+2.370 đ/việc** khi khối lượng giảm một nửa (**5.784 đ = 0,48×**, `simulated`). Phụ trách: `PM trợ lý hoàn phí`.

**Tại CP3 (Nhiệm vụ C — Bảng lỗi và cách khắc phục):**

- **Gắn nhãn độc lập 20 ca lỗi và đối chiếu đồng thuận trong `report/team/bang_loi.md`:**
  - Thực hiện gắn nhãn độc lập 20 ca lỗi (Người gắn nhãn 2: Phạm Công Dũng) trong 8 phút theo 5 loại của Google PAIR (Do người dùng, Hệ thống, Ngữ cảnh, Giới hạn hệ thống, Ngầm).
  - So nhãn với Người gắn nhãn 1 (Nguyễn Văn Huy): trùng **18/20 ca**, đạt **tỉ lệ đồng thuận 90%** (vượt ngưỡng yêu cầu ≥ 80%).
  - Thảo luận và ghi câu quy tắc phân biệt theo nguyên nhân gốc cho 2 ca lệch nhau:
    - **Ca 6:** Khách chọn mục "Hoàn phí giao trễ" nhưng mô tả hàng vỡ → thống nhất là **Do người dùng** (gốc lỗi từ thao tác chọn sai mục của khách; việc kiểm tra chéo nội dung thuộc bước khắc phục).
    - **Ca 13:** Khách hỏi bảo hiểm hàng hoá của đối tác ngoài phạm vi trợ lý → thống nhất là **Giới hạn hệ thống** (yêu cầu nằm ngoài phạm vi thiết kế thì gốc lỗi là giới hạn hệ thống, dù cách trợ lý trả lời chung chung cần được cải thiện).
- **Điền phương án khắc phục cho 2 loại lỗi phụ trách (Giới hạn hệ thống & Ngầm) trong `report/team/bang_loi.md` và cập nhật Mục 5 hồ sơ:**
  - **Ca 4 (Giới hạn hệ thống):** Phát hiện qua event `handoff_to_staff` với `reason == 'thieu_du_lieu'` (kèm `trace_id`), thống kê theo loại yêu cầu mỗi ngày (ngưỡng cảnh báo > 10%). Khắc phục: giữ cơ chế chuyển nhân viên kèm tóm tắt và loại `quoc_te` (1,88×, thành công 27,3%, `simulated`) khỏi phạm vi pilot. Phụ trách: `PM trợ lý hoàn phí`.
  - **Ca 17 (Ngầm):** Phát hiện qua event `audit_sample_checked` kiểm tra mẫu ngẫu nhiên 100 đơn hoàn/tuần đối chiếu bảng giá hiện hành (ngưỡng cảnh báo ≥ 1% đơn lệch tiền). Khắc phục: tự động xoá cache ngay khi bảng giá cập nhật và ghi `pricing_table_version` vào mọi `trace_id`. Phụ trách: `Kế toán trưởng`.
  - Cập nhật **Mục 5 (Bảng lỗi và cách khắc phục)** vào `report/team/ho_so_launch_v0.md` với tỉ lệ đồng thuận 90% (18/20), đủ 5 loại lỗi (ca 1, 7, 3, 4, 17), trạng thái `Xong, có bằng chứng`, người phụ trách `Kỹ sư trưởng agent`.

**Tại CP4 (Nhiệm vụ D — Luật dừng trong `pilot_plan.yaml` & Mục 6 hồ sơ):**

- **Viết 3 luật dừng (D3) đủ 4 vế NẾU – TRONG – THÌ – KHÔNG THÌ trong `report/team/pilot_plan.yaml`:**
  - **Luật dừng 1 (An toàn):** Dựa trên tỉ lệ `mo_lai_trong_7_ngay` hiện tại là **4,25%** toàn mẫu (51/1.200) và **3,97%** trong phạm vi `noi_dia` + `hang_nang` (39/982) — nếu đặt ngưỡng tuyệt đối 3% thì pilot sẽ dừng ngay tuần đầu. Do đó đặt luật: *NẾU tỉ lệ mở lại 7 ngày của nhóm trợ lý cao hơn đối chứng ≥ 2 điểm, hoặc vượt trần 6% (~1,5× mức 3,97%), hoặc có ≥ 1 ca hoàn trùng hay lệch sổ cái (ca 7, ca 20) TRONG 3 ngày liên tiếp THÌ Giám đốc vận hành ra lệnh tắt trợ lý trong 15 phút và Kỹ sư trưởng agent rà trace trong 24 giờ KHÔNG THÌ không được chuyển sang bước rollout tiếp theo*.
  - **Luật dừng 2 (Chi phí):** *NẾU chi phí mỗi việc thành công biến đổi trong phạm vi vượt **5.100 đ** (`simulated`, tương ứng kịch bản số ca làm lại tăng gấp đôi) TRONG 2 tuần liên tiếp THÌ PM trợ lý hoàn phí thu hẹp về `noi_dia` và giữ giới hạn tối đa 2 lần chạy KHÔNG THÌ không được giữ `hang_nang` trong phạm vi*.
  - **Luật dừng 3 (Mức độ sử dụng):** *NẾU tỉ lệ bỏ qua gợi ý (`sua + bo` trên số được xem lại) vượt **40%** (~1,5× mức 27,12% của đợt chạy thử) TRONG 1 tuần THÌ Trưởng nhóm CSKH phỏng vấn 5 nhân viên và gửi báo cáo trong 3 ngày KHÔNG THÌ không được chuyển sang bước rollout tiếp theo*.
- **Ghi Mục 6 (Pilot plan) vào `report/team/ho_so_launch_v0.md`:**
  - Tóm tắt thiết kế chia ngẫu nhiên theo nhân viên **20 + 20** phân tầng theo depot, chỉ chạy `noi_dia` + `hang_nang`, chấp nhận mức chênh phát hiện **6 điểm** (`n = 859` mỗi nhóm, `m ≥ 299` yêu cầu/người, `DE = 6,96`) do trần `20 / 0,02 = 1.000 < 1.251`, nêu rõ con số bất lợi **power = 0,64** nếu tác động thật chỉ 5 điểm, lộ trình rollout `0.10 → 0.25 → 0.50`, 3 luật dừng và ngày quyết định `2027-01-11` (trạng thái `Xong, có bằng chứng`, phụ trách `Giám đốc vận hành LogiX-VN`).

**Tại CP5 & Duyệt chéo Gate 2a (Nhiệm vụ E — Hoàn thiện `ho_so_launch_v0.md`, `phieu_cham.md` & Soát cuối):**

- **Hoàn thiện đủ 7 mục và dòng Đề xuất trong `report/team/ho_so_launch_v0.md`:**
  - Điền **Mục 4 (Chỉ số chính, dùng, an toàn)**: trong đợt chạy thử (chưa có đối chứng), chỉ số chính đạt **82,83%** (994/1.200), bỏ qua gợi ý **27,12%** (48/177), mở lại 7 ngày **4,25%** (51/1.200; **3,97%** trong phạm vi), kèm 2 chỉ số tự đề xuất và **11 event** có `trace_id` (trạng thái `Xong, có bằng chứng`, phụ trách `PM trợ lý hoàn phí`).
  - Điền **Mục 7 (Rủi ro kinh tế)**: tổng hợp 3 rủi ro từ bảng độ nhạy (số ca làm lại gấp đôi **+51,8%** lên **6.787 đ**; xem lại 100% kéo dài lên **11.743 đ = 0,98×** hoặc **12.415 đ = 1,03×** với 15,3 phút làm lại, hoà vốn ≤ 4,8–5,1 phút; khối lượng giảm một nửa làm cố định thành **+2.370 đ/việc**, tổng **5.784 đ = 0,48×**, `simulated`; trạng thái `Giả lập`, phụ trách `PM trợ lý hoàn phí`).
  - Chốt đề xuất cuối: **Go có điều kiện** cho phạm vi `noi_dia` + `hang_nang`, giới hạn tối đa 2 lần chạy, kèm 4 điều kiện tiên quyết có vai trò phụ trách và ngày kiểm tra cụ thể (sửa lỗi ca 7 & ca 20 trước 2026-12-04; Giám đốc vận hành ký chấp nhận MDE 6 điểm / power 0,64 trước 2026-12-04; bật đủ 11 event có `trace_id` để thay phút `simulated` bằng phút đo thật vào 2026-12-14; kế hoạch giảm xem lại theo bậc khi `sua + bo < 15%` trước 2026-12-14).
- **Tổng hợp phiếu chấm hội đồng Gate 2a trong `report/team/phieu_cham.md` và soát toàn bộ 6 file hồ sơ:**
  - Điền đầy đủ điểm và lý do có số liệu cho 3 tiêu chí C6, C7, C8, quyết định hội đồng, câu hỏi phản biện (về kịch bản xem lại 100% B4 và ngưỡng hoà vốn ≤ 4,8–5,1 phút) và câu trả lời tại buổi duyệt chéo trong `report/team/phieu_cham.md`.
  - Soát toàn bộ 6 file hồ sơ trong `report/team/` (`bang_chi_phi.md`, `bang_loi.md`, `pilot_plan.yaml`, `chi_so.md`, `ho_so_launch_v0.md`, `phieu_cham.md`): đúng tên file, không còn dấu `?` ngoài chú thích, đọc được bằng `yaml.safe_load`, và không chứa từ cấm theo Quy tắc 5.

## 4. Bằng chứng

- File hồ sơ tổng hợp (Chủ file): [report/team/ho_so_launch_v0.md](ho_so_launch_v0.md) (đủ 7 mục và đề xuất **Go có điều kiện** kèm 4 điều kiện, đầy đủ con số, nhãn `simulated`, trạng thái `Giả lập` / `Xong, có bằng chứng` và vai trò phụ trách).
- File phiếu chấm hội đồng Gate 2a (Chủ file): [report/team/phieu_cham.md](phieu_cham.md) (đủ bảng chấm 3 tiêu chí C6–C8 có số liệu, quyết định hội đồng, câu hỏi và câu trả lời duyệt chéo).
- File kế hoạch pilot: [report/team/pilot_plan.yaml](pilot_plan.yaml) (mục `stop_rules` gồm 3 luật dừng đủ 4 vế NẾU – TRONG – THÌ – KHÔNG THÌ; đọc hợp lệ bằng `yaml.safe_load`, không còn dấu `?`).
- File bảng lỗi: [report/team/bang_loi.md](bang_loi.md) (cột "Nhãn người 2" cho 20 ca lỗi đạt đồng thuận 18/20 = 90%, quy tắc phân biệt ca 6 & ca 13, và 2 dòng khắc phục Ca 4 Giới hạn hệ thống, Ca 17 Ngầm).
- File bảng chi phí & chỉ số: [report/team/bang_chi_phi.md](bang_chi_phi.md) (câu trả lời A2, A3, A4 ≤ 3 dòng), [report/team/chi_so.md](chi_so.md) (bảng E2 Rủi ro kinh tế).
- Kết quả chạy kiểm tra `python lab13.py` trong `src/` khớp 100% với toàn bộ con số trong hồ sơ.

## 5. Công cụ AI đã dùng

- **Antigravity (Gemini)** trong IDE, dùng để giải thích yêu cầu từng checkpoint, kiểm tra chéo các phép tính tỷ trọng chi phí ở CP1 (A2, A3, A4), rà soát quy tắc trình bày (≤ 3 dòng/câu, gắn nhãn `simulated`, không dùng từ cấm) và hỗ trợ tổng hợp nội dung vào `ho_so_launch_v0.md` và báo cáo cá nhân.
- **Cách tự kiểm tra:**
  - Tự tính tay kiểm chứng lại các con số trong câu trả lời A2–A4:
    - Tỉ lệ CPS so với hoá đơn/yêu cầu: `4.472 / 274,7 = 16,28 ≈ 16,3 lần`.
    - Tỉ trọng làm lại và xem lại: `2.264.000 / 4.373.585 = 51,77% ≈ 51,8%`; `1.780.000 / 4.373.585 = 40,70% ≈ 40,7%`.
    - Chi phí cả hệ thống trên mỗi yêu cầu: `(4.373.585 + 222 × 12.000) / 1.200 = 7.037.585 / 1.200 = 5.864,65 ≈ 5.865 đ (0,49×)`.
    - Chi phí cố định mỗi việc ở phạm vi `noi_dia` + `hang_nang`: `40.000.000 / (45.000 × 900 / 1.200) = 40.000.000 / 33.750 = 1.185,18 ≈ 1.185 đ`; cộng CPS biến đổi `3.413,90 + 1.185,18 = 4.599 đ (0,38×)`.
  - Tự kiểm tra số liệu độ nhạy ở CP2 (B1, B2, B4):
    - Tính cộng tuyến tính B2: `(4.723 − 4.472) + (6.292 − 4.472) = 251 + 1.820 = 2.071 đ` → `4.472 + 2.071 = 6.543 đ (+46,3%)`, khớp với `+5,6% + 40,7% = +46,3%`.
    - Kịch bản xem lại 100% (B4) trên `noi_dia` + `hang_nang`: `948 ca có ≥1 lần ok × 5 phút × 2.000 đ = 9.480.000 đ`; `48 ca làm lại × 9 phút × 2.000 đ = 864.000 đ`; cộng token+tool `224.513 đ` = `10.568.513 đ / 900 việc = 11.743 đ (0,98×)`. Với trung bình thực tế `15,3125 phút/ca làm lại`: `(9.480.000 + 48 × 15,3125 × 2.000 + 224.513) / 900 = 11.174.513 / 900 = 12.416 đ ≈ 12.415 đ (1,03×)`.
  - Kiểm tra định dạng và soát hồ sơ cuối (CP4–CP5):
    - Kiểm tra tỉ lệ mở lại 7 ngày dùng cho luật dừng an toàn: `51 / 1.200 = 4,25%` toàn mẫu; `39 / 982 = 3,97%` trong phạm vi `noi_dia` + `hang_nang` → xác nhận ngưỡng tuyệt đối 3% không khả thi, phải dùng ngưỡng so với đối chứng (+2 điểm) và trần 6%.
    - Chạy kiểm tra `yaml.safe_load` cho `report/team/pilot_plan.yaml` (với `PYTHONUTF8=1`) không báo lỗi, không còn dấu `?` ngoài các dòng chú thích `#`.
    - Rà soát 7 mục trong `report/team/ho_so_launch_v0.md`: mọi mục dựa trên cột `*_simulated` (Mục 1, 2, 3, 7) đều ghi trạng thái `Giả lập`, các mục 4, 5, 6 ghi `Xong, có bằng chứng`; không có mục nào ghi người phụ trách là "cả đội"; chạy tìm kiếm xác nhận không xuất hiện từ cấm theo Quy tắc 5 trong toàn bộ `report/team/`.

## 6. Tự đánh giá

- Hoàn thành đầy đủ nhiệm vụ của vai **Người gắn nhãn 2 kiêm giữ hồ sơ** xuyên suốt từ CP1 đến CP5 và Duyệt chéo Gate 2a: chủ trì hoàn thiện `report/team/ho_so_launch_v0.md` (7 mục + đề xuất **Go có điều kiện**) và `report/team/phieu_cham.md`, đóng góp câu trả lời A2–A4 trong `bang_chi_phi.md`, bộ nhãn độc lập 20 ca + 2 dòng khắc phục trong `bang_loi.md`, 3 luật dừng 4 vế trong `pilot_plan.yaml`, và 3 dòng rủi ro kinh tế trong `chi_so.md`.
- Bài học rút ra:
  - Khi đánh giá kinh tế một AI Agent để trình duyệt Gate 2a, không được nhìn vào hoá đơn token chia đầu yêu cầu (274,7 đ) hay chỉ chia cho số ca thành công mà bỏ quên chi phí nhân viên xử lý các ca chuyển giao/làm lại (giờ nhân viên chiếm 92,5% chi phí). Bóc tách chi phí theo phân khúc (`loai`) giúp loại bỏ sớm phân khúc gây lỗ (`quoc_te` 1,88×).
  - Một hồ sơ Gate 2a thuyết phục không phải là hồ sơ che giấu điểm yếu để xin "Go", mà phải chỉ ra rõ các con số bất lợi (power giảm còn 0,64 ở mức 5 điểm khi chia 20 + 20 nhân viên; xem lại 100% làm chi phí chạm 0,98×–1,03×; các lỗi hệ thống ca 7, ca 20 và lỗi ngầm ca 17) kèm theo điều kiện tiên quyết, luật dừng định lượng và người chịu trách nhiệm rõ ràng.
