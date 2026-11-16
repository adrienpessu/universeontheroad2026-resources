# Speaker Guide: Agentic Security for Every Developer

## Session overview

This session introduces GitHub's approach to agentic security, demonstrating how GitHub Advanced Security and Copilot help developers detect, prevent, and remediate security vulnerabilities throughout the software development lifecycle.

**Core message:** Security needs to keep pace with AI-driven development. GitHub is bringing security directly into developer workflows, using AI agents to identify and fix vulnerabilities earlier and at scale.

### Before you present

- Review the presentation deck and AI session summary for additional talking points.
- Familiarise yourself with GitHub Advanced Security, CodeQL, AI scanning, and Agentic Autofix.
- Confirm access to the demo environments and enabled features.
- Prepare completed scans and remediation pull requests as backups.
- Rehearse the guest demo handoff if delivering with a second presenter.

**Session timing:** Approximately 15 minutes of slides and 25 minutes of demonstrations.

#### Get prepared

- Install the Advanced Security plugins in the Copilot app so the Security canvas is available, then open it with the existing findings loaded.
- In the Copilot app, import the repository, create a new session, and say “hello” in chat. Then use the right panel to browse the repository files.
go to open `products/urls.py` and replace the content with :

```python
from django.urls import path

from . import catalog, views

app_name = 'products'

urlpatterns = [
    path('', catalog.ProductList.as_view(), name='list'),
    path('products/add/', catalog.ProductCreate.as_view(), name='create'),
    path('products/generate-description/', catalog.generate_description, name='generate-description'),
    path('products/<int:pk>/', catalog.ProductDetail.as_view(), name='detail'),
    path('products/<int:pk>/edit/', catalog.ProductUpdate.as_view(), name='update'),
    path('products/<int:pk>/delete/', catalog.ProductDelete.as_view(), name='delete'),
    path('products/<int:pk>/photo/', catalog.product_photo, name='photo'),
    path('__insecure__/catalog-search/', views.catalog_search),
    path('__insecure__/price-report/', views.price_report),
    path('__insecure__/search-heading/', views.search_heading),
    path('__insecure__/promotion-preview/', views.promotion_preview),
    path('__insecure__/stock-notice/', views.stock_notice),
    path('__insecure__/supplier-probe/', views.supplier_probe),
    path('__insecure__/supplier-price/', views.supplier_price),
]

```
You will be ready for the `/security-review` command

**Do not change settings. Make changes only as part of this demo flow.**

## Session flow

### 1. Setting the scene (Slides 1–5)

- Security threats and vulnerability disclosures are increasing, while the time available to respond is shrinking.
- Introduce the GitHub Advanced Security pillars: **code security, code quality, supply chain security, and Copilot Autofix**.
- Explain why security must be integrated throughout the SDLC, not just when code reaches a pull request.
- Introduce GitHub's approach to securing every stage of agent-driven development.

### 2. Securing the agent loop (Slides 6–7)

- Explain how security checks are integrated into coding-agent workflows.
- Highlight code, dependency, and secret security checks.
- Demonstrate how agents identify and fix issues before code is committed.

### 3. Security in developer environments (Slides 8–9)

- Show how developers can request on-demand security reviews from the CLI.
- Highlight security findings alongside code in supported IDEs.
- Introduce the Copilot security extension and security canvas for reviewing, triaging, and fixing issues.

#### Demo CCA

Open the Copilot Cloud agent session for the issue that has already been assigned. Show the secret scanning and CodeQL scan results.

Learn more :
https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/security-governance-and-network-settings/risks-and-mitigations

Copilot cloud agent's security validation does not require a GitHub Secret Protection, GitHub Code Security, or GitHub Advanced Security license.
- CodeQL is used to identify code security issues.
- Newly introduced dependencies are checked against the GitHub Advisory Database for malware advisories, and for any CVSS-rated High or Critical vulnerabilities.
- Secret scanning is used to detect sensitive information such as API keys, tokens, and other secrets.

#### Demo `/secrurity-review` in the Copilot app

In the copilot app, with the code prepared, you can now run a security review by executing:

```text
/security-review
```

Display the security-review results in the Security canvas alongside the existing alerts. Select an alert and use **Explain** to discuss it or **Fix** to start remediation. Review any proposed change and its tests before presenting the alert as resolved.

https://github.blog/changelog/2026-07-14-security-reviews-now-available-in-the-github-copilot-app/
https://github.blog/changelog/2026-10-28-security-extension-for-the-github-copilot-app/

You can now run a security review on your in-flight code changes directly from the GitHub Copilot app. The /security-review slash command is bringing the same AI-driven vulnerability scanning already available in Copilot CLI into your everyday coding workflow.
You can now work through your repository’s GitHub code scanning alerts without leaving the GitHub Copilot app. The new GitHub security extension, now in public preview, lets you find the alerts that matter most and ask Copilot to explain or help fix them.
- High-confidence security findings, scored by severity and confidence.
- Actionable suggestions you can apply and reverify without leaving Copilot.
- A focused, prioritised view so you can fix the issues that matter before code lands.

### 4. AI-powered security scanning (Slides 10–11)

- Explain how **CodeQL and AI scanning complement each other** to identify vulnerabilities.
- Introduce standard AI scanning and deeper repository-level analysis.
- Demonstrate security scanning on pull requests and across repositories.
- Highlight AI application scanning for risks such as prompt injection, sensitive information disclosure, and excessive agency.
- If using the original delivery format, hand over to the guest presenter for the AI application scanning demonstration, then return for repository scanning.

### 5. Agentic Autofix (Slides 12–13)

- Explain the challenge of large vulnerability backlogs and manual remediation.
- Introduce Agentic Autofix for addressing multiple security alerts.
- Demonstrate selecting alerts and assigning remediation to Copilot.
- Show how the agent investigates findings, proposes fixes, runs validation, and creates a pull request.
- Highlight how Copilot memories can help improve future remediation.

#### Demo Agentic Autofix

Open the **Feature: Add extended view** pull request. Show the CodeQL findings in the Python code and the AI findings in the Terraform code.
https://github.blog/changelog/2026-07-14-code-scanning-shows-ai-security-detections-on-pull-requests/

 AI-powered security detections directly on pull requests, expanding vulnerability coverage to languages and frameworks not currently supported by CodeQL.

Then open **Security & quality → Code Scanning**. Show the CodeQL findings and the AI scan findings for the Terraform code.
https://github.blog/changelog/2026-10-28-ai-scan-for-repositories-in-public-preview/

You can now use AI Scan to find vulnerabilities across your whole repository, not just in pull request changes. It covers languages and frameworks that CodeQL doesn’t support and finds issues that rule-based analysis can miss in languages CodeQL already covers.
- An agentic code scanner explores your repository and focuses on the code most likely to contain vulnerabilities. Each scan runs within a fixed time budget, which keeps its cost bounded.
- When both AI Scan and CodeQL are scanning the same repository, AI Scan skips issues that CodeQL already reports.
- On rescans, AI Scan keeps existing findings open if it detects them again and only reports new findings.

To showcase Agentic Autofix, select three existing alerts and assign them to Copilot. Wait three seconds, go to the pull request, and show the Copilot session.
https://github.blog/changelog/2026-10-15-agentic-autofix-for-code-scanning-alerts-general-availability/

Agentic autofix remediates alerts by working across your codebase the way a developer would: it explores relevant files, proposes a fix, and reruns CodeQL to confirm the fix closes the alert before opening a pull request for your review.

if you have extra-time : 
Show the AI vulnerability in the PR named : "Formatting in prompt for product description generation"
https://github.blog/changelog/2026-10-28-code-scanning-for-ai-applications-in-public-preview/

### 6. Wrap-up (Slides 14–15)

- Reinforce that security is becoming integrated into every stage of development.
- Summarise how developers can access security through agents, IDEs, the CLI, pull requests, and repositories.
- Highlight the available configuration options and next steps for enabling the capabilities.

## Presenter checklist

- [ ] Review the slides and AI session summary.
- [ ] Confirm all required security features are available in the demo environment.
- [ ] Rehearse each demonstration and prepare fallback examples.
- [ ] Coordinate the guest presenter handoff, if applicable.
- [ ] Verify feature availability, product claims, and links on the closing slide.

**Key takeaway:** Agentic security brings detection and remediation closer to where developers work, helping teams build and ship software securely without slowing down development.