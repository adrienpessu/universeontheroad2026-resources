# Speaker Guide: Agentic Security for Every Developer

## Session overview

This session introduces GitHub's approach to agentic security, demonstrating how GitHub Advanced Security and Copilot help developers prevent, detect, and remediate vulnerabilities throughout the agent-native software development lifecycle.

**Core message:** Security must keep pace with AI-driven development. GitHub is embedding security directly into developer and agent workflows, helping teams identify and fix vulnerabilities earlier, secure AI-generated code, and remediate security backlogs at scale.

### Before you present

- Review the presentation deck and accompanying speaker notes.
- Review the [demo repository and instructions](https://github.com/octodemo/agentic-security-for-every-developer/blob/main/DEMO_NOTES.md).
- Familiarise yourself with GitHub Advanced Security, CodeQL, AI Scan, Deep Scans, Copilot security reviews, and Agentic Autofix.
- Confirm access to all required demo environments and enabled features.
- Prepare completed scans, security findings, and remediation pull requests as backups.
- Rehearse the guest presenter handoff if delivering with a second presenter.
- Verify product availability, statistics, and links before presenting.

**Session timing:** Approximately 40 minutes — 15 minutes of slides and 25 minutes of demonstrations, including one guest demo.

## Session flow

### 1. Setting the scene (Slides 1–5)

- Introduce GitHub's mission to secure the agent-native engineering system, where humans and AI agents build software together.
- Explain the growing security challenge: vulnerability disclosures continue to increase while automated attacks significantly reduce the time between discovery and exploitation.
- Introduce GitHub Advanced Security and its four core pillars:
  - **Code Security:** Identify vulnerabilities across repositories and pull requests.
  - **Code Quality:** Improve code quality through automated checks and coverage.
  - **Supply Chain Security:** Detect and prevent vulnerable dependencies.
  - **Copilot Autofix:** Accelerate vulnerability remediation.
- Explain why security cannot wait until code reaches a pull request.
- Introduce GitHub's approach to embedding security throughout the development lifecycle: agent loop, CLI, IDE, Copilot App, pull requests, repositories, and enterprise remediation.

**Key message:** Security must adapt its speed and depth to every stage of development, preventing vulnerabilities before they reach production.

### 2. Securing the agent loop (Slides 6–7)

- Explain how security checks are integrated directly into AI coding-agent workflows.
- Highlight automatic code, dependency, and secret security checks for supported agents.
- Explain how CodeQL identifies vulnerabilities, dependency checks identify known risks, and secret scanning detects exposed credentials.
- Demonstrate how agents detect and resolve security issues before committing code.
- Highlight that Copilot cloud agent security validation is enabled without requiring a separate GitHub Advanced Security license.

**Demo — Agent loop security checks**

- Show the security validation performed during an agent-driven coding task.
- Highlight detected issues and how the agent addresses them.
- Demonstrate the resulting code changes and security validation.

### 3. Security in developer environments (Slides 8–9)

- Introduce proactive security reviews directly within developers' existing tools.
- Demonstrate how developers can request on-demand security reviews using `/security-review` in the CLI.
- Highlight side-by-side security findings and code in supported IDEs.
- Introduce the Copilot security extension and security canvas for interactive scanning, triaging, and remediation.
- Explain how these capabilities bring security expertise closer to developers without requiring them to switch tools.

**Demo — CLI, IDE, and Copilot Security Extension**

- Run an on-demand security review from the CLI.
- Show security findings within the IDE.
- Demonstrate interactive investigation and remediation using the Copilot security extension.

### 4. AI-powered security scanning (Slides 10–11)

- Explain how **CodeQL and AI Scan complement one another** to identify vulnerabilities.
- Introduce hybrid scanning for pull requests, combining deterministic analysis with AI-powered detection.
- Explain how AI Scan extends coverage to additional languages, frameworks, and vulnerabilities that traditional analysis might miss.
- Highlight repository-wide AI scanning and the ability to perform deeper analysis of critical areas.
- Explain how findings are maintained across rescans and how AI Scan avoids duplicating issues already identified by CodeQL.
- Introduce AI application security risks, including cross-prompt-injection attacks.

**Demo — Pull request and repository scanning**

- Demonstrate AI scanning within a pull request.
- Show how AI-generated findings complement CodeQL results.
- If following the original delivery format, hand over to the guest presenter for the **PR XPIA scanning demonstration**, then return to the main presenter.
- Demonstrate standard repository-wide AI scanning.
- Show how Deep Scans provide more targeted analysis of critical code.

### 5. Agentic Autofix (Slides 12–13)

- Explain the challenge of large vulnerability backlogs and the limited number of findings traditionally remediated.
- Introduce Agentic Autofix as a way to accelerate remediation across repositories.
- Highlight the improved remediation rates presented in the deck.
- Explain how Agentic Autofix investigates vulnerabilities, proposes code changes, and validates fixes before creating pull requests.
- Introduce bulk remediation and the use of Copilot memories to provide context for subsequent remediation tasks.

**Demo — Agentic Autofix and bulk remediation**

- Use vulnerabilities identified during the previous scanning demonstrations.
- Select security alerts and initiate remediation using Agentic Autofix.
- Show how the agent investigates relevant code, proposes fixes, and validates the changes.
- Demonstrate the resulting remediation pull request.
- Highlight Copilot memories and bulk remediation capabilities.

**Key message:** Security agents can help teams move beyond identifying vulnerabilities to actively reducing security backlogs, while keeping developers involved in reviewing and approving changes.

### 6. Wrap-up and next steps (Slides 14–16)

- Reinforce that GitHub is integrating security across the entire agent-native development lifecycle.
- Summarise how attendees can access or enable the capabilities:
  - **Agent Loop:** Security validation enabled by default for Copilot cloud agent jobs.
  - **CLI & IDE:** Trigger a security review using `/security-review`.
  - **PRs & Repositories:** Enable AI Scan in repository Advanced Security settings.
  - **Deep Scans:** Request access using the link on the closing slide.
  - **Copilot App:** Install the Copilot security extension.
  - **Agentic Autofix:** Enable the capability through enterprise settings.
- Encourage attendees to start by enabling security checks in their existing development workflows.
- Thank attendees and direct them to the session feedback QR code.

## Presenter checklist

- [ ] Review the presentation deck and embedded speaker notes.
- [ ] Review the demo repository and rehearse all four demonstration sections.
- [ ] Verify that the required security features, licenses, and permissions are available.
- [ ] Prepare backup scan results, security alerts, and completed remediation pull requests.
- [ ] Confirm the Copilot security extension and CLI security review work as expected.
- [ ] Coordinate and rehearse the guest presenter handoff, if applicable.
- [ ] Verify statistics, product claims, and feature availability.
- [ ] Confirm all links and calls to action on Slide 14 are working.
- [ ] Check the final Agentic Autofix screenshot on Slide 12.
- [ ] Confirm the feedback QR code is appropriate for the event.

**Key takeaway:** Agentic security brings prevention, detection, and remediation directly into the tools and workflows developers already use. By securing agent-generated code, extending security analysis across the development lifecycle, and automating remediation, GitHub helps teams ship software faster and more securely.