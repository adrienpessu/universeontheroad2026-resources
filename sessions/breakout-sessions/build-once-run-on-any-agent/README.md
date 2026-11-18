# Delivery resources

Presenter and re-delivery materials for **Build once, run on any agent: A practical guide to agent skills**.

**Session format:** Approximately 35 minutes, including Q&A. The presentation includes two recorded demonstrations: **Proof Agent** and **DataForge**. Confirm the final timing and playback arrangements for your city.

## Core materials

| Item | Link | Purpose |
| --- | --- | --- |
| Presentation deck | [Slides — official Universe on the Road PowerPoint](https://microsofteur.sharepoint.com/:p:/t/UniverseontheRoad/cQorcuPyjO47Q72lf1qP1CgfEgUBBSX7m8yQYKaZa-qMsr36Vw) | Approved event deck to use for delivery |
| Speaker talking points | [Andrea's speaker notes and demo narration](https://gist.github.com/AndreaGriffiths11/6e479129bf5ca6ef3c66e7c6b7e6d71e) | Slide-by-slide prompts; full word-for-word narration for Proof Agent only |
| Original talk resources | [Talk resource page](https://gh.io/skills-talk) | Original speakers' deck, recordings and supporting resources |
| Proof Agent recording | [Narrated video (3:43)](https://github.com/githubevents/build-once-run-on-any-agent/blob/main/assets/recordings/proof-agent-narrated.mp4) | Andrea's prerecorded demo with voiceover |
| DataForge recording | [DataForge video](https://github.com/githubevents/build-once-run-on-any-agent/blob/main/assets/recordings/Dataforge.mp4) | Demo recording; no supplied voiceover script |
| Supporting article | [Build once, run on any agent — GitHub Blog](https://github.blog/ai-and-ml/github-copilot/build-once-run-on-any-agent-a-practical-guide-to-agent-skills/) | Additional context for both examples, particularly Shishir's DataForge section |
| Demo repository | [Original session repository](https://github.com/githubevents/build-once-run-on-any-agent) | Proof Agent and DataForge demo files and references |

> **IMPORTANT**
>
> There is no complete word-for-word script for the talk. Andrea's notes were written as short prompter bullets for GitHub Universe. The exception is her Proof Agent demonstration, which has an exact narration script in the talking-points Gist. Shishir did not supply a voiceover for DataForge; presenters must prepare their own explanation for that video.

## 1. Learn the presentation

1. Open the [official PowerPoint deck](https://microsofteur.sharepoint.com/:p:/t/UniverseontheRoad/cQorcuPyjO47Q72lf1qP1CgfEgUBBSX7m8yQYKaZa-qMsr36Vw) and read the [speaker talking points](https://gist.github.com/AndreaGriffiths11/6e479129bf5ca6ef3c66e7c6b7e6d71e) together. Convert the bullets into a natural talk track in your own words.
2. Review the [original resource page](https://gh.io/skills-talk) and watch both recorded demos so you understand what the audience will see.
3. Read the [supporting blog post](https://github.blog/ai-and-ml/github-copilot/build-once-run-on-any-agent-a-practical-guide-to-agent-skills/) before preparing Shishir's DataForge portion. It explains the four skills, the shared project manifest and human checkpoints.
4. Rehearse the talk with the videos and allow time for questions. Use the [breakout presenter overview](../README.md) for local event requirements.

## 2. Deliver the talk

Use the [speaker talking points](https://gist.github.com/AndreaGriffiths11/6e479129bf5ca6ef3c66e7c6b7e6d71e) as the primary guide for your narration. The talk follows this story:

- **Opening and problem:** Repeated prompts and undocumented engineering judgement create friction; agent skills capture repeatable instructions.
- **What is an agent skill?:** A versioned skill centred on `SKILL.md` describes when and how an agent should perform a task.
- **Proof Agent:** An independent verifier reviews the original request and changed files, then produces evidence-based PASS, FAIL or PARTIAL findings.
- **DataForge:** Four skills — `forge-init`, `forge-dbx`, `forge-lint` and `forge-builder` — coordinate pipeline development using shared project context and human approval checkpoints.
- **Portability and limitations:** Skills can be packaged for different agent clients, but models, tools, credentials and permissions still come from the host environment.
- **Closing:** Encourage attendees to start with one task they repeatedly explain, turn it into a skill and verify the result.

The talking-points Gist follows the original Universe slides. **Check slide references against the approved event PowerPoint**, as the delivery deck may differ from the original.

## 3. Prepare the demos

The source repository provides **recorded demo videos**, so live setup is not required unless your local event team chooses a different delivery approach.

1. **Proof Agent (Andrea Griffiths):** Use the [narrated recording](https://github.com/githubevents/build-once-run-on-any-agent/blob/main/assets/recordings/proof-agent-narrated.mp4) and the exact demo narration in the [Gist](https://gist.github.com/AndreaGriffiths11/6e479129bf5ca6ef3c66e7c6b7e6d71e). The demonstration shows independent, evidence-based review. Its GitHub Action example is advisory; it does not replace tests, security scanning or human review. **Play and test the recording with audio.**
2. **DataForge (Shishir Tewari, Procore):** Watch the [DataForge recording](https://github.com/githubevents/build-once-run-on-any-agent/blob/main/assets/recordings/Dataforge.mp4), read the [blog](https://github.blog/ai-and-ml/github-copilot/build-once-run-on-any-agent-a-practical-guide-to-agent-skills/) and prepare your own timed commentary. Explain how `forge-init` resolves project context, `forge-dbx` handles platform execution, `forge-lint` applies standards and `forge-builder` orchestrates the issue-to-pull-request workflow. **No supplied DataForge voiceover or word-for-word script is available.**

Confirm whether the approved deck embeds the videos or whether you need to play them separately. Check audio, offline access and the transition back into the slides. If presenting solo, credit Shishir and his Procore team for the DataForge example.

## Final checklist

- [ ] Official PowerPoint deck opened and slide sequence checked against the talking points.
- [ ] Speaker prompts reviewed and a natural talk track prepared.
- [ ] Proof Agent recording watched; its narration and audio playback tested.
- [ ] DataForge recording watched; own commentary prepared and rehearsed against the video.
- [ ] Supporting blog reviewed, especially the DataForge workflow and human checkpoints.
- [ ] Video playback method, offline copies and fallback agreed with the local AV team.
- [ ] Full session rehearsed within the allocated time, including Q&A.
- [ ] All resource links and local event requirements verified before delivery.

## Support

**Original presenters:** Andrea Griffiths (GitHub) and Shishir Tewari (Procore). The [session repository](https://github.com/githubevents/build-once-run-on-any-agent) contains the original materials. For local timing, room and AV questions, use the [breakout presenter overview](../README.md) and your event team.
