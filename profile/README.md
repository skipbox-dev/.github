# Skipbox

**Your own warm GitHub Actions runner at a flat monthly price.** Minutes are unlimited, there are no usage charges, and Docker layers and package caches stay on your machine between jobs.

[skipbox.dev](https://skipbox.dev/?ref=gh-org-profile) · [Pricing](https://skipbox.dev/pricing) · [Docs](https://docs.skipbox.dev/quickstart) · [Cost calculator](https://skipbox.dev/tools/github-actions-cost)

## Move a job in one line

```yaml
jobs:
  build:
    runs-on: skipbox   # was: ubuntu-latest
```

Install the Skipbox GitHub App on a GitHub organization or a personal account, change `runs-on`, and the job runs on Skipbox. Everything else in the workflow stays as it is. Skipbox can also open the pull request that changes the `runs-on` lines for you.

## Plans

| Plan | Price a month | CPU · memory · disk | Largest `runs-on` label |
| --- | --- | --- | --- |
| S | $39 | 4 vCPU · 8 GB · 80 GB | `skipbox` |
| M | $79 | 8 vCPU · 16 GB · 160 GB | `skipbox-8x16` |
| L | $149 | 16 vCPU · 32 GB · 320 GB | `skipbox-16x32` |

- Unlimited minutes on every plan. Hold any number of plans in any mix, and their concurrent jobs add up.
- Free trial: 7 days or 3,000 job-minutes, whichever comes first. No card.
- Faster than GitHub on your own jobs within 30 days of your first payment, or your money back ([Terms §7](https://skipbox.dev/legal/terms#section-7)).

## What a job gets

- **Kept between jobs:** Docker images, layers and build cache; npm, pip, Go, Gradle and Cargo caches; the tool cache that `setup-*` actions fill.
- **Wiped after every job:** the runner's credentials, the work directory, the runner user's processes and every container, and credential files such as `~/.npmrc`.
- **A fresh VM, deleted after the job,** for pull requests from forks, or for every job if you turn on "Clean every job".
- Ubuntu 24.04 on x64 with Docker, Node 22 and Python 3.12. Up to 6 hours per job.
- Linux x64 jobs in private repositories. macOS, Windows, Arm and public-repository jobs stay where they run today.

## Why teams move

GitHub bills hosted runners for every minute a job runs. Self-hosted runner minutes are free on GitHub, and Skipbox is a self-hosted runner you don't have to operate: you pay one flat price, not the minutes.

- [Flat-price GitHub Actions runners](https://skipbox.dev/guides/flat-price-github-actions-runners)
- [GitHub Actions cost calculator: work out your bill](https://skipbox.dev/guides/github-actions-cost-calculator)
- [Jobs stopped by a spending limit: get CI running today](https://skipbox.dev/guides/github-actions-spending-limit-job-not-started)
- [Are GitHub self-hosted runners free?](https://skipbox.dev/guides/are-github-self-hosted-runners-free)
- [GitHub Actions runners compared](https://skipbox.dev/compare/github-actions-runners-compared)
- [GitHub Actions pricing changes in 2026](https://skipbox.dev/blog/github-actions-pricing-changes-2026)

## For coding agents

[skipbox-dev/skills](https://github.com/skipbox-dev/skills) teaches Claude Code, Codex and other agents to move a repository's jobs to Skipbox. Every page on skipbox.dev and docs.skipbox.dev is also served as Markdown: see [llms.txt](https://skipbox.dev/llms.txt).

## Contact

hello@skipbox.dev · [Support](https://skipbox.dev/support) · Skipbox is run by [Fluxenic Inc.](https://skipbox.dev/company), Tokyo.
