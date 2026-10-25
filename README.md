# Faraday's fuzz corpora

The inputs Faraday's fuzz targets have grown, minimized, one commit per
release, tagged with the release's tag (`v0.1.7`, …). Faraday's
repository is https://github.com/bitcoinpasada/faraday.

Each folder is one fuzz target of Faraday's `fuzz/` or `faraday/fuzz/`
workspace, as `just fuzz-corpus-export` writes them
(`tools/fuzz-corpus-export.sh`, `cargo fuzz cmin`).

To reproduce a release's run: check out Faraday at the release's tag,
check this repository out at the commit the release notes quote, and run
`FARADAY_FUZZ_CORPUS=<this checkout> just fuzz-release` (Faraday's
`fuzz/README.md`, "Before a release").
