# StrataLabs Project Template

Use this repository as the baseline for public projects displayed on the StrataLabs website.

## What the website reads

The hourly StrataLabs synchronizer reads:

- `.stratalabs/project.json` for presentation metadata and external links
- `.stratalabs/roadmap.json` for the public project roadmap
- `README.md` for the project overview
- `docs/index.md` and other Markdown files under `docs/` for documentation
- GitHub Releases for version history and downloadable assets
- GitHub repository metadata for language, license, stars, topics, and activity

The website owns all visual presentation. Repository files provide content only and cannot override the StrataLabs theme.

## Starting a project

1. Create a repository from this template.
2. Replace every `REPLACE_ME` value.
3. Update the project metadata and roadmap.
4. Add the GitHub topic `stratalabs-project`.
5. Publish at least one GitHub Release when the project is ready.
6. Validate JSON files before merging.
7. Wait for the hourly website synchronization or run a manual sync.

## Required files

| File | Purpose |
| --- | --- |
| `.stratalabs/project.json` | Project identity, lifecycle, ordering, and external links |
| `.stratalabs/roadmap.json` | Roadmap status and milestones |
| `README.md` | Repository and website overview |
| `docs/index.md` | Documentation landing page |
| `CHANGELOG.md` | Human-readable project history |
| `CONTRIBUTING.md` | Contribution workflow |
| `SECURITY.md` | Vulnerability reporting policy |

See [docs/stratalabs-integration.md](docs/stratalabs-integration.md) for the complete field reference and migration checklist.

## Project overview

> Replace this section with a concise explanation of the project, its intended users, and the problem it solves.

## Quick start

```bash
# Replace with real installation and startup commands
git clone https://github.com/Strata-Development-Platform/REPLACE_ME.git
cd REPLACE_ME
```

## Documentation

Start with [the documentation index](docs/index.md).

## License

MIT unless replaced before the first public release.
