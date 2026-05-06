# Solo Pitch Lab — TA_Chatbot Pitch Deck

## Sản phẩm: TA_Chatbot — AI Trợ Giảng Hybrid
## Người thuyết trình: [Tên của bạn]
## Thời lượng: 5 phút + 5 phút Q&A

---

## SLIDE 1: Slide tiêu đề

**TA_Chatbot**
> AI Trợ Giảng 24/7 — Theo môn học, tuân thủ, luôn sẵn sàng.

**Phụ đề:** Hybrid AI Teaching Assistant cho đại học Việt Nam
**Tagline:** "Không còn đêm khuya lạc lối debug — TA_Chatbot luôn bên bạn."

---

## SLIDE 2: Vấn đề (30 giây)

**"Sinh viên CS năm nhất tại VinUniversity thường bị kẹt bug vào 10 PM trước deadline — nhưng TA chỉ online 9 AM-5 PM."**

Các con số:
- **12+ giờ/ngày** không có TA hỗ trợ (buổi tối + cuối tuần)
- Sinh viên mất **2-4 giờ** mỗi lần tìm lỗi trên Google/StackOverflow
- **60% thời gian TA** dành cho câu hỏi lặp lại (lỗi cú pháp, khái niệm cơ bản)
- AI phổ thông (ChatGPT) = **không bám theo môn** + **rủi ro tuân thủ PDPA**

**Khoảnh khắc đau:**
> 22h đêm Chủ Nhật. Deadline 0h. Gặp segmentation fault. Không có TA. Google 30 phút không ra. Panic.

---

## SLIDE 3: Giải pháp (30 giây)

**TA_Chatbot** — Hybrid AI Teaching Assistant

- **Khả dụng 24/7** — Luôn on, kể cả 10 PM
- **Trả lời theo môn học** — Bám theo tài liệu môn (slides, labs, assignments)
- **Có trích dẫn** — Mỗi câu trả lời có nguồn: "Slide 42, Week 3: Pointers"
- **Tuân thủ PDPA** — Triển khai hybrid giữ PII tại Việt Nam
- **Giảm 60% workload TA** — Tự động hóa Q&A lặp lại

**Công nghệ cốt lõi:**
> ReAct Agent + Course-Grounded RAG + Hybrid On-Premise/Cloud Deployment

---

## SLIDE 4: Khách hàng mục tiêu (30 giây)

**Phân khúc chính:**
Sinh viên CS năm nhất tại VinUniversity hoảng khi kẹt bug ngoài giờ TA.

**Chân dung cụ thể:**
> "Sinh viên CS năm nhất panic lúc 10 PM đêm trước deadline lab khi gặp bug không giải được và không có TA để hỏi."

**Quy mô phân khúc (SAM):**
- **~300** sinh viên CS năm nhất tại VinUni
- **Mục tiêu adoption 80%** = **240 users hoạt động** (Năm 1)
- **Khả năng mở rộng:** 1,000 sinh viên CS toàn trường → các đại học khác ở VN

**Đường tiếp cận:**
Tích hợp LMS (Canvas) + TA endorsement trong tuần orientation

---

## SLIDE 5: Quy mô thị trường (30 giây)

| Tầng | Quy mô | Ghi chú |
|------|--------|--------|
| **TAM** | ~61,250 sinh viên | Toàn bộ sinh viên CS/IT VN (~250 trường × 350 TB × 70% cần) |
| **SAM** | ~240 users | CS năm nhất VinUni, 80% adoption |
| **SOM** | ~380 users | 12-24 tháng: năm nhất + một phần năm 2 |

**Mô hình doanh thu:**
- **B2B SaaS:** Đại học trả 500,000 VND/sinh viên/năm (~$20)
- **Doanh thu năm 1:** 240 × 500K = **120M VND** (~$4,800)
- **Tiềm năng năm 3:** 5,000 sinh viên × 500K = **2.5B VND** (~$100K ARR)

**Không phải từ thiện:** Tiết kiệm chi phí + cải thiện kết quả học là đủ để phân bổ ngân sách.

---

## SLIDE 6: Unit Economics (45 giây)

**Kịch bản cơ sở (Năm 1):**

| Chỉ số | Giá trị | Benchmark | Kết luận |
|-------|--------|-----------|---------|
| ARPU | 500,000 VND/tháng | — | Hợp lý |
| Biên lợi nhuận gộp | 430,000 VND (86%) | AI: 40-60% | ✅ Mạnh |
| LTV | 14,190,000 VND | — | Tốt |
| CAC | 500,000 VND | — | Thấp (mạng lưới TA) |
| **LTV/CAC** | **28.38** | VC: >3 | ✅ Rất tốt |
| **CAC Payback** | **1.16 tháng** | <12 tháng | ✅ Rất tốt |
| **Project Payback** | **~8.9 tháng** | <24 tháng | ✅ Rất tốt |

**Runway bi quan: ~44 tháng** — vẫn an toàn.

**Insight chính:** Không cần paid ads — tiếp cận trực tiếp qua mạng lưới TA giúp CAC rất thấp.

---

## SLIDE 7: Moat (45 giây)

**"Vì sao ChatGPT không chỉ thêm upload tài liệu và giết bạn?"**

**Hai moat cấu trúc:**

**1. Rào cản tuân thủ (PDPA + Data Residency)**
- Đại học Việt Nam **không thể** gửi PII sinh viên lên server US của OpenAI
- Chúng tôi dùng **triển khai hybrid**: LLM on-prem xử lý PII, cloud cho query ẩn danh
- ChatGPT là pure cloud → bị chặn pháp lý cho đại học Việt Nam
- **Đối thủ cần 6-12 tháng + hàng triệu USD hạ tầng để sao chép**

**2. Vòng quay học theo miền (Domain-Learning Flywheel)**
- Mỗi deployment → thêm dữ liệu Q/A theo môn
- Sau 50 deployments → độ chính xác retrieval ↑ → chất lượng trả lời ↑
- **Dataset là độc quyền** — đối thủ không thể có nếu không được trường cấp quyền

**Moat phụ:**
- Tích hợp LMS + TA endorsement (quan hệ 2 học kỳ)
- RAG theo môn học cải thiện theo thời gian

---

## SLIDE 8: Chiến lược PMF (30 giây)

**Aha Moment:**
> Sinh viên fix bug và tiếp tục làm lab trong 10 phút sau khi hỏi TA_Chatbot.

**Chỉ số thành công (Actionable):**
| Chỉ số | Mục tiêu | Loại |
|-------|----------|------|
| Bug resolution rate | >70% | Task completion |
| D30 retention | >30% | Benchmark B2B SaaS |
| Sean Ellis score | >40% "very disappointed" | Tín hiệu PMF |
| Task resumption | >60% | Hành vi |

**Vanity metrics bỏ qua:** Total sign-ups, total queries, thumbs-up count.

**Cách test PMF:** Pilot 50 sinh viên (Tháng 1-3), đo hành vi thực tế — không chỉ khảo sát.

---

## SLIDE 9: MVP & Roadmap (30 giây)

**MVP (Tháng 1-3) — chỉ 2 tính năng core:**
1. Q&A bám theo môn học với RAG (FAISS trên tài liệu môn)
2. Hiển thị citation (nguồn: slide X, lab Y)

**Trong phạm vi:** 1 lớp pilot, 50 sinh viên
**Ngoài phạm vi:** Đa môn, dashboard TA, mobile app, các đại học khác

**Lộ trình:**
- **Tháng 4-12:** Rollout toàn bộ năm nhất (240 users)
- **Năm 2:** Mở rộng sang năm 2 + các môn CS khác (380 users)
- **Năm 3+:** Cấp phép cho các đại học Việt Nam khác

**Fallback UX:** Khi retrieval fail → chuyển sang hàng đợi TA (office hours kế tiếp)

---

## SLIDE 10: Team & Ask (30 giây)

**Mục gọi vốn:**
> Gọi **[Số tiền]** seed để hoàn tất pilot + scale đến toàn bộ năm nhất.

**Phân bổ vốn:**
- 40% — Kỹ thuật (hybrid deployment, RAG pipeline)
- 30% — Tích hợp môn học & audit tuân thủ
- 20% — Vận hành pilot & đào tạo TA
- 10% — Dự phòng

**Vì sao là bây giờ:**
1. Gen Z kỳ vọng hỗ trợ AI tức thì (hiệu ứng ChatGPT)
2. LLM đủ tốt cho 70%+ câu hỏi CS
3. VinUni cần giải pháp tuân thủ PDPA — đối thủ không đáp ứng được
4. Tỉ lệ TA/sinh viên 1:50 là không bền vững — cần tự động hóa gấp

---

## Chuẩn bị Q&A — Top 5 câu hỏi nhà đầu tư

### Q1. "SAM chỉ 240 users. Làm sao venture-scale?"
**Trả lời:** 240 là beachhead năm 1. Lộ trình: Năm 2 → 1,000 sinh viên CS VinUni → Năm 3+ → 70,000 sinh viên toàn VN. TAM = $525K ARR khi thâm nhập đầy đủ. VinUni là khách hàng tham chiếu.

### Q2. "Nếu OpenAI ra sản phẩm cho đại học thì sao?"
**Trả lời:** Họ cần hạ tầng on-prem tuân thủ PDPA tại Việt Nam — mất 6-12 tháng. Chúng tôi có lợi thế 2 học kỳ về quan hệ + dữ liệu môn + thói quen sinh viên. Nếu OpenAI làm hoàn hảo, chúng tôi pivot thành đối tác compliance nội địa.

### Q3. "Ai trả tiền — sinh viên hay nhà trường?"
**Trả lời:** Nhà trường trả. 1.44B VND/năm cho 240 sinh viên = 0.38% doanh thu học phí (học phí ~$15K/sinh viên). Đây là đầu tư nâng chất lượng, không chỉ tiết kiệm chi phí.

### Q4. "Làm sao biết sinh viên sẽ dùng?"
**Trả lời:** Pilot 50 sinh viên trước. Đo: time-to-first-query sau khi mở lab (<5 phút), bug resolution rate (>70%), task resumption (>60%). Nếu adoption <40%, pivot trước khi scale.

### Q5. "LTV/CAC 28.38 quá đẹp. Bẫy ở đâu?"
**Trả lời:** CAC thấp vì không chạy ads — tiếp cận trực tiếp qua TA. Nhưng CAC thật phải tính thêm chi phí pháp lý/tuân thủ (~900K-1M VND/user). LTV/CAC điều chỉnh ~15.84, vẫn rất tốt (>3).

---

## Phân bổ thời gian pitch

| Phần | Thời lượng |
|------|------------|
| Slide 1 — Tiêu đề | 15s |
| Slide 2 — Vấn đề | 30s |
| Slide 3 — Giải pháp | 30s |
| Slide 4 — Khách hàng | 30s |
| Slide 5 — Thị trường | 30s |
| Slide 6 — Unit Economics | 45s |
| Slide 7 — Moat | 45s |
| Slide 8 — Chiến lược PMF | 30s |
| Slide 9 — MVP/Roadmap | 30s |
| Slide 10 — Ask | 30s |
| **Tổng pitch** | **~5 phút** |
| **Q&A** | **5 phút** |

---

## Cụm câu cần nhớ (Cheat Sheet)

**Câu mở đầu:**
> "22h đêm Chủ Nhật. Deadline 0h sáng. Bạn gặp bug không giải được. TA thì offline từ chiều 5h. Bạn làm gì?"

**Value prop (1 câu):**
> "TA_Chatbot mang lại hỗ trợ lập trình tức thì, bám theo môn học, 24/7 cho sinh viên VinUni — đồng thời đảm bảo dữ liệu tuân thủ PDPA."

**Moat (1 câu):**
> "Chúng tôi là giải pháp tuân thủ duy nhất — các đối thủ pure cloud như ChatGPT bị chặn pháp lý tại đại học Việt Nam."

**Ask (1 câu):**
> "Chúng tôi gọi [Số tiền] để chứng minh PMF với 240 sinh viên và xây moat giúp dẫn trước AI phổ thông."

---

*Solo Pitch Lab — TA_Chatbot Pitch Deck*
