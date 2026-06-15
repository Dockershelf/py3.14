# py3.14

Debian packaging for CPython 3.14: patches, `debiandirs/`, and changelog tracks used by the [Dockershelf python-pipeline](https://github.com/Dockershelf/python-pipeline).

## Supported Debian suites

- `trixie`
- `unstable`

Packaging trees live under `debiandirs/<suite>/`. Changelogs live under `changelogs/mainline/<suite>`.

## Build (from workspace)

Clone this repo as a sibling of `python-pipeline/`, then from `python-pipeline/`:

```bash
make materialize PY=3.14 DIST=trixie
make build PY=3.14 DIST=trixie
```

See the [operations manual](https://github.com/Dockershelf/python-pipeline/blob/main/docs/operations.md) for new lines, version bumps, and new suites.

## Layout

| Path | Purpose |
|------|---------|
| `cpython/` | Upstream CPython git submodule |
| `patches/` | Quilt series applied at materialize |
| `debiandirs/` | Per-suite Debian packaging (`trixie`, `unstable`) |
| `changelogs/mainline/` | Debian changelog history per suite |
