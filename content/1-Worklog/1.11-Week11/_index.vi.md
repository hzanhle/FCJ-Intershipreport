---
title: "Worklog Tuần 11"
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---

## 🎯 Mục tiêu
- Tích hợp tất cả dịch vụ AWS trong kiến trúc vào webapp.  
- Xây dựng luồng xác thực, truy cập dữ liệu, thông báo.  
- Dùng Amplify để đơn giản hóa tích hợp AWS trên frontend.  
- Hoàn thiện webapp kết nối cloud vận hành được.

---

## 📋 Nhiệm vụ trong tuần

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ----- | ---------- | --------------- | ------------------ |
| 1 | - Tích hợp Cognito auth vào webapp <br>- Cấu hình login, signup, quản lý session | 11/17/2025 | 11/17/2025 | AWS Cognito Docs |
| 2 | - Kết nối webapp với Amplify hosting <br>- Thiết lập CI/CD GitHub → Amplify | 11/18/2025 | 11/18/2025 | Amplify Hosting Docs |
| 3 | - Tích hợp S3 cho frontend (truy cập file, lưu dữ liệu IoT nếu cần) <br>- Render nội dung từ S3 lên UI | 11/19/2025 | 11/19/2025 | S3 Docs |
| 4 | - Tích hợp DynamoDB vào webapp (query, hiển thị, lọc) <br>- Kết nối qua API Gateway + Lambda | 11/20/2025 | 11/20/2025 | DynamoDB Docs |
| 5 | - Tích hợp SES (thông báo) nếu cần <br>- Kiểm thử tích hợp toàn bộ AWS trong webapp <br>- Viết tài liệu tuần | 11/21/2025 | 11/21/2025 | SES Docs |

