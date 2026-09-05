# GitHub Metrics setup

The README now uses the real [lowlighter/metrics](https://github.com/lowlighter/metrics) GitHub Action.

## One-time setup

1. Create a GitHub personal access token with the least privileges required for the plugins. For public repositories, start with a token that can read public profile and repository data.
2. Open the `tharunstryker` profile repository on GitHub.
3. Go to **Settings → Secrets and variables → Actions → New repository secret**.
4. Create a secret named `METRICS_TOKEN` and paste the token value.
5. Open **Actions → GitHub Metrics → Run workflow**.
6. After the workflow completes, `github-metrics.svg` will be committed to the repository automatically.

The workflow also refreshes once per day at 00:17 UTC and runs when the repository is updated. The generated SVG is intentionally committed to the profile repository so the README can load it with a stable relative path.

## Important

Do not put the token in `README.md`, the workflow file, or any committed source file. If the repository later includes private-repository metrics, organization metrics, package metrics, or other restricted plugins, add only the specific token scopes documented by the corresponding Metrics plugin.
