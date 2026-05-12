# bulk-github-org-settings-sync

Manages GitHub organization settings for `joshjohanning-org` using [bulk-github-org-settings-sync-action](https://github.com/joshjohanning/bulk-github-org-settings-sync-action).

## What's synced

| Feature | Config |
|---|---|
| Member privileges | Inline in workflow |
| Org profile | Inline in workflow |
| Actions policy | `actions-allow-list.yml` |
| Custom repo roles | `custom-repo-roles.yml` |

## Setup

The workflow uses a GitHub App for auth. Set these secrets on the repo:

| Secret | Value |
|---|---|
| `APP_CLIENT_ID` | App client ID (`Iv1.xxx`) |
| `APP_PRIVATE_KEY` | App private key (PEM) |

## Running

The workflow runs automatically:
- **On push** to `main` (e.g., when you update config files)
- **Weekly** on Monday at 2am UTC
- **Manually** via `workflow_dispatch` (with optional dry-run toggle)

To preview changes without applying, use the manual trigger with **Dry run** enabled.
