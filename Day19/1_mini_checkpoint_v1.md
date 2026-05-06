# Mini Checkpoint V1 — Kiểm tra mức sẵn sàng để pitch

## Sản phẩm: TA_Chatbot — AI Trợ Giảng Hybrid

---

## 1. Tuyên bố chiến lược (từ Day 16)

**Dành cho** sinh viên CS năm nhất thường xuyên bị kẹt bug khi học đêm,  
**TA_Chatbot giúp** họ nhận câu trả lời tức thì, bám theo môn học, có nguồn trích dẫn,  
**thông qua** ReAct agent với RAG bám theo môn học và triển khai hybrid,  
**khác với** các trợ lý AI phổ thông (ChatGPT) hoặc việc chờ TA office hours,  
**vì chúng tôi tận dụng** triển khai hybrid vừa tuân thủ PDPA vừa duy trì khả dụng 24/7.

---

## 2. Checklist mức sẵn sàng để pitch

### A. Độ rõ của vấn đề — "Bạn có thể nói nỗi đau trong 1 câu không?"

> "Sinh viên CS năm nhất tại VinUniversity thường bị kẹt bug lúc 10 PM trước deadline, trong khi TA chỉ online giờ hành chính — khiến sinh viên bị bỏ lại 12+ giờ không có hỗ trợ đáng tin cậy."

**Kết luận:** ✅ ĐẠT — Cụ thể, trực quan, có mốc thời gian, đủ đau.

---

### B. Độ cụ thể của khách hàng — "Bạn có thể gọi đúng phân khúc trong 1 câu không?"

> "Sinh viên CS năm nhất hoảng loạn lúc 10 PM đêm trước deadline lab khi gặp bug không giải được và không có TA để hỏi."

**Kết luận:** ✅ ĐẠT — Phân khúc hẹp, dễ tiếp cận, có nỗi đau rõ.

---

### C. Nhu cầu bị bỏ ngỏ — "Đây là nhu cầu thật, không phải tính năng?"

| Tiêu chí | Nhu cầu #1 (Hỗ trợ ngay) | Nhu cầu #2 (Câu trả lời đáng tin) | Nhu cầu #3 (Giảm tải TA) |
|---------|---------------------------|-----------------------------------|--------------------------|
| Không phải tính năng trá hình | ✅ Nỗi đau: kẹt lúc đêm | ✅ Nỗi đau: sai lệch thông tin | ✅ Nỗi đau: việc lặp lại |
| Nỗi đau lặp lại | ✅ 3-5 lần/tuần/sinh viên | ✅ Mỗi khái niệm mới | ✅ Hàng nghìn/lần học |
| Có cách đối phó | ✅ Google, chờ TA | ✅ ChatGPT, StackOverflow | ✅ Trả lời thủ công |
| Có bằng chứng | ✅ Lệch giờ TA | ✅ Rủi ro ảo giác | ✅ Dữ liệu tracking |
| Tác động kết quả | ✅ Tỷ lệ hoàn thành ↑ | ✅ Chất lượng học ↑ | ✅ Hiệu suất TA ↑ |

**Kết luận:** ✅ ĐẠT — Cả 3 nhu cầu đều là nhu cầu thật, không phải tính năng.

---

### D. Giả thuyết moat — "Vì sao đối thủ không thể copy trong 6 tháng?"

**Cơ chế moat:** Vòng quay học theo miền + Rào cản tuân thủ

| Rào cản | Giải thích | Độ khó sao chép |
|---------|-----------|-----------------|
| **Hiệu ứng mạng dữ liệu** | 50+ triển khai → bộ dữ liệu hỏi/đáp theo môn học riêng của VinUni | Khó — cần cùng quyền truy cập |
| **Hạ tầng tuân thủ** | Hybrid on-prem + cloud để đáp ứng PDPA — tốn kém, phức tạp | Khó — đa số đối thủ chọn pure cloud |
| **Niềm tin tích hợp môn học** | Tích hợp LMS + TA endorse qua 2 học kỳ | Trung bình — niềm tin cần thời gian |
| **Vòng lặp cải tiến liên tục** | Rating sinh viên → cập nhật RAG → trả lời tốt hơn → tăng tin tưởng | Trung bình — cần đủ khối lượng |

**Kết luận:** ✅ ĐẠT — Xác định ít nhất 2 rào cản khó sao chép.

---

### E. Quy mô thị trường — "Các con số có hợp lý?"

| Tầng | Ước tính | Giả định chính | Mức tin cậy |
|------|----------|---------------|-------------|
| **TAM** | ~61,250 sinh viên (CS/IT toàn quốc) HOẶC tiết kiệm $10-20K/trường/năm | 250 trường × 350 sinh viên trung bình × 70% cần | Thấp |
| **SAM** | ~240 users hoạt động (CS năm nhất VinUni) | 300 sinh viên năm nhất × 80% adoption | Trung bình |
| **SOM** | ~380 users hoạt động (12-24 tháng) | Mở rộng lên năm 2, 85% adoption | Trung bình-Cao |

**Kết luận:** ✅ ĐẠT — SAM cụ thể, có thể tiếp cận; TAM định hướng.

---

### F. Unit Economics — "Có khả thi về tài chính?"

**Kịch bản cơ sở (từ Day 18):**

| Chỉ số | Giá trị | Benchmark | Kết luận |
|-------|--------|-----------|---------|
| ARPU | 500,000 VND (~$20)/tháng | — | Hợp lý cho ngân sách đại học |
| Biên lợi nhuận gộp | 430,000 VND (86%) | AI: 40-60% | ✅ Mạnh (lợi thế công cụ nội bộ) |
| LTV | 14,190,000 VND | — | — |
| CAC | 500,000 VND | — | Thấp (mạng lưới TA trực tiếp) |
| **LTV/CAC** | **28.38** | Chuẩn VC: >3 | ✅ Rất tốt |
| **CAC Payback** | **1.16 tháng** | Benchmark: <12 tháng | ✅ Rất tốt |
| **Project Payback** | **~8.9 tháng** | Benchmark: <24 tháng | ✅ Rất tốt |
| **Runway (bi quan)** | **~44 tháng** | Cần: ≥12 tháng | ✅ An toàn |

**Kết luận:** ✅ ĐẠT — Unit economics mạnh ngay cả kịch bản bi quan.

---

### G. Chỉ số PMF — "Bạn sẽ đo thành công thế nào?"

| Phương pháp | Chỉ số | Mục tiêu | Loại |
|------------|--------|----------|------|
| **Aha Moment** | Sinh viên fix bug và tiếp tục lab trong 10 phút sau query | 40%+ phiên | Actionable |
| **Retention** | D30 active user rate | >30% (benchmark B2B SaaS) | Actionable |
| **Sean Ellis** | "Rất thất vọng" nếu chatbot bị gỡ | >40% | Actionable |
| **Task completion** | Tỷ lệ giải bug sau câu trả lời | >70% | Actionable |

**Vanity metrics nên tránh:**
- ❌ Tổng số đăng ký
- ❌ Tổng số query (rủi ro spam)
- ❌ Click citation (tò mò ≠ tin tưởng)
- ❌ Thumbs up count (tỷ lệ tham gia thấp)

**Kết luận:** ✅ ĐẠT — Chỉ số hành động rõ ràng, tránh vanity metrics.

---

### H. Phạm vi MVP — "Có đang xây đúng thứ trước tiên?"

**Trong phạm vi (Core test):**
1. Q&A bám theo môn học với RAG (FAISS trên tài liệu môn)
2. Hiển thị citation (nguồn: slide X, lab Y)

**Ngoài phạm vi (để sau):**
- Hỗ trợ đa môn (ngoài CS năm nhất)
- Dashboard/analytics cho TA
- Đa ngôn ngữ
- Mobile app

**Không làm (red line):**
- Thay thế TA hoàn toàn
- Hỗ trợ môn không thuộc CS
- Mở đăng ký cho trường khác

**Kill question:** Nếu bỏ phần citation, giá trị cốt lõi còn không?
→ **KHÔNG** — citation là cơ chế tạo niềm tin. ✅ Cả hai tính năng đều là core.

**Kết luận:** ✅ ĐẠT — Trong phạm vi ≤ 2 tính năng, ngoài phạm vi dài hơn trong phạm vi.

---

### I. Fallback UX — "Khi AI thất bại thì sao?"

**Kích hoạt:** Retrieval hit rate < 70% HOẶC query có "error"/"bug" mà không match tốt

**Hành động fallback:**
1. Hiển thị: "Mình chưa có câu trả lời đủ tự tin từ tài liệu môn học cho câu hỏi này."
2. Đề nghị: "Bạn có muốn chuyển lên TA không? (Phản hồi trong office hours kế tiếp)"
3. Log: Query + context → hàng đợi TA review để cải thiện RAG

**Anti-pattern tránh:** ❌ "Confidence score < 80%" (LLM vẫn có thể hallucinate tự tin)

**Kết luận:** ✅ ĐẠT — Fallback khả thi về vận hành, không phụ thuộc AI tự nhận biết.

---

### J. Bảng giả thuyết — "Bạn đang đặt cược vào điều gì?"

| Giả thuyết | Chỉ số thành công | Ngưỡng | Cách test |
|-----------|------------------|--------|----------|
| RAG bám theo môn đạt >70% hit rate cho query CS năm nhất | Retrieval hit rate | >70% | Chạy 100 query thật trên FAISS index |
| Sinh viên dùng chatbot trong 5 phút sau khi bị kẹt ban đêm | Time-to-first-query sau khi mở lab | <5 phút (ngoài giờ) | Phân tích log trong pilot |
| Sinh viên nhận câu trả lời có citation và tiếp tục lab | Task resumption rate | >60% | Phân tích phiên |

**Giả định rủi ro nhất:** Chất lượng tài liệu môn đủ tốt để đạt >70% hit rate.
**Test:** Audit tài liệu + chạy 50 query trước khi viết code. Chi phí: ~4 giờ.

**Kết luận:** ✅ ĐẠT — Giả thuyết có thể kiểm chứng, rủi ro lớn nhất đã xác định và test rẻ.

---

## 3. Kết luận mức sẵn sàng để pitch

| Checkpoint | Trạng thái |
|-----------|-----------|
| Độ rõ vấn đề | ✅ ĐẠT |
| Độ cụ thể khách hàng | ✅ ĐẠT |
| Nhu cầu bị bỏ ngỏ | ✅ ĐẠT |
| Giả thuyết moat | ✅ ĐẠT |
| Quy mô thị trường | ✅ ĐẠT |
| Unit economics | ✅ ĐẠT |
| Chỉ số PMF | ✅ ĐẠT |
| Phạm vi MVP | ✅ ĐẠT |
| Fallback UX | ✅ ĐẠT |
| Bảng giả thuyết | ✅ ĐẠT |

**Tổng kết: 10/10 ĐẠT — Sẵn sàng để pitch.**

---

## 4. Kiểm tra tự tin trước khi pitch

**Nếu nhà đầu tư hỏi "Vì sao là bây giờ?" — Trả lời:**
1. Gen Z kỳ vọng hỗ trợ tức thì (hiệu ứng ChatGPT)
2. LLM hiện đủ tốt để trả lời 70%+ câu hỏi CS cơ bản
3. Yêu cầu tuân thủ PDPA của VinUniversity tạo moat trước AI phổ thông
4. Tỉ lệ TA/sinh viên 1:50 là không bền vững — cần tự động hóa ngay

**Nếu nhà đầu tư hỏi "Lợi thế không công bằng là gì?" — Trả lời:**
Kiến trúc triển khai hybrid đáp ứng PDPA data residency — đối thủ dùng pure cloud (OpenAI API) không thể phục vụ hợp pháp cho đại học Việt Nam. Kết hợp với RAG bám theo môn học cải thiện theo từng lần triển khai.

---

*Mini Checkpoint V1 — Kiểm tra mức sẵn sàng để pitch*
