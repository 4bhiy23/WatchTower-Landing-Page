# Private Docker mode

Private Docker mode runs Watchtower on your own machine. It has no GitHub Pages deployment, no scheduled scans, and no Telegram delivery. You decide when to scan by using the dashboard button.

## Start it

1. Add repositories to `config/projects.yml`.
2. Copy the local secret template:

   ```bash
   cp .env.private.example .env.private
   ```

3. For private monitored repositories, put a read-only GitHub token in `WATCHTOWER_GITHUB_TOKEN`.
4. Start the local services:

   ```bash
   pnpm docker:private:start
   ```

5. Open [http://localhost:8787](http://localhost:8787).

The dashboard initially shows the number and names of repositories in `config/projects.yml`. Select **Scan repositories** to begin a scan. The scanner permits one active scan at a time and reports project-by-project progress.

## Privacy model

- The dashboard listens only on `127.0.0.1`, so it is not reachable from your local network.
- Scan results are written to `runtime/data/`, which is ignored by Git.
- The GitHub token stays in `.env.private` and is passed only to the scanner container.
- Docker mode does not schedule scans, publish GitHub Pages, send Telegram reports, or commit generated data.

## Useful commands

```bash
# Follow local scanner activity
pnpm docker:private:logs

# Stop local Watchtower
pnpm docker:private:stop
```
