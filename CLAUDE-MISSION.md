# Claude Mission & Repository Mandates

## Repository Goal
Maintain the tiny **Corgi Fever** (`corgifever.com`) boutique site about the fictional ailment, using the **Boris** static compiler.

## Core Rules
1. **Engine**: Static site output is rendered by Boris. Do not add JavaScript frameworks or static site generators (Vite, Next, Astro, Eleventy, etc.).
2. **Scope**: Three trunk pages only — `index`, `symptoms`, `about`. No registries, no form-ID satellites (`CRG-XXXX`, `LIN-XXXX`, etc.). Do not reintroduce them without asking.
3. **Voice**: Deadpan boutique lore. Fiction only — no medical, veterinary, breed, or training authority, no unproven claims.
4. **Graph Integrity**: All pages are trunks with no parent.
5. **Verification Gate**: `./bin/validate_graph.sh` must succeed clean before any release or commit.
