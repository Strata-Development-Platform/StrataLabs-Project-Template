# StrataLabs website integration

The StrataLabs website synchronizes public repository content approximately once per hour. It caches the last successful result so GitHub availability does not affect normal page rendering.

## Discovery

A repository is eligible when it is public, not archived, and has the GitHub topic `stratalabs-project`. The synchronizer then looks for `.stratalabs/project.json`.

## Project metadata

Required:

- `$schemaVersion`: currently `1`
- `displayName`: public project name
- `shortDescription`: card summary
- `longDescription`: detail-page introduction
- `category`: one of `application`, `framework`, `library`, `cli`, `integration`, `documentation`, or `other`
- `lifecycle`: one of `incubating`, `active`, `stable`, `maintenance`, or `archived`
- `featured`: homepage eligibility
- `weight`: lower numbers appear first

Optional links must be fully qualified HTTPS URLs or `null`.

## Roadmap

Roadmap statuses are `planning`, `active`, `paused`, and `complete`. Milestone statuses are `planned`, `in-progress`, `complete`, and `cancelled`.

Milestone IDs must remain stable because the website uses them when comparing cached versions.

## Documentation

Markdown under `docs/` is rendered inside StrataLabs-themed documentation components. Scripts, embedded HTML, iframes, and unsafe URL schemes are stripped. Use relative links for files in the same repository.

## Releases

The Releases page uses published GitHub Releases. Draft releases are ignored. Pre-releases are visibly labeled. Release titles, tags, notes, assets, and publication dates come from GitHub.

## Migration checklist

- Copy `.stratalabs/`, `docs/`, and the community health files into the project.
- Replace all `REPLACE_ME` values.
- Validate both JSON files.
- Add the `stratalabs-project` repository topic.
- Confirm README and documentation links.
- Publish or verify the latest GitHub Release.
- Confirm the repository license.
- Wait for synchronization and review the rendered project page.
