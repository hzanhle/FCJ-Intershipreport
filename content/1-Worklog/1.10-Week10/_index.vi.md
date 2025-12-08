---
title: "Worklog Tuần 10"
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---

## 🎯 Mục tiêu
- Kết nối pipeline IoT device → AWS IoT Core → backend.  
- Đảm bảo thu nhận dữ liệu thời gian thực từ sensor vào AWS.  
- Hiển thị dữ liệu IoT trong web app.  
- Xây dựng luồng end-to-end IoT → Web đầu tiên.

---

## 📋 Nhiệm vụ trong tuần

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ----- | ---------- | --------------- | ------------------ |
| 1 | - Cấu hình endpoint IoT Core <br>- Đăng ký IoT thing, certificate, policy <br>- Test MQTT publish/subscribe | 11/10/2025 | 11/10/2025 | AWS IoT Core Docs |
| 2 | - Tạo IoT Rule trigger Lambda <br>- Kiểm tra transform dữ liệu và routing vào S3/DynamoDB | 11/11/2025 | 11/11/2025 | IoT Rule Engine Docs |
| 3 | - Xây API (API Gateway + Lambda) để expose dữ liệu IoT cho webapp | 11/12/2025 | 11/12/2025 | API Gateway Docs |
| 4 | - Kết nối frontend với API <br>- Fetch và render dữ liệu thiết bị IoT lên UI | 11/13/2025 | 11/13/2025 | React + API Integration |
| 5 | - Test full pipeline: Sensor → IoT Core → Lambda → DB → API → Web UI <br>- Debug độ trễ và tính nhất quán dữ liệu | 11/14/2025 | 11/14/2025 | Ghi chú kiểm thử end-to-end |
