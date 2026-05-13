# sync-github-org-settings

🔄 Syncs configuration across a set of organizations using the [bulk-github-org-settings-sync-action](https://github.com/joshjohanning/bulk-github-org-settings-sync-action) 🚀

## How It Works

A GitHub Actions workflow runs the sync action, which reads [`orgs.yml`](orgs.yml) and pushes the referenced config files to each listed repository. This keeps org settings in sync and consistent across orgs without manual updates.

Each entry in `orgs.yml` maps a organization to its settings and configuration. Adding a new org or changing a shared config is a single PR in this repo.

## Folder Structure

```text
orgs.yml                           # List of orgs to sync
config/                            # Configuration files used by the sync (contents may vary)
```
