# StarPlan Talent Assessment — Demo

Interactive single-page demo of the StarPlan AI Product Manager talent-assessment prototype.

**Live site:** https://difeili9.github.io/starplan-demo/

## Contents

| Path | Purpose |
| --- | --- |
| `site/index.html` | Self-contained single-file demo (React bundle inlined, no build step) |
| `.github/workflows/deploy-pages.yml` | GitHub Actions workflow that publishes `site/` to GitHub Pages |

## How deployment works

Every push to `main` triggers `Deploy StarPlan Demo to GitHub Pages`:

1. `actions/configure-pages` prepares the Pages configuration.
2. `actions/upload-pages-artifact` packages the `site/` folder.
3. `actions/deploy-pages` publishes it at https://difeili9.github.io/starplan-demo/

To update the demo, replace `site/index.html` and push. You can also re-run the
workflow manually from the **Actions** tab (`workflow_dispatch`).

## Notes

- The demo is one static HTML file; no build tooling or dependencies are required.
- External dependency: Google Fonts ("Plus Jakarta Sans"). If it is unreachable the
  page still works and falls back to system fonts.
- Prototype data is stored in the browser (localStorage); nothing is sent to a server.
