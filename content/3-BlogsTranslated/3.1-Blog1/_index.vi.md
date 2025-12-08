---
title: "Blog 1"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

## Bắt đầu với Amazon CloudWatch Investigations

**Tác giả:** Andres Silva  
**Ngày:** 21/12/2024  
**Chủ đề:** Amazon CloudWatch, AWS CloudTrail, AWS Systems Manager

### Tổng quan
Hướng dẫn thiết lập và chạy phiên điều tra đầu tiên với Amazon CloudWatch Investigations có hỗ trợ AI: quyền truy cập, mã hóa, tích hợp.

### CloudWatch Investigations làm gì?
- Dùng generative AI để liên kết metrics, logs, traces, sự kiện triển khai…  
- Tạo giả thuyết nguyên nhân gốc và insight hành động, tăng tốc phản ứng sự cố.

### Bắt đầu nhanh
1) CloudWatch → AI Operations → Investigations → Configure for this account (IAM principal có `AIOpsConsoleAdminPolicy` hoặc tương đương).  
2) Chọn thời gian lưu trữ (mặc định 90 ngày) và KMS key do khách hàng quản lý nếu cần.  
3) Quyền truy cập: Admin (`AIOpsConsoleAdminPolicy`), Operator (`AIOpsOperatorAccess`), Read-only (`AIOpsReadOnlyAccess`).  
4) (Tùy chọn) Kết nối IAM Identity Center để gán đề xuất theo từng người dùng.  
5) Investigation configuration: cho phép AWS tự tạo IAM role đọc telemetry.  
6) Enhanced integration:  
   - Tags nhận diện ranh giới ứng dụng (thu hẹp phạm vi tìm kiếm)  
   - CloudTrail cho phát hiện sự kiện thay đổi  
   - X-Ray và Application Signals để bổ sung topology và health context  
7) (Tùy chọn) Tích hợp bên thứ ba (chat, SNS).  
8) Hoàn tất và chạy phiên điều tra đầu tiên.

### Bước tiếp theo & tăng cường bảo mật
- Chạy thử investigation để kiểm tra quyền và phạm vi dữ liệu.  
- Tinh chỉnh IAM role/policy; ưu tiên KMS key do khách hàng quản lý nếu cần.  
- Bật CloudTrail, X-Ray, App Signals để làm giàu giả thuyết.  
- Giữ vững tư thế ứng phó sự cố khi khai thác trợ lý AI.

### Tags
`Amazon CloudWatch` · `AWS CloudTrail` · `AWS Systems Manager` · `Cloud Operations` · `Monitoring`

