# Daily Reminder

A lightweight workflow that fires at 09:00 every morning and prepares a reminder payload you can forward to Slack, email, or any notifier.

## Usage

1. Import `daily-reminder.json` into n8n.
2. Connect a delivery node (Slack, webhook, email, etc.) to the `Daily Reminder` node.
3. Adjust the cron expression or message text as needed.

## Inside the workflow

- `Daily Cron`: schedule trigger that runs daily at `0 9 * * *`.
- `Daily Reminder`: Set node that holds a friendly task reminder plus the current ISO timestamp.
