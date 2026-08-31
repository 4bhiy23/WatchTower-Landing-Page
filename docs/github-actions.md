# GitHub Actions setup

This mode scans configured projects every day using a temporary GitHub-hosted runner. There is no server to provision, maintain, or pay for.

## Before you begin

| You need | Why |
| --- | --- |
| Your own Watchtower repository | Holds configuration and scan history |
| A GitHub account | Runs the scheduled workflow |
| Optional GitHub token | Required only for private monitored repositories |
| Optional Telegram bot | Required only for Telegram reports |

## Setup checklist

- [ ] Copy or fork Watchtower into your GitHub account.
- [ ] Edit <code>config/projects.yml</code>.
- [ ] Set Actions permissions to **Read and write**.
- [ ] Add a private-repository token only if required.
- [ ] Run **Actions → Watchtower scan → Run workflow**.
- [ ] Optionally enable Telegram and/or Pages.

## 1. Configure projects

Use a full GitHub HTTPS clone URL:

~~~yaml
settings:
  publicDashboard: false

projects:
  - id: storefront
    name: Storefront
    source:
      type: github
      repository: https://github.com/acme/storefront.git
      ref: main
~~~

| Field | Meaning | Example |
| --- | --- | --- |
| <code>id</code> | Stable internal identifier; must be unique | <code>storefront</code> |
| <code>name</code> | Human-friendly display name | <code>Storefront</code> |
| <code>repository</code> | HTTPS clone URL | <code>https://github.com/acme/storefront.git</code> |
| <code>ref</code> | Optional branch | <code>main</code> |

Add one entry per monitored repository. Do not use a local Mac path in GitHub Actions mode; a GitHub runner cannot access your computer.

## 2. Allow the workflow to save history

In your Watchtower repository open **Settings → Actions → General**. Under **Workflow permissions**, select **Read and write permissions**, then save.

This lets Watchtower commit generated <code>data/</code> history into its own repository. It does not grant Watchtower write access to monitored repositories.

## 3. Run the first scan

1. Commit and push <code>config/projects.yml</code>.
2. Open **Actions**.
3. Select **Watchtower scan**.
4. Choose **Run workflow** and the branch containing your configuration.
5. Wait for the scan job to finish.

The first run creates a baseline. Later runs store factual changes against it.

## 4. Choose optional delivery

| Feature | How to enable it | Important note |
| --- | --- | --- |
| Telegram report | Follow [Telegram reports](telegram.md) | No bot secret = no report |
| Public dashboard | Set <code>publicDashboard: true</code>, then enable Pages → GitHub Actions | Dashboard data becomes shareable |
| Private local dashboard | Follow [Private Docker mode](private-docker.md) | Separate from Actions mode |

## Change the schedule

The default is 8:00 AM India Standard Time:

~~~yaml
# .github/workflows/watchtower.yml
- cron: "30 2 * * *"
~~~

GitHub Actions uses UTC. For 9:00 AM IST, use <code>30 3 * * *</code>. You can always use **Run workflow** for an immediate scan.

## What each run stores

~~~text
data/current.json                         latest snapshot
data/changes.json                         change events since prior scan
data/history-index.json                   dates available per project
data/history/YYYY/MM/YYYY-MM-DD.json      daily snapshots
~~~

See the [documentation index](README.md) for the remaining guides.
