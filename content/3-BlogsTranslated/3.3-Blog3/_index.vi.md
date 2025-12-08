---
title: "Blog 3"
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

## AI có trách nhiệm trong thực tiễn: Red Teaming của Data Reply trên AWS

**Tác giả:** Cassandre Vandeputte, Davide Gallitelli, Amine Ait el Harraj  
**Ngày:** 29/4/2025  
**Chủ đề:** Amazon Bedrock, SageMaker, Responsible AI, Red Teaming

### Vì sao cần AI có trách nhiệm
- GenAI mang rủi ro: ảo giác, nội dung không an toàn, rò rỉ IP/dữ liệu, khó kiểm soát.  
- Red teaming (mô phỏng tấn công đối kháng) giúp phát hiện lỗ hổng trước khi bị khai thác.

### Mối đe dọa & khung tham chiếu
- Điểm yếu mô hình + đe dọa đối kháng (prompt injection, data poisoning, lộ thông tin nhạy cảm, DoS).  
- Tham chiếu OWASP Top 10 for LLMs để ưu tiên biện pháp giảm thiểu.

### Dịch vụ AWS cho Responsible AI
- **Công bằng:** SageMaker Clarify phát hiện bias; SageMaker Data Wrangler cân bằng dữ liệu.  
- **Độ bền vững:** Amazon Bedrock evaluations kiểm thử prompt biên và tình huống đối kháng.  
- **Bảo mật/riêng tư:** Bedrock Guardrails lọc nội dung, bảo vệ thông tin nhạy cảm.  
- **Minh bạch:** LangFuse giữ audit trail, giúp truy vết quyết định.

### Red Teaming Playground của Data Reply (kiến trúc)
- Identity: Amazon Cognito (kèm IdP ngoài) để cấp quyền an toàn.  
- UI: AWS Amplify + React qua ALB.  
- Knowledge: Amazon Bedrock Knowledge Bases + S3 + OpenSearch Serverless.  
- Quản lý mô hình: Bedrock Guardrails, SageMaker cho đánh giá, model registry đa nhà cung cấp.  
- Đánh giá:  
  - Online: AppSync (WebSocket) cho kiểm thử đối kháng thời gian thực, tập trung vào rủi ro OWASP LLM.  
  - Offline: SageMaker Clarify (bias), Amazon Comprehend (nội dung gây hại), Giskard + LLM-as-a-judge; LangFuse lưu audit trail.

### Khung ứng xử: Answer – Deflect – Safe response
- Với lĩnh vực nhạy cảm (ví dụ trợ lý sức khỏe tâm thần):  
  - Answer khi câu hỏi trong phạm vi.  
  - Deflect khi ngoài phạm vi.  
  - Safe response khi cần xác nhận chuyên gia.

### Kết luận
- Red teaming là liên tục; cần kết hợp chính sách quản trị và kiểm soát kỹ thuật.  
- Đánh giá online/offline trước khi production; ghi log đầy đủ để đảm bảo trách nhiệm giải trình.  
- Mở rộng với theo dõi vòng đời (SageMaker) hoặc IaC (CloudFormation) cho triển khai kiểm soát.

### Tags
`Responsible AI` · `Red Teaming` · `Amazon Bedrock` · `Amazon SageMaker` · `Generative AI`

