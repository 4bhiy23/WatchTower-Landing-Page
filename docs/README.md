# Watchtower documentation

Choose the path that matches how you want to use Watchtower.

| Path | Best for | Hosting cost | Public by default? | Scan trigger |
| --- | --- | ---: | --- | --- |
| [GitHub Actions](github-actions.md) | Daily monitoring without a server | $0* | No | Daily schedule or manual run |
| [Private Docker](private-docker.md) | Keeping results on your computer | $0 | No | **Scan repositories** button |

*Subject to your GitHub Actions allowance.

## Setup map

~~~text
                           ┌──────────────────────┐
                           │ Configure projects   │
                           │ config/projects.yml  │
                           └──────────┬───────────┘
                                      │
                 ┌────────────────────┴─────────────────────┐
                 │                                          │
       ┌─────────▼─────────┐                      ┌─────────▼─────────┐
       │ GitHub Actions    │                      │ Private Docker    │
       │ daily automation  │                      │ local dashboard   │
       └──────┬─────┬──────┘                      └───────────────────┘
              │     │
   ┌──────────▼┐  ┌─▼────────────────┐
   │ Telegram  │  │ Public Pages      │
   │ optional  │  │ explicit opt-in   │
   └───────────┘  └───────────────────┘
~~~

## Guides

| Guide | What it covers |
| --- | --- |
| [GitHub Actions setup](github-actions.md) | Forking, projects, first scan, schedule, data storage |
| [Private repositories](private-repositories.md) | Fine-grained token permissions and common failures |
| [Telegram reports](telegram.md) | Bot creation, chat IDs, secrets, report contents |
| [Private Docker mode](private-docker.md) | Local dashboard, commands, and privacy model |

## Configuration reference

| File or setting | Purpose | Safe default |
| --- | --- | --- |
| <code>config/projects.yml</code> | Projects to scan and dashboard choice | No projects; Pages disabled |
| <code>settings.publicDashboard</code> | Enables GitHub Pages deployment | <code>false</code> |
| <code>WATCHTOWER_GITHUB_TOKEN</code> | Read access to private monitored repositories | Not set |
| <code>TELEGRAM_BOT_TOKEN</code> / <code>TELEGRAM_CHAT_ID</code> | Enables Telegram reports | Not set |
| <code>.github/workflows/watchtower.yml</code> | Daily scan schedule | 8:00 AM IST |

## Quick answers

| Question | Answer |
| --- | --- |
| Does Watchtower modify my projects? | No. It clones and reads them only. |
| Must I enable GitHub Pages? | No. Pages is optional and disabled by default. |
| Can I scan private repositories? | Yes, with a fine-grained, read-only GitHub token. |
| Can I use it without GitHub Actions? | Yes, use Private Docker mode. |
| Does it upgrade packages automatically? | No. It reports facts; you choose changes. |

Return to the [main README](../README.md) for the full project overview.
