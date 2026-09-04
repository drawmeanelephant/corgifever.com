# Corgi Fever

Corgi Fever (`corgifever.com`) is a tiny boutique site about the fictional ailment known as **corgi fever**, compiled by [Boris](https://github.com/drawmeanelephant/boris) and deployed to Cloudflare Pages at [https://corgifever.com](https://corgifever.com).

It is deliberately small — three pages, no registry, no authority claims:

* `content/index.md` — what corgi fever is (fiction)
* `content/symptoms.md` — the reported signs (lore, not diagnosis)
* `content/about.md` — what this site is and is not

---

## Production Deployment

* **Source of Record**: `drawmeanelephant/corgifever.com`
* **Compiler**: [Boris](https://github.com/drawmeanelephant/boris) (CI tracks the `main` branch)
* **Production Theme**: Cantilever (`themes/cantilever/`)
* **Output Path**: `dist/cantilever/`
* **Host**: Cloudflare Pages (`corgifever`)
* **Public URL**: [https://corgifever.com](https://corgifever.com)

---

## Quick Start & Operating Commands

Build the primary site and serve it locally:

```sh
./preview.sh
```

The default output is written to `dist/cantilever/` and the server listens on `http://localhost:8000`.

Run the complete local validation gate:

```sh
./bin/validate_graph.sh
```

Primary build and publishing scripts:

* `./scripts/corgi-build.sh`: Runs the production HTML build.
* `./scripts/corgi-publish.sh`: Exports HTML, IR, RAG, Context, sitemap, and `llms.txt` artifacts.

---

## Repository Layout

```text
content/                    # Three-page boutique corpus (index, symptoms, about)
themes/cantilever/         # Primary production theme and templates
metadata/id-policy.json    # Boutique identity rules (trunk slugs, no form IDs)
metadata/id-map.jsonl      # Identity map
scripts/corgi-build.sh     # Production HTML build script
scripts/corgi-publish.sh   # HTML, IR, RAG, Context, and llms publishing script
bin/validate_graph.sh      # Graph integrity and publication gate
```

Generated outputs under `dist/`, `publish/`, `site/`, and local compiler binaries (`bin/boris*`) are build artifacts and must not be committed to git.
