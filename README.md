# artifacts

Static assets for [fool@40](https://fat40.github.io).

<img src="52538.png" alt="icon" width="120">

## Contents

| File | Description |
| --- | --- |
| `52538.png` | Icon, 400x400 PNG |

## Usage

Reference assets through a release tag so the URL never changes under you:

```
https://raw.githubusercontent.com/fat40/artifacts/<tag>/<file>
```

For example, `https://raw.githubusercontent.com/fat40/artifacts/0.2639.1/52538.png`.
Use `main` in place of a tag to always get the latest version.

## Versioning

Releases follow [HeadVer](https://github.com/line/headver): `{head}.{yearweek}.{build}`.

| Part | Meaning | Example |
| --- | --- | --- |
| `head` | Zero-based, bumped manually for breaking changes | `0` |
| `yearweek` | 2-digit ISO year + ISO-8601 week number | `2639` (2026, week 39) |
| `build` | Commit count on `main` | `1` |

Tags have no `v` prefix. See [tags](https://github.com/fat40/artifacts/tags) for all releases.

To cut a release from `main`:

```bash
V="0.$(date +%g%V).$(git rev-list --count HEAD)"
git tag -a "$V" -m "$V"
git push origin "$V"
```
