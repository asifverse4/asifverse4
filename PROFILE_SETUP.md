# Profile Setup (Animated Chemistry Dashboard)

## What this profile uses

- `README.md` as the dashboard surface (tables, badges, Mermaid, details blocks)
- Custom animated SVG assets in `/assets`:
  - `hero.svg` (main identity banner)
  - `research-loop.svg` (pipeline visual)
  - `orbit-panel.svg` (decorative status panel)
- Dynamic external cards already GitHub-safe (`github-readme-stats`, `streak-stats`, shields)

## Contribution snake workflow

Workflow file: `.github/workflows/snake.yml`

- Runs daily and on manual trigger
- Uses only `GITHUB_TOKEN`
- Requires `contents: write` permission
- Publishes generated snake SVGs to the `output` branch

Expected output files on `output` branch:

- `github-contribution-grid-snake.svg`
- `github-contribution-grid-snake-dark.svg`

## First-run notes

1. Ensure Actions are enabled for the repository.
2. Run **Generate Contribution Snake** once via **Run workflow**.
3. Confirm the `output` branch appears with generated SVG files.
4. README snake image path should resolve from:
   `https://raw.githubusercontent.com/asifverse4/asifverse4/output/github-contribution-grid-snake-dark.svg`
