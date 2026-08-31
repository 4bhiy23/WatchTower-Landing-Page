# Private repository access

Watchtower uses a fine-grained GitHub personal access token only to clone private monitored repositories. It needs **read-only** repository access.

## Create the token

1. Open GitHub **Settings → Developer settings → Personal access tokens → Fine-grained tokens**.
2. Select **Generate new token**.
3. Choose the account or organization that owns the private repository as **Resource owner**.
4. Under **Repository access**, select the repositories Watchtower may scan.
5. Under **Repository permissions**, set **Contents** to **Read-only**.
6. Generate the token and copy it.

## Add it to GitHub Actions

In the Watchtower repository:

1. Open **Settings → Secrets and variables → Actions**.
2. Select **New repository secret**.
3. Name it <code>WATCHTOWER_GITHUB_TOKEN</code>.
4. Paste the token and save.

Never put this value in <code>config/projects.yml</code>, a commit, an issue, or a chat message.

## Add it to Private Docker mode

Create <code>.env.private</code> from the provided example and add:

~~~env
WATCHTOWER_GITHUB_TOKEN=github_pat_your_token_here
~~~

Then recreate the scanner so it reloads the secret:

~~~bash
pnpm docker:private:start
~~~

## Common access failures

| Error | Likely reason | Fix |
| --- | --- | --- |
| <code>Repository not found</code> | Wrong URL, token owner, or repository selection | Check URL and selected repository access |
| <code>could not read Username</code> in Docker | Scanner did not receive a token or GitHub denied it | Check <code>.env.private</code>, then restart Docker |
| Token works for one repository but not another | Fine-grained token did not select every private repository | Add that repository to token access or create a new token |
| Organization repository is unavailable | Organization approval or SSO is required | Ask the organization owner to approve/authorize the token |

Public repositories are cloned anonymously first. A token restricted to one private repository does not stop public scans.

Return to the [documentation index](README.md).
