---
title: "Event 1"
date: 2026-06-27
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# FCAJ Community Day – June 2026

**Thời gian tổ chức:** Ngày 27/06/2026

**Địa điểm:** Tầng 26 & 36, Bitexco Financial Tower, TP. Hồ Chí Minh (đồng thời phát trực tiếp trên YouTube).

**Vai trò:** Người tham dự (Participant)

### Mục đích của sự kiện
- Định hướng sự nghiệp & tư duy công nghệ: Chia sẻ góc nhìn thực tế từ các Founder và Chuyên gia về lộ trình phát triển bản thân trong thời đại AI khuếch đại.
- Cập nhật xu hướng AI Agent chuyên biệt: Đi sâu vào các giải pháp Multi-Agent, Voice AI tiếng Việt, DevOps AI Agent và Amazon Q áp dụng trực tiếp cho môi trường Doanh nghiệp (Enterprise/BFSI).
- Thực thi kiến trúc & bảo mật thực tế: Hướng dẫn cách thiết kế hệ thống Serverless, tối ưu hóa quy trình làm việc (SDLC/HR) và thiết lập kết nối Private bảo mật cho AI.

### Nội dung nổi bật

#### 1. Vận hành hạ tầng Cloud bằng Agentic Platform
- Diễn giả: Anh Steve Trần (Founder & CEO tại Cloud Thinker, cựu Solution Architect tại AWS)
- Thực trạng thị trường lao động thời đại AI:
  - Doanh nghiệp ngưng tuyển dụng dồn dập hoặc siết chặt đầu vào Fresher/Junior. Ưu tiên tuyển nhân sự Senior biết phối hợp cực tốt với các công cụ AI.
  - Tuy nhiên, việc vận hành hạ tầng Production là cực kỳ then chốt (critical). Mỗi phút dừng hệ thống (downtime) gây tổn hại doanh thu rất lớn nên AI chưa thể thay thế hoàn toàn con người.
- Giải pháp nền tảng Agentic (Cloud Thinker):
  - Incident Investigation: Đọc log và điều tra nguyên nhân sự cố trong vài phút thay vì tốn nhiều giờ đồng hồ của kỹ sư.
  - Code & Infra Review: Kiểm soát chất lượng tự động trước khi đẩy lên Production nhằm giải quyết nút thắt cổ chai (bottleneck) ở khâu kiểm thử Quality Control.
  - FinOps: Tự động hóa quản lý và tối ưu hóa chi phí Cloud 100% nhờ AI hiểu rõ cả kiến trúc AWS lẫn nghiệp vụ tài chính.
  - Security & Pen Testing: Chuyển đổi tư duy của Hacker (Whitehat/Blackhat) thành công cụ tự động mô phỏng tấn công (Penetration Testing) và đánh giá bảo mật hạ tầng.
- Kiến trúc kỹ thuật:
  - Single Agent vs Multi-Agent: Single Agent có thể xử lý hơn 95% tác vụ nhưng dễ bị loãng ngữ cảnh (context window). Multi-Agent với các Agent chuyên biệt (Specialist Agents) giúp thu nhỏ ngữ cảnh, giảm chi phí Token, tăng tốc độ xử lý và đáp ứng cơ chế phân quyền RBAC (Role-Based Access Control).
  - Khác với các công cụ Chat/Coding phổ thông dễ gây rủi ro thao tác nhầm trên Production, hệ thống thiết kế nhiều lớp phê duyệt (Multi-layer Approval) để bảo đảm an toàn.

#### 2. Triển khai Voice AI cho doanh nghiệp (thực tế tiếng Việt & môi trường ngân hàng)
- Diễn giả: Anh Hiếu Nghị (Renova Cloud), Anh Kiệt (AWS Student Community Builder), Anh Trung Đỗ (Founder & CEO tại R AI, cựu YC Founder)
- Thách thức Voice AI tiếng Việt: Tiếng Việt là ngôn ngữ ít tài nguyên (Low-Resource Language) nên các mô hình nói-sang-nói trực tiếp (Speech-to-Speech) chuẩn trên thế giới chưa hỗ trợ tốt.
- Kiến trúc Voice AI 3 bước tiêu chuẩn doanh nghiệp:
  1. STT (Speech-to-Text): Chuyển âm thanh đầu vào của khách hàng thành dạng văn bản (Text).
  2. LLM Agent + Tool Calling: Đưa văn bản vào LLM xử lý với Prompt định hướng nghiệp vụ. Gọi API tự động (Tool Calling) như khóa thẻ, tra cứu số dư.
  3. TTS (Text-to-Speech): Chuyển văn bản phản hồi thành giọng nói tự nhiên trả về cho người dùng.
- Xử lý các bài toán thực tế khi lên Production (VPBank, VIP):
  - Streaming Real-time: Đẩy dữ liệu liên tục theo dạng dòng (stream) ở cả 3 bước để giảm độ trễ cuộc gọi.
  - Nhận diện giới tính (Gender Detection): Tự động phát hiện giọng Nam/Nữ để xưng hô "Anh/Chị" chuẩn xác.
  - Cơ chế ngắt lời & ngữ cảnh (VAD & Context Understanding): Tránh việc AI nhảy vào miệng khách hàng khi họ chỉ đang khựng lại suy nghĩ (như đọc số điện thoại), đồng thời ngắt lời AI kịp thời khi khách phản hồi.
  - Giọng vùng miền (Accents): Huấn luyện 10–20% dữ liệu giọng miền Trung/Bắc/Nam để tăng khả năng nhận diện.
  - Human-in-the-Loop: Khi AI không thể xử lý hoặc phát hiện khách hàng tức giận, AI sẽ tự động chuyển giao cuộc gọi (handover) mượt mà cho nhân viên tổng đài.

#### 3. Tự động hóa giám sát & xử lý sự cố với DevOps AI Agent
- Diễn giả: Anh Nguyên Nguyễn & Chị Bảo (Cloud Engineers tại Cloud Kinetics)
- Vấn đề của quy trình DevOps truyền thống:
  - Dữ liệu giám sát bị phân tán (Fragmented Telemetry) ở nhiều nơi (CloudWatch, CloudTrail, Grafana).
  - Rào cản kiến thức (Knowledge Gap), ngắt quãng công việc liên tục khiến thời gian điều tra lỗi (MTTD) và khắc phục (MTTR) kéo dài.
- 6 trụ cột của DevOps AI Agent:
  - Context Learning: Học hạ tầng thông qua Agent Space và tạo ra bản đồ kiến trúc (Topology).
  - Control: Giới hạn quyền truy cập tài nguyên minh bạch dựa trên Resource Tags.
  - Integration: Mở rộng năng lực kết nối cơ sở dữ liệu/công cụ qua giao thức MCP (Model Context Protocol).
  - Collaboration: Tích hợp giao tiếp qua Slack, ServiceNow, Jira.
  - Convenience: Dễ dàng thiết lập trực tiếp trên AWS Console.
  - Cost-Effective: Tính phí linh hoạt dựa trên thời gian thực thi (khoảng $0.083/giây).
- Quy trình xử lý sự cố 4 bước:
  1. Triage (Phân loại): Nhận Trigger từ Alert/CloudWatch hoặc chat trực tiếp.
  2. Investigation (Điều tra): Đưa ra các giả thuyết và kiểm chứng dựa trên Topology/Logs để tìm Root Cause Analysis.
  3. Mitigation (Khắc phục): Đề xuất kịch bản xử lý (Prepare -> Validate -> Execute -> Post-validate). Không tự ý thực thi nhằm bảo đảm tính an toàn (Safety First).
  4. Improvement (Cải thiện): Đề xuất giải pháp nâng cấp hệ thống để ngăn ngừa sự cố lặp lại trong tương lai.
- Demo thực tế & kết quả doanh nghiệp:
  - Demo DDoS Attack: Agent phát hiện cuộc tấn công giả lập 1,000 req/s vào ECS/ALB, điều tra ra 10 ECS Task gây tràn traffic và cung cấp lệnh Terminal dừng Task khôi phục ứng dụng.
  - Case Studies: Đại học WGU giảm 77% thời gian MTTR (từ 2 giờ xuống 28 phút); Zenchef giảm 75% thời gian phát hiện lỗi Misconfiguration; Tập đoàn KDDI rút ngắn thời gian xử lý sự cố từ nhiều tuần xuống vài ngày.

#### 4. Tối ưu hóa quy trình tuyển dụng & quản trị nhân sự với Amazon Q (Quick)
- Diễn giả: Anh Trường (Quen) & Chị Minh Anh (Solution Shapers tại Noventic)
- Thách thức của bộ phận nhân sự (HR):
  - Sàng lọc CV thủ công tốn thời gian (Time-to-hire mất 1–2 tháng), dễ bỏ lỡ nhân tài (Missing Key Talent).
  - Đánh giá ứng viên dựa trên cảm tính, thiếu tiêu chuẩn dữ liệu định lượng giữa các bộ phận.
  - Rủi ro bảo mật dữ liệu nghiêm trọng khi đưa CV/thông tin nội bộ lên các AI Public.
- Sức mạnh kết nối của Amazon Q (Quick):
  - Đa dạng kết nối (Action Connectors): Tích hợp sâu với Microsoft (SharePoint, Outlook, OneDrive), Google Workspace (Gmail, Drive), S3, Relational DB, Jira, Salesforce, GitHub và MCP.
  - Quản trị bảo mật: Mô hình chạy hoàn toàn trên môi trường bảo mật của AWS Bedrock (Nova, Claude) và tuân thủ Local Zone.
- Demo trực tiếp kịch bản HR (Quick Desktop):
  - Tạo kỹ năng tự động (Custom Skill): Đưa file Markdown để AI tự định nghĩa Skill "HR Talent Review Assistant" bao gồm các bước kiểm tra, đánh giá cấp độ kinh nghiệm.
  - Sàng lọc CV & đánh giá tự động: Đọc và OCR hàng loạt CV (kể cả file PDF/scan), tự động đối chiếu với Job Description (JD) Junior Cloud Engineer.
  - Báo cáo trực quan: Xuất báo cáo HTML chi tiết phân loại ứng viên (Strong, Good, Low), phân tích điểm mạnh/điểm yếu, gợi ý câu hỏi phỏng vấn và dự báo dải lương (Salary Benchmark).

#### 5. Kiến trúc bảo mật Private MCP Server cho Amazon Q trong doanh nghiệp
- Diễn giả: Anh Toàn Nguyễn (AWS Security Builder) & Anh Hiếu Nghị (Renova Cloud)
- Rủi ro bảo mật Enterprise: Khi Amazon Q kết nối với các hệ thống MCP Server nội bộ (Zalo, WhatsApp, DB nội bộ, AWS resources...), việc dùng Public Endpoint mở ra các lỗ hổng bị tấn công DDoS, Man-in-the-Middle hoặc rò rỉ dữ liệu.
- Mô hình kiến trúc bảo mật khép kín (Private Security Architecture):
  - Đặt MCP Server hoàn toàn trong Private Subnet của VPC.
  - Sử dụng VPC Connection / Interface Endpoint để tạo luồng kết nối nội bộ riêng tư với Amazon Q.
  - Sử dụng Internal ALB tích hợp chứng chỉ mã hóa TLS (AWS Certificate Manager - ACM) kết hợp Route 53 Private Hosted Zone / Resolver để phân giải tên miền DNS nội bộ.
  - Giúp toàn bộ dữ liệu lưu thông khép kín trong AWS Cloud (Zero Public Exposure).
- Ước tính chi phí vận hành hạ tầng Private: Chi phí vận hành hạ tầng riêng tư (Route 53 Resolver, ALB, EC2, Endpoints, Secret Manager) ước tính từ $250 – $350/tháng tùy thuộc vào lưu lượng dữ liệu truyền tải.

### Những gì học được
- Tư duy làm việc cùng AI: AI là "bộ khuếch đại" năng lực. Trong các mảng phức tạp như hạ tầng Production hay tuyển dụng, AI đóng vai trò hỗ trợ đắc lực (Support/Assistant), nhưng con người (Human-in-the-loop) luôn giữ quyền quyết định cuối cùng.
- Kiến trúc AI thực tế: Nắm vững mô hình Multi-Agent chuyên biệt để tối ưu hóa cửa sổ ngữ cảnh (Context Window), kiến trúc 3 bước cho Voice AI tiếng Việt, quy trình 4 bước của DevOps Agent và phương pháp kết nối Private MCP Server an toàn tuyệt đối cho Enterprise.
- Ứng dụng thực thi đa ngành: Thấy được tiềm năng tự động hóa vượt trội từ việc ứng dụng AI vào vận hành hạ tầng Cloud, xử lý sự cố hệ thống tự động cho tới tối ưu hóa quy trình HR/Business trong doanh nghiệp.

### Minh chứng tham gia
<img src="/images/event1/event1.jpg">
