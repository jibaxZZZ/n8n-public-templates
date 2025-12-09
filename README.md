# 🧩 n8n Public Workflows by JibaxZZZ

A collection of production-ready, open-source **n8n** workflows built and maintained by [@JibaxZZZ](https://github.com/jibaxZZZ). These templates are designed to be plug-and-play for automation, monitoring, data extraction, and more.

---

## 📦 Workflows

| Workflow Name        | Description                                                                 | Tags                              |
|----------------------|-----------------------------------------------------------------------------|------------------------------------|
| **Uptime Monitor**   | Check website status via HTTP every 15s and feed a JSON dashboard           | `monitoring`, `uptime`, `cron`     |
| **Daily Reminder**   | Build a reminder payload once per day and send it to any notifier of choice | `reminder`, `cron`, `set`          |

Each workflow includes:
- A `.json` file ready to import in n8n
- A `README.md` with documentation and expected setup
- MIT license

---

## 📥 How to Use

1. Open [n8n](https://n8n.io/)
2. Go to `Workflows → Import from File`
3. Select the `.json` file of the workflow you want
4. Configure any needed credentials or URLs
5. Enable the workflow

---

## 📚 Directory Structure

```text
n8n-public-templates/
├── anomaly-watcher/
│   ├── detect-anomalies.json
│   └── README.md
├── uptime-monitor/
│   ├── services-ping-monitor.json
│   └── README.md
├── daily-reminder/
│   ├── daily-reminder.json
│   └── README.md
├── LICENSE
└── README.md
```

---

## 📖 License

All templates in this repository are released under the **MIT License**.  
Feel free to use, modify, and redistribute — no attribution required (though appreciated 🙏).

---

## 💬 Feedback & Contributions

You’re welcome to:
- Open an [issue](https://github.com/jibaxZZZ/n8n-public-templates/issues) for suggestions or bugs
- Fork and submit a PR with your own workflows
- Reach out on [LinkedIn](https://www.linkedin.com/in/jibril-gharib/) or [GitHub](https://github.com/jibaxZZZ)

---

> ⚡ Made with care for indie hackers, devs, and automation nerds.
