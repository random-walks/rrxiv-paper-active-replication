# Many small claims, all under active replication

A paper that registers its own seven claims for active replication while arguing, from those same claims, that pre-registration pulls replication completion forward by about six weeks — a demonstration paper in the [rrxiv](https://rrxiv.com) reference corpus.

**Read the published paper:** [rrxiv.com/papers/rrxiv:2605.00008](https://rrxiv.com/papers/rrxiv:2605.00008)

## What this demonstrates

A double-duty paper: it pre-registers its own claims for replication and, in the same document, argues that pre-registration shifts replication completion forward by roughly six weeks. Seven claims, each individually addressable and marked for active replication — a worked example of the claim graph carrying process metadata, not just findings.

## The annotations

The seven pre-registrations live in [`annotations/`](./annotations/) as real protocol objects: `annotation.schema.json`-valid documents with `annotation_type: comment` (the v0.1 enum has no dedicated `active_replication` type, and a pre-registration has no outcome yet, so `replication` would be wrong — see §3.1 of the paper). They are posted to the live instance against the claim ids `rrxiv:2605.00008:claim:c1`…`c7` and queryable via `GET /annotations?target_id=<claim-id>&target_type=claim`. Annotations are post-submission discourse held by the instance; they do not appear in the build-time CIR sidecar. The team handles in the registry are illustrative — the registrations are posted by the paper's own authors as reference-corpus demonstrations, and each annotation says so.

## Build it locally

This repo was created from the [rrxiv-paper-template](https://github.com/random-walks/rrxiv-paper-template).

```bash
./scripts/build.sh          # tectonic → build/main.pdf
./scripts/extract-cir.sh    # rrxiv parse → build/main.cir.json
./scripts/verify.sh         # validate the CIR against the rrxiv schema
```

Install the `rrxiv` CLI used by these scripts:

```bash
pip install 'rrxiv>=0.2.1'
```

## License

Dual-licensed, matching the rest of the corpus:

- **Content** — the paper text and figures in `paper/`, plus `rrxiv-meta.json`, under [CC-BY-4.0](./LICENSE-CONTENT).
- **Code** — the `scripts/` and CI under [MIT](./LICENSE-CODE).
