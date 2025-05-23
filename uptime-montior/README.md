# 📡 Uptime Monitor

This n8n workflow allows you to monitor the availability of one or multiple websites or APIs. It sends HTTP requests every 15 seconds and writes the results (status code, response time, timestamp) to a JSON file. This file is then used by a frontend dashboard for real-time visualization.

---

## 🔧 Features

- ⏱️ Runs every 15 seconds using a Cron trigger
- 🌐 Checks multiple URLs via HTTP GET
- 📉 Measures response time and status code
- 🧠 Maintains a `history[]` of status and response times per site
- 📝 Updates a JSON file on disk (per-client basis) via HTTP POST

---

## 🗂 Structure

```json
{
  "id": "https://example.com",
  "status": 200,
  "responseTime": 123,
  "timestamp": "2025-05-23T15:11:20.287Z",
  "history": [
    { "timestamp": "...", "status": 200, "responseTime": 111 },
    ...
  ]
}