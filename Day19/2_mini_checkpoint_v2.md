# Mini Checkpoint V2 — Stress-test Q&A với nhà đầu tư

## Sản phẩm: TA_Chatbot — AI Trợ Giảng Hybrid

---

## Hướng dẫn
Đây là một phiên mô phỏng với nhà đầu tư. Mỗi câu hỏi kiểm tra một điểm yếu trong pitch. Trả lời ngắn gọn bằng dữ liệu từ Day 16-18.

---

## Q1. "SAM của bạn chỉ 240 users. Quá nhỏ. Làm sao thành business tầm venture?"

**Trả lời:**
SAM 240 là **beachhead năm 1**, không phải quy mô thị trường toàn phần. Lộ trình mở rộng:

1. **Năm 2:** Mở rộng toàn bộ 4 năm CS tại VinUni → ~1,000 sinh viên (4x SAM)
2. **Năm 3:** Mở rộng sang các khoa khác tại VinUni (Toán, Vật lý, Kỹ thuật) → ~5,000 sinh viên
3. **Năm 4+:** Cấp phép cho các đại học Việt Nam (~200 trường × 350 trung bình = 70,000 sinh viên TAM)

Pilot 240 users cố tình nhỏ để **giảm rủi ro trước khi scale**. VinUniversity là **khách hàng tham chiếu** — khi chứng minh giảm 60% workload TA và >70% hài lòng sinh viên, các trường khác sẽ theo.

**Business thật là B2B SaaS licensing** với mức $5-10/sinh viên/năm cho đại học. TAM: 70,000 sinh viên × $7.5 trung bình = **$525K doanh thu định kỳ/năm** khi thâm nhập đầy đủ — và mới chỉ là Việt Nam.

---

## Q2. "Vì sao ChatGPT không chỉ thêm upload tài liệu và giết bạn?"

**Trả lời:**
Có 2 lý do cấu trúc khiến ChatGPT khó cạnh tranh trực tiếp:

**1. Tuân thủ PDPA / Data residency (moat thật):**
Đại học Việt Nam không thể gửi PII của sinh viên (tên, MSSV, bài nộp code) lên server của OpenAI — vi phạm PDPA. ChatGPT là pure cloud. Chúng tôi dùng **triển khai hybrid**: LLM on-prem xử lý PII, chỉ gửi query đã ẩn danh lên cloud. OpenAI phải tự xây hạ tầng on-prem cho Việt Nam — rất tốn kém với ROI thấp.

**2. RAG bám theo môn học cần quyền truy cập tổ chức:**
Chúng tôi tích hợp trực tiếp với LMS (Canvas) và tài liệu môn. ChatGPT không có tích hợp này. Để làm được cần:
- Thỏa thuận hợp tác với đại học
- Pipeline ingest theo cấu trúc môn học
- Quy trình xác thực bởi TA

Việc này cần 6-12 tháng xây quan hệ cho mỗi trường. Chúng tôi đã có 2 học kỳ ở VinUni.

**Kết luận:** ChatGPT cạnh tranh bằng chất lượng model. Chúng tôi cạnh tranh bằng **tuân thủ + tích hợp + tính đặc thù theo môn** — 3 thứ OpenAI không có động cơ làm cho một thị trường đại học của một quốc gia.

---

## Q3. "Unit economics giả định ARPU 500K VND. Ai trả — sinh viên hay trường?"

**Trả lời:**
**Đại học trả**, không phải sinh viên. Lý do bền vững:

**Bài toán chi phí:**
- Hiện tại: 50 TA × 20 giờ/tuần × 50 tuần × 250,000 VND/giờ = **125M VND/năm** (chi phí nhân sự TA)
- TA_Chatbot giảm 60% workload lặp lại → **tiết kiệm 75M VND/năm**
- Chi phí của chúng tôi: 240 sinh viên × 500K VND × 12 tháng = **1.44B VND/năm**

**Khoan — cao hơn tiết kiệm?** Đúng. Insight quan trọng: **TA_Chatbot không phải công cụ tiết kiệm chi phí, mà là nâng chất lượng.**

Giá trị thật:
1. **Cải thiện kết quả học** → NPS cao hơn, thứ hạng tốt hơn cho VinUni
2. **Tái phân bổ thời gian TA** → TA làm mentoring giá trị cao, tăng output nghiên cứu
3. **Khả dụng 24/7** → giảm xin gia hạn deadline, tăng tỉ lệ tốt nghiệp

Đại học trả cho kết quả học tập, không chỉ tiết kiệm chi phí. Học phí VinUni khoảng ~$15,000/sinh viên — chi phí 1.44B VND (~$57K) cho 240 sinh viên chỉ **0.38% doanh thu học phí**. Đây là khoản ngân sách dễ duyệt.

---

## Q4. "Kịch bản bi quan vẫn 44 tháng runway. Không thực tế. Worst case thật là gì?"

**Trả lời:**
Bạn nói đúng. 44 tháng runway trong mô hình Day 18 giả định **steady-state operations**. Worst case thực tế:

**Kịch bản bi quan thật ("Kill Switch"):**
1. **Adoption thất bại:** Chỉ 20% sinh viên dùng (không phải 80%) → Gross Profit giảm còn 10.8M VND/tháng
2. **Churn tăng:** 8%/tháng (rơi sau kỳ giữa) → LTV giảm 60%
3. **Trường từ chối trả:** VinUni chặn mọi AI xử lý PII → **0 doanh thu, dự án dừng**
4. **Đối thủ xuất hiện:** Edtech VN ra bản pure cloud, phá giá 200K VND/sinh viên → price war

**Tác động tài chính:**
- Gross Profit: 10.8M VND/tháng
- Fixed costs: 100M VND/tháng (gồm chi phí pivot khẩn)
- **Burn mỗi tháng: -89.2M VND**
- Tiền mặt ban đầu: 2.5B VND → **Runway: ~28 tháng**

Vẫn > 12 tháng nhưng chặt hơn nhiều. **Rủi ro thật không phải tài chính — mà là chính sách.** Nếu VinUni xem AI vi phạm học thuật, dự án chết bất kể runway.

**Giảm rủi ro:** Pilot 50 sinh viên trước (Tháng 1-3), đo adoption + hài lòng rồi mới scale. Nếu adoption < 40%, pivot sang B2C để sinh viên trả trực tiếp.

---

## Q5. "Bạn xây hybrid để tuân thủ PDPA. Độ phức tạp kỹ thuật gấp đôi. Sao không dùng cloud và xin lỗi sau?"

**Trả lời:**
Vì **đó là vi phạm pháp luật**, và đại học Việt Nam rất nghiêm về PDPA.

**Thực tế pháp lý:**
- PDPA (Nghị định 13/2023) yêu cầu **đồng ý rõ ràng** và **lưu trữ dữ liệu nội địa** với PII
- Bài nộp code chứa: tên, MSSV, email, dữ liệu học tập
- Gửi lên server OpenAI tại Mỹ = **chuyển dữ liệu xuyên biên giới không phép** = phạt + rủi ro pháp lý

**Hệ quả thực:** Nếu VinUni bị audit và vi phạm PDPA:
- Phạt: đến 5% doanh thu năm
- Mất uy tín: rủi ro mất kiểm định quốc tế
- Khiếu kiện: rò rỉ PII

**Không CTO đại học nào chấp nhận cách “xin lỗi sau”.** Họ thà không dùng AI còn hơn vi phạm PDPA.

**Chi phí kỹ thuật là xứng đáng:** Hybrid phức tạp hơn thật, nhưng cũng là **moat**. Đối thủ dùng pure cloud dễ làm hơn nhưng bị chặn về pháp lý. Chúng tôi xây **giải pháp tuân thủ duy nhất** — đáng để đầu tư.

---

## Q6. "LTV/CAC 28.38 trông quá đẹp. Bẫy nằm ở đâu?"

**Trả lời:**
"Bẫy" là **CAC hiện tại bị thấp giả tạo** vì chưa tính đủ chi phí acquisition thật:

**CAC hiện tại (500K VND) chỉ gồm:**
- Thời gian TA endorsement
- Công sức tích hợp LMS
- Tài liệu demo orientation

**Chưa tính (nhưng nên tính):**
1. **Chi phí sales cycle:** 3-6 tháng xây quan hệ với ban giám hiệu → ~50M VND thời gian founder
2. **Chi phí pháp lý/tuân thủ:** audit PDPA, review data residency → ~30M VND
3. **Chi phí pilot:** pilot miễn phí 50 sinh viên trong 3 tháng → ~15M VND

**CAC điều chỉnh:** (500K × 240) + 50M + 30M + 15M = 215M VND tổng  
**CAC điều chỉnh mỗi user:** 215M / 240 = **~896K VND** (không phải 500K)

**LTV/CAC điều chỉnh:** 14,190K / 896K = **15.84** — vẫn rất tốt (>3) nhưng thực tế hơn.

**Thành thật:** Startup giai đoạn sớm thường đánh giá thấp CAC. Con số 28.38 đúng về hướng (unit economics tốt) nhưng độ chính xác dễ gây hiểu lầm. Nhà đầu tư thận trọng nên model CAC ở mức 900K-1M VND.

---

## Q7. "Nếu ngày mai OpenAI ra 'ChatGPT University' thì sao?"

**Trả lời:**
Đây là **mối đe dọa lớn nhất**. Phản ứng của chúng tôi:

**Ngắn hạn (0-6 tháng):**
OpenAI chưa có hạ tầng tuân thủ PDPA tại Việt Nam. "ChatGPT University" sẽ là pure cloud → **bị chặn pháp lý**. Chúng tôi an toàn trong cửa sổ 6-12 tháng họ cần để xây năng lực on-prem.

**Trung hạn (6-18 tháng):**
Nếu OpenAI bắt tay với cloud nội địa (Viettel, VNPT) để có data residency:
- Chất lượng model tốt hơn (GPT-5/6 so với cấu hình hiện tại)
- Nhiều tài nguyên tích hợp LMS
- **Chúng tôi thua về công nghệ, nhưng thắng về quan hệ**

Phòng thủ: **2 học kỳ quan hệ với TA + dữ liệu RAG theo môn + thói quen sinh viên**. Switching cost xuất hiện — sinh viên không muốn re-upload tài liệu giữa kỳ.

**Dài hạn (18+ tháng):**
Nếu OpenAI thực sự làm hoàn hảo, chúng tôi **pivot thành lớp compliance nội địa**. OpenAI lo LLM; chúng tôi lo PDPA, LMS integration, RAG theo môn. Trở thành **đối tác bản địa hóa** thay vì cạnh tranh model.

**Sự thật:** Nếu OpenAI làm hoàn hảo cả compliance + localization, chúng tôi thua. Nhưng lịch sử big tech vào thị trường nhỏ, bị quản lý chặt (VN) cho thấy họ ưu tiên thị trường lớn trước. Chúng tôi có **cửa sổ 2-3 năm** để xây moat.

---

## Q8. "TAM của bạn dùng giả định 70% sinh viên cần hỗ trợ 24/7. Đó là giả định, không phải dữ liệu. Chứng minh đi."

**Trả lời:**
Đúng — con số 70% là giả định. Đây là **bằng chứng thực tế** hiện có:

**Bằng chứng trực tiếp (VinUni):**
- TA office hours: Thứ 2-6, 9 AM - 5 PM
- Bài nộp lab peak: **10 PM - nửa đêm** (có dữ liệu LMS)
- Khoảng trống: 17 giờ/ngày + cuối tuần không có hỗ trợ
- **Quan sát:** CS năm nhất, ~60-70% câu hỏi là lỗi cú pháp/debug (theo kinh nghiệm TA)

**Bằng chứng gián tiếp (benchmark ngành):**
- StackOverflow: 22M câu hỏi, peak usage **buổi tối trong tuần**
- GitHub Copilot: 90%+ sinh viên CS dùng (khảo sát GitHub 2024)
- Hành vi: Gen Z kỳ vọng câu trả lời tức thì (messenger, ChatGPT)

**Những điều chưa biết (cần test trong pilot):**
- Adoption thực tế khi có sản phẩm
- Sinh viên có tin AI cho bài chấm điểm không
- Hỗ trợ 24/7 có cải thiện kết quả học không

**Trả lời thẳng:** TAM 70% là **giả thuyết**, chưa phải fact. Pilot 50 sinh viên sẽ cho data đầu tiên. Nếu adoption < 40%, cần điều chỉnh TAM giảm đáng kể.

---

## Tóm tắt: Các điểm yếu chính

| Điểm yếu | Mức độ | Giảm thiểu |
|---------|--------|-----------|
| Giả định TAM 70% chưa được kiểm chứng | Trung bình | Pilot 50 sinh viên trước |
| CAC bị ước tính thấp | Thấp | Model CAC 900K-1M VND trong pitch |
| Đe dọa cạnh tranh từ OpenAI | Cao | Xây quan hệ + moat tuân thủ |
| Khả năng chi trả của đại học | Trung bình | Bắt đầu pilot, chứng minh giá trị |
| Rủi ro chính trị/học thuật | Cao | Làm cùng giảng viên, không đối đầu |

**Nhận định nhà đầu tư:** Unit economics mạnh và moat rõ, nhưng giai đoạn sớm, adoption chưa được chứng minh. Khuyến nghị: **Seed để chạy pilot** — Series A sau khi chứng minh Sean Ellis >40%.

---

*Mini Checkpoint V2 — Stress-test Q&A với nhà đầu tư*
