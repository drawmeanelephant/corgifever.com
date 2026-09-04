# Corgi Fever — Project Rules

1. **Static Site Build System**:
   - Compiler: Boris (Zig)
   - Input: `content/`
   - Output: `dist/cantilever/`
   - Theme: `themes/cantilever/`

2. **Scope**:
   - Boutique site about the fictional ailment "corgi fever": `index`, `symptoms`, `about`.
   - No registry, no bloodlines, no breed standards, no health/training authority.
   - Fiction only. No medical, veterinary, or breed claims.

3. **Frontmatter Constraints**:
   - Allowed fields: `id`, `title`, `parent`, `status`, `tags`, `relations`.
   - Do not use arbitrary or unsupported frontmatter keys.

4. **Validation & Deployment**:
   - Run `./bin/validate_graph.sh` to check graph diagnostics and IDs.
   - Cloudflare Pages deploys `dist/cantilever` via GitHub Actions (`.github/workflows/deploy.yml`).
