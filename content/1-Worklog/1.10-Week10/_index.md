---
title: "Week 10 Worklog"
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---

## 🎯 Objectives
- Connect the IoT device → AWS IoT Core → backend pipeline.
- Ensure real-time data ingestion from sensor into AWS.
- Display IoT data inside the web application.
- Build the first functional end-to-end IoT → Web flow.

---

## 📋 Tasks for this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ----- | ---------- | --------------- | ------------------ |
| 1 | - Configure IoT Core endpoint <br>- Register IoT thing, certificates, and policies <br>- Test MQTT publish/subscribe | 11/10/2025 | 11/10/2025 | AWS IoT Core Docs |
| 2 | - Implement IoT Rule to trigger Lambda <br>- Validate data transformation and routing into S3/DynamoDB | 11/11/2025 | 11/11/2025 | IoT Rule Engine Docs |
| 3 | - Build API (via API Gateway + Lambda) to expose IoT data to webapp | 11/12/2025 | 11/12/2025 | API Gateway Docs |
| 4 | - Connect frontend web app to the API <br>- Fetch and render IoT device data in UI | 11/13/2025 | 11/13/2025 | React + API Integration |
| 5 | - Test full pipeline: Sensor → IoT Core → Lambda → DB → API → Web UI <br>- Debug latency and data consistency | 11/14/2025 | 11/14/2025 | End-to-End Test Notes |