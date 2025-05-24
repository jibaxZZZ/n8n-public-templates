


# 📡 n8n Workflow — System Anomaly Detection (CPU, RAM, Disk)

This workflow is part of the open-source project [anomaly-watcher](https://github.com/jibaxZZZ/anomaly-watcher).

## 🧠 Purpose

This `n8n` workflow receives system metrics from a Python monitoring script and sends a **Discord alert** when thresholds are exceeded (CPU, RAM, or disk usage).

## 🏗️ Architecture

- 📤 A **Python script** (`monitor.py`) sends system metrics via `POST` every few minutes
- 🌐 The workflow starts with an **HTTP Webhook Trigger**
- ⚙️ A **logic node** checks if any threshold is exceeded
- 📩 A **Discord message** is sent using a bot if anomalies are detected

---

## 📥 Expected Input JSON (sent by Python script)

```json
{
  "timestamp": "2025-05-24T10:59:30.465167Z",
  "cpu": 87.3,
  "ram": 72.1,
  "disk": {
    "/": 12.4,
    "/System/Volumes/Data": 92.3
  }
}
```

---

## 📈 Thresholds

| Resource | Threshold |
|----------|-----------|
| CPU      | > 90%     |
| RAM      | > 85%     |
| Disk     | > 95% on any partition |

---

## 🧪 Example Discord Alert Message

> Anomaly Watcher 🤖 APP
> — 14:51
>🚨 Anomaly Detected!
>
>🕒 2025-05-24T12:51:02.779782Z
>🧠 CPU: 12%
>🧵 RAM: 55.9%
>
>📀 Top Disk Usage:
>{"/":1.4,"/System/Volumes/VM":0,"/System/Volumes/Preboot":0.9,"/System/Volumes/Update":0,"/System/Volumes/xarts":1.2,"/System/Volumes/iSCPreboot":1.1,"/System/Volumes/Hardware":0.5,"/System/Volumes/Data":18,"/Library/Developer/CoreSimulator/Cryptex/Images/bundle/SimRuntimeBundle-9DEEED9B-21AF-452B-849E-BB712F060338":97.1,"/Library/Developer/CoreSimulator/Volumes/iOS_22D8075":97.5,"/Library/Developer/CoreSimulator/Cryptex/Images/bundle/SimRuntimeBundle-4FB79FA0-0A56-4117-B5BB-E342E24B70DB":97.1,"/Library/Developer/CoreSimulator/Volumes/iOS_22B81":97.5} }}

---

## 🔗 Related Resources

- 📁 Main Repository: [github.com/jibaxZZZ/anomaly-watcher](https://github.com/jibaxZZZ/anomaly-watcher)
- 🐍 Python Agent: `agent/monitor.py`
- 🐳 Docker Setup: `agent/docker-compose.yml`
- 🧠 Workflow JSON Export: `backend-n8n/detect-anomalies.json`

---

## 🚀 How to Use

1. Import `detect-anomalies.json` into your n8n instance
2. Activate the workflow
3. Point your Python agent to the webhook URL
4. (Optional) Set up a Discord bot and webhook integration

---

## 🔒 Security Note

- Use a token or IP whitelist to protect the webhook
- Do not expose your n8n instance publicly without reverse proxy and filtering

---

## 🧾 License

MIT — Feel free to reuse and adapt this workflow.