# Many small claims, all under active replication

A paper that registers its own seven claims for active replication while arguing, from those same claims, that pre-registration pulls replication completion forward by about six weeks — a demonstration paper in the [rrxiv](https://rrxiv.com) reference corpus.

**Read the published paper:** [rrxiv.com/papers/rrxiv:2605.00008](https://rrxiv.com/papers/rrxiv:2605.00008)

## What this demonstrates

A double-duty paper: it pre-registers its own claims for replication and, in the same document, argues that pre-registration shifts replication completion forward by roughly six weeks. Seven claims, each individually addressable and marked for active replication — a worked example of the claim graph carrying process metadata, not just findings.

## Build it locally

This repo was created from the [rrxiv-paper-template](https://github.com/random-walks/rrxiv-paper-template).

```bash
./scripts/build.sh          # tectonic → build/main.pdf
./scripts/extract-cir.sh    # rrxiv parse → build/main.cir.json
./scripts/verify.sh         # validate the CIR against the rrxiv schema
```

The `rrxiv` CLI used by these scripts isn't on PyPI yet — install it from source:

```bash
pip install "rrxiv @ git+https://github.com/random-walks/rrxiv-python.git"
```

## License

Dual-licensed, matching the rest of the corpus:

- **Content** — the paper text and figures in `paper/`, plus `rrxiv-meta.json`, under [CC-BY-4.0](./LICENSE-CONTENT).
- **Code** — the `scripts/` and CI under [MIT](./LICENSE-CODE).
