---
title: "Blog 2"
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

## Phân tích dữ liệu khai thác mỏ lịch sử bằng Amazon Bedrock

**Tác giả:** Benjamin Weber  
**Ngày:** 24/4/2025  
**Chủ đề:** Amazon Bedrock, Amazon Textract, Generative AI, Khai thác mỏ

### Bối cảnh
Cách tóm tắt và cấu trúc hồ sơ khai thác mỏ cũ bằng mô hình ngôn ngữ lớn trên Amazon Bedrock, biến tài liệu quét thành insight hành động.

### Vì sao quan trọng
- Báo cáo thực địa, khảo sát địa vật lý, log khoan… chứa thông tin về quặng và khả năng thu hồi.  
- Rà soát thủ công rất chậm; OCR thiếu ngữ cảnh; LLM giúp tóm tắt và rút trích thuộc tính nhanh.

### Cách tiếp cận
- Dùng Amazon Textract để OCR quy mô lớn; kết hợp LLM của Amazon Bedrock (Converse API) để tóm tắt.  
- Kỹ thuật prompt: chuyển từ prompt chung sang prompt có vai trò, định dạng ngắn gọn, sát yêu cầu.  
- Ví dụ cải thiện prompt: đặt vai trò “geologist”, yêu cầu định dạng “Name. Location. Mineralization. Total recovered.”  
- Tool use: yêu cầu xuất JSON (file_name, mine_name, summary, location, first_mined, recovery, primary/secondary minerals); cần kiểm tra JSON hợp lệ.

### Lợi ích
- Sàng lọc nhanh hàng nghìn trang, ra quyết định sớm về mỏ cũ.  
- Đầu ra có cấu trúc (JSON) phục vụ phân tích và tìm kiếm.  
- Có thể mở rộng với RAG hoặc fine-tuning để tăng độ chính xác và khả năng truy vết.

### Hướng phát triển
- Củng cố prompt; thêm bước kiểm tra JSON.  
- Khám phá phân tích đa phương thức và fine-tuning để nâng độ tin cậy.  
- Tham khảo notebook trên GitHub để xem mã mẫu.

### Tags
`Amazon Bedrock` · `Amazon Textract` · `Generative AI` · `Mining`

