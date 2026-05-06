# Pitch Memo — TA_Chatbot (Investor One-Pager)

## 1. Problem
Sinh viên CS năm nhất tại VinUniversity thường bị kẹt bug vào 10 PM trước deadline, trong khi TA chỉ online 9 AM-5 PM. Khoảng 12+ giờ/ngày không có hỗ trợ, dẫn đến chậm tiến độ, panic và chất lượng học tập giảm.

## 2. Insight
Vấn đề không phải là thiếu AI, mà là thiếu câu trả lời bám theo môn học + cần tuân thủ PDPA. ChatGPT không được phép nhận PII của sinh viên, và không có kết nối với tài liệu môn học.

## 3. Solution
TA_Chatbot là trợ giảng AI 24/7 cho từng môn học, trả lời dựa trên tài liệu môn (slides, labs) và hiển thị citation cụ thể. Hệ thống hybrid deployment giữ PII trong nước, đáp ứng PDPA.

## 4. Why now
- Gen Z đã quen với phản hồi ngay lập tức (ChatGPT effect).
- LLM đủ tốt để giải đáp 70% câu hỏi CS cơ bản.
- VinUni cần giải pháp PDPA-compliant, đối thủ pure-cloud bị chặn.
- Tỉ lệ TA/sinh viên 1:50 không bền vững.

## 5. Traction
- KPI PMF dự kiến: bug resolution rate >70%, D30 retention >30%, Sean Ellis >40%.
- Pilot 50 sinh viên trong 3 tháng để đo time-to-first-query <5 phút và task resumption >60%.

## 6. Ask
Gọi seed để hoàn tất pilot và scale đến lớp CS năm nhất (240 users). Ngân sách dự kiến:
- 40% Engineering (hybrid deployment, RAG pipeline)
- 30% Compliance + LMS integration
- 20% Pilot ops + TA training
- 10% Buffer

---
Nguồn: Day 16-18 + Solo Pitch Lab
