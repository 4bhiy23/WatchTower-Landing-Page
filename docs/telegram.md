# Telegram reports

Telegram is optional. When configured, Watchtower sends a compact daily report after the scan finishes.

## Create your bot

1. Open **@BotFather** in Telegram.
2. Send <code>/newbot</code>.
3. Choose a bot display name and username.
4. Copy the token BotFather gives you.
5. Open a chat with your bot and send <code>/start</code>.

## Find your chat ID

Open this URL in a browser after replacing <code>BOT_TOKEN</code> locally:

~~~text
https://api.telegram.org/botBOT_TOKEN/getUpdates
~~~

Look for:

~~~json
{
  "message": {
    "chat": {
      "id": 123456789
    }
  }
}
~~~

Use that <code>id</code> value. For a group, add the bot to the group and send a message there before requesting updates.

## Add Actions secrets

In your Watchtower repository, open **Settings → Secrets and variables → Actions**:

| Secret name | Value |
| --- | --- |
| <code>TELEGRAM_BOT_TOKEN</code> | Token from BotFather |
| <code>TELEGRAM_CHAT_ID</code> | Chat or group ID |

The Telegram workflow step runs only when **both** secrets exist.

## What the report contains

| Section | Meaning |
| --- | --- |
| Changes | Differences since the previous scan |
| Security issues | Current OSV vulnerabilities and fixed versions |
| Major updates | Available new major releases |
| Routine updates | Minor or patch releases without known security issues |
| Deprecated packages | Dependencies marked deprecated by npm |

With <code>settings.publicDashboard: true</code>, the report includes a dashboard link. Otherwise it stays link-free.

## Test before waiting for the schedule

Run a scan locally first, then preview the report without sending it:

~~~bash
pnpm telegram -- --dry-run
~~~

To test delivery from GitHub, manually run **Actions → Watchtower scan → Run workflow** after adding the secrets.

Return to the [documentation index](README.md).
