<div align="center">

<img src="https://code-critic.com/logo.svg" alt="CodeCritic" width="220" />

# CodeCritic Reviews

**AI code review for GitHub pull requests** — GitHub Action, VS Code / Cursor extension, and REST API.

[![GitHub Marketplace](https://img.shields.io/badge/Marketplace-CodeCritic%20Review-8b5cf6?logo=github)](https://github.com/marketplace/actions/codecritic-review)
[![Website](https://img.shields.io/badge/website-code--critic.com-6366f1)](https://code-critic.com)
[![License](https://img.shields.io/badge/license-MIT-22c55e)](https://github.com/CodeCritic-Reviews/review-action/blob/main/LICENSE)

[Install the Action](https://github.com/marketplace/actions/codecritic-review) · [Free code review](https://code-critic.com/free-code-review) · [VS Code extension](https://marketplace.visualstudio.com/items?itemName=CodeCriticReviews.codecritic) · [Blog](https://blog.code-critic.com)

</div>

---

## What we build

| | | |
|---|---|---|
| 🤖 **[Review Action](https://github.com/CodeCritic-Reviews/review-action)** | AI review on every pull request — findings posted as PR comments, optional merge gate on severity. | [Marketplace](https://github.com/marketplace/actions/codecritic-review) |
| 🌐 **[Web app](https://code-critic.com)** | Paste code in the browser, review GitHub PRs, or call the REST API. Free tier, no card needed. | [Start free](https://code-critic.com/free-code-review) |
| 🧩 **[Editor extension](https://marketplace.visualstudio.com/items?itemName=CodeCriticReviews.codecritic)** | AI code review inside VS Code and Cursor — same API key as the web app. | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=CodeCriticReviews.codecritic) |
| 📝 **[Blog](https://blog.code-critic.com)** | Code review practices, security notes, and product updates. | [Read](https://blog.code-critic.com) |

## What the review looks like

Open a pull request and CodeCritic posts a comment with line-level findings: bugs, security risks, and quality issues — each with a plain-language fix. Findings are advisory; humans keep merge ownership.

```yaml
name: CodeCritic Review
on: [pull_request]

permissions:
  contents: read
  pull-requests: write

jobs:
  review:
    runs-on: ubuntu-latest
    steps:
      - uses: CodeCritic-Reviews/review-action@v1
        with:
          api_key: ${{ secrets.CODECRITIC_API_KEY }}
```

That's the whole setup. Free tier included — [get an API key](https://code-critic.com/free-code-review).

## Honest scope

CodeCritic uses AI models to analyze code. Results may contain inaccuracies and are not a substitute for human review of critical systems. We document [what AI review does not catch](https://code-critic.com/ai-code-review-limitations) — and we think you should ask that question of every AI review tool.

## Contact

- 🐛 Issues & feature requests: [review-action issues](https://github.com/CodeCritic-Reviews/review-action/issues)
- 📧 support@code-critic.com
- 🔒 Security disclosures: [SECURITY.md](https://github.com/CodeCritic-Reviews/review-action/blob/main/SECURITY.md)
