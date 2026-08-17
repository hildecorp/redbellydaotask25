<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/hildecorp/redbellydaotask25/main/website/dao-logo-on-dark.png">
    <img alt="Redbelly DAO logo" src="https://raw.githubusercontent.com/hildecorp/redbellydaotask25/main/website/dao-logo-on-light.png" width="280">
  </picture>
</p>

<h1 align="center">TASK-25: Proposal Evaluation Framework with Automated Pre-Screening</h1>

<p align="center">
  A Redbelly DAO Task Board submission. Turns the DAO's ratified 11-criterion Proposal Review Checklist into structured, constitution-cited pre-screening.
</p>

<p align="center">
  <a href="https://cdn.jsdelivr.net/gh/hildecorp/redbellydaotask25@main/website/TASK-25-Proposal-Evaluation-Rubric.pdf">PDF Report</a> ·
  <a href="https://docs.google.com/viewer?url=https://raw.githubusercontent.com/hildecorp/redbellydaotask25/main/website/TASK-25-Proposal-Evaluation-Rubric.docx&embedded=true">Word Doc</a>
</p>

<p align="center"><sub>Two links still need adding once confirmed: the live Vercel site, and the dev.to article once it is published. Add them to the row above as <code>· [Live Site](url) · [Article](url)</code>.</sub></p>

---

## What this is

Redbelly DAO ratified an 11-criterion Proposal Review Checklist on 6 October 2025 (Snapshot proposal #7), but it was applied by hand and inconsistently. TASK-25 asks for a pre-screening layer that runs a proposal against all 11 criteria and returns a pass or flag for each one, with the reason and the exact Constitution or Code of Conduct section it cites.

Reward: 18,830 RBNT, about 70 dollars, paid 100% in RBNT, winner-take-all.

Pre-screening is not a decision. It runs before Guild and High Council review, not instead of it. A flag means a reviewer should look closer, not that a proposal is rejected.

## Sources

Everything in this repo traces back to three ratified documents. No criterion, section, or flag condition is paraphrased from memory.

| Document | What it is | Link |
|---|---|---|
| Proposal Review Checklist | The 11 ratified criteria, Snapshot proposal #7, passed 6 Oct 2025 | [Snapshot](https://snapshot.box/#/s:rbnt.eth/proposal/0xf2a05384e37a710c1600db1abbac9b4dc66444a56a1ed49df7f0e3dbfd7570e7) |
| Constitution v1.2 | Ratified 20 Sep 2025 | [PDF](https://firebasestorage.googleapis.com/v0/b/redbelly-community-dao.firebasestorage.app/o/resources%2F1762476390856-Redbelly%20Community%20DAO%20Constitution%20v1.2%20-%20Ratified.pdf?alt=media&token=c89ccef9-cc7c-4a37-9b43-a3fac9e49ddc) |
| Code of Conduct v1.0 | Snapshot proposal #9, passed 6 Oct 2025, 92.97% For | [PDF](https://firebasestorage.googleapis.com/v0/b/redbelly-community-dao.firebasestorage.app/o/resources%2F1762476540292-Redbelly%20Community%20DAO%20Code%20of%20Conduct%20-%20Ratified.pdf?alt=media&token=84ca2c33-a502-4991-9720-4e6154847416) |

## The 11 criteria

| # | Criterion | Constitution anchor |
|---|---|---|
| 01 | Budget Alignment & Limits | Section 6.2 |
| 02 | Payment & Payout Structure | Section 7 |
| 03 | Strategic Fit | Section 3 |
| 04 | Feasibility & Timeline | No Constitution anchor |
| 05 | Oversight & Accountability | Section 6.1 |
| 06 | Impact & Measurement | No Constitution anchor |
| 07 | Risk & Mitigation | No Constitution anchor |
| 08 | Co-Funding & Leverage | No Constitution anchor |
| 09 | Contribution Equity | Section 5 |
| 10 | Compliance & Ethical Standards | Code of Conduct v1.0 |
| 11 | Community Involvement | Section 8 |

Full pass and flag conditions for each criterion are in the [rubric document](https://cdn.jsdelivr.net/gh/hildecorp/redbellydaotask25@main/website/TASK-25-Proposal-Evaluation-Rubric.pdf), not repeated here.

## Known discrepancies

Two places where the source documents disagree with each other. Both are surfaced, not silently resolved.

**Three working groups vs. five pods.** The ratified checklist text names three working groups: Community, Marketing, Developers/Builders. Constitution Section 3 ratifies five pods, adding Researcher and Partnerships. This framework follows the Constitution as the current, in-force structure. A Researcher or Partnerships submission is not flagged for its pod choice.

**Criterion 11 has no ratified flag condition.** Every other criterion pairs a pass condition with an explicit flag rule. Community Involvement does not. Any flag raised there is informational only and never marks a proposal as failing pre-screening on its own.

## Demo proposals

The rubric runs against one passed and one rejected proposal from the same campaign, the task's own suggested pair.

**#20, "Marketing Press Only, FINPR Agency."** Passed, March 2026. The original campaign.

**#26, "Continuation of Long-Term Marketing & PR Campaign with FINPR."** Rejected. Against 71.36%, Abstain 28.64%, For 0%. Voting ended 4 Jul 2026, 12:35 PM. Sought three more months continuing #20.

## Deliverables

- [x] Rubric document mapping all 11 criteria to pass/flag conditions and Constitution sections, PDF and Word
- [ ] Structured submission form
- [ ] Working pre-screening flow, runnable end to end
- [ ] Demo run against #20 and #26
- [ ] Documentation: how it works, how to update the mapping when the Constitution is amended, day-to-day non-technical operation

Confirm and check off the last four before submitting. This README reflects what is built as of the last update, not necessarily what is live now.

## Repo structure

```
website/
├── TASK-25-Proposal-Evaluation-Rubric.pdf
├── TASK-25-Proposal-Evaluation-Rubric.docx
├── dao-logo-on-dark.png
├── dao-logo-on-light.png
├── favicon-16.png
├── favicon-32.png
├── favicon-192.png
├── favicon-512.png
├── favicon.ico
├── filetype-pdf.svg
├── docs-svgrepo-com.svg
├── devto-ar21.svg
└── github.svg
```

## Site

- [Live Site](https://redbellydaotask25.vercel.app/)
- [PDF Report](https://cdn.jsdelivr.net/gh/hildecorp/redbellydaotask25@main/website/TASK-25-Proposal-Evaluation-Rubric.pdf)
- [Word Doc](https://docs.google.com/viewer?url=https://raw.githubusercontent.com/hildecorp/redbellydaotask25/main/website/TASK-25-Proposal-Evaluation-Rubric.docx&embedded=true)
- [Article](https://dev.to/hildecorp/from-ratified-checklist-to-working-tool-redbelly-daos-proposal-pre-screening-framework-3im4)

Deployed on Vercel. Dark theme, Kinetic Consensus design language from the Redbelly DAO Task Board brand kit: Be Vietnam Pro for headings and body, JetBrains Mono for machine-generated values, one accent color, #EF5350, no second accent anywhere.

Four sections: how pre-screening works, known discrepancies, the 11 criteria with clickable Constitution citations, and the full report embedded inline.

Copy follows the board's voice rules: plain hyphens, no em or en dashes, no emoji beyond the board's own check and cross glyphs, no filler verbs, exact numbers instead of "a few," answer before reasoning.
