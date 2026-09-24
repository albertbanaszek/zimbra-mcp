# Fork and upstream

This repository is a fork of
[jeremie-lesage/zimbra-mcp](https://github.com/jeremie-lesage/zimbra-mcp).
Local changes are developed and published in the fork
[albertbanaszek/zimbra-mcp](https://github.com/albertbanaszek/zimbra-mcp).

## Remotes

| Remote     | URL                                                | Role                              |
|------------|----------------------------------------------------|-----------------------------------|
| `origin`   | https://github.com/albertbanaszek/zimbra-mcp.git   | fork — own commits are pushed here |
| `upstream` | https://github.com/jeremie-lesage/zimbra-mcp.git   | original — fetch only             |

The working branch `develop` tracks `origin/develop`.

To reproduce this setup in a fresh clone:

```powershell
git clone https://github.com/albertbanaszek/zimbra-mcp.git
cd zimbra-mcp
git remote add upstream https://github.com/jeremie-lesage/zimbra-mcp.git
```

## Syncing with upstream

```powershell
git fetch upstream
git merge upstream/develop
git push
```

## Commit convention

This project is not tied to Azure DevOps, so commit messages do **not**
include a work-item number (`#NNNNN`). Use the
[Conventional Commits](https://www.conventionalcommits.org/) style that
upstream uses, for example:

```
feat(emails): add search_folder tool
fix(attachments): send auth token as cookie instead of query string
docs: update README with new tools and dev section
```
