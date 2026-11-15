
# Delivery resources

Presenter and re-delivery materials for **Agentic security for every developer**.

Session format: Approximately 30 minutes

## Core materials

| Item | Link | Purpose |
| --- | --- | --- |
| Presentation deck | [Slides](https://microsofteur.sharepoint.com/:p:/t/UniverseontheRoad/cQrc9iPk2uWNS6I9y09nmgpKEgUBpRhpfHqC8WBcITqGsGPqmQ) | Presentation slides and speaker notes |
| Session recording | Not available | Use the deck, presenter guide, and demo notes |
| Presenter guide | [Presenter guide](speaker-resources/presenter-guide.md) | Talk track, slide flow, timing, and transitions |
| Demo repository | [Agentic security demo](https://github.com/octodemo/agentic-security-for-every-developer) | Demo resources and setup |
| Demo instructions | [Demo notes](https://github.com/octodemo/agentic-security-for-every-developer/blob/main/DEMO_NOTES.md) | Walkthrough and expected results |

## 1. Learn the presentation

1. Review the slides and speaker notes from start to finish.
2. Use the [presenter guide](speaker-resources/presenter-guide.md) to understand the key messages and transitions.
3. Rehearse the talk and demos together, keeping to the 15-minute slide and 25-minute demo allocation, please cut down the demo if time doesn't allow.

## 2. Deliver the talk

Follow the [presenter guide](speaker-resources/presenter-guide.md) for the slide-by-slide flow. The session covers:

- **Slides 1–5:** Security challenges, GitHub Advanced Security, and the agent-native development lifecycle.
- **Slides 6–7:** Security checks and automated fixes in the agent loop.
- **Slides 8–9:** Security reviews in the CLI, IDE, and Copilot App.
- **Slides 10–11:** CodeQL, AI Scan, and repository-wide and deep scanning.
- **Slides 12–13:** Agentic Autofix, memories, and bulk remediation.
- **Slides 14–16:** How to get started, closing, and feedback.

Transition into each demo at the marked **DEMO** slide. If using a guest presenter, coordinate the pull-request prompt-injection scanning handoff in the scanning section.

## 3. Reproduce the demos

Use the [demo repository](https://github.com/octodemo/agentic-security-for-every-developer) and follow its [demo notes](https://github.com/octodemo/agentic-security-for-every-developer/blob/main/DEMO_NOTES.md). The presentation calls for four demonstration sections:

1. **Agent loop security:** Show code, dependency, and secret checks during an agent task, including remediation before commit.
2. **Developer environment:** Run `/security-review` in the CLI and show security findings and fixes in the IDE and Copilot security extension.
3. **AI scanning:** Demonstrate pull-request scanning, the optional guest prompt-injection scanning demo, and standard and deep repository scans.
4. **Agentic Autofix:** Remediate identified alerts, review the proposed pull request, and highlight memories and bulk remediation.

Run the demos end-to-end before presenting. Verify required access, enabled features, expected results, and backup examples. Use completed scans or pull requests if a live demo fails.

## Final checklist

- [ ] Slides, speaker notes, and presenter guide reviewed.
- [ ] Talk and four demo sections rehearsed; timing confirmed.
- [ ] Demo setup, permissions, and required features verified.
- [ ] Guest handoff rehearsed, if applicable.
- [ ] Backup scans and pull requests prepared.
- [ ] Slide 12 screenshot, Slide 14 links, and feedback QR code checked.
- [ ] All resource links verified before delivery.

## Support

**Content owners:** April Yoho — [GitHub](https://github.com/scubaninja) and Adrien Pessu — [GitHub](https://github.com/adrienpessu).

