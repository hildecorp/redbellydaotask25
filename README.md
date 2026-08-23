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
  <a href="https://redbellydaotask25.vercel.app/">Live Site</a> ·
  <a href="https://cdn.jsdelivr.net/gh/hildecorp/redbellydaotask25@main/website/TASK-25Proposal-Evaluation-Rubric.pdf">PDF Report</a> ·
  <a href="https://docs.google.com/viewer?url=https://raw.githubusercontent.com/hildecorp/redbellydaotask25/main/website/TASK-25-Proposal-Evaluation-Rubric.docx&embedded=true">Word Doc</a> ·
  <a href="https://dev.to/hildecorp/from-ratified-checklist-to-working-tool-redbelly-daos-proposal-pre-screening-framework-3im4">Article</a>
</p>

---

## What this is

Redbelly DAO ratified an 11-criterion Proposal Review Checklist on 6 October 2025 (Snapshot proposal #7), but it was applied by hand and inconsistently. TASK-25 asks for a pre-screening layer that runs a proposal against all 11 criteria and returns a pass or flag for each one, with the reason and the exact Constitution or Code of Conduct section it cites.

Reward: 18,830 RBNT, about 70 dollars, paid 100% in RBNT, winner-take-all.

Pre-screening is not a decision. It runs before Guild and High Council review, not instead of it. A flag means a reviewer should look closer, not that a proposal is rejected.

## Sources

Everything in this repo traces back to four ratified documents. No criterion, section, or flag condition is paraphrased from memory.

| Document | What it is | Link |
|---|---|---|
| Proposal Review Checklist | The 11 ratified criteria, Snapshot proposal #7, passed 6 Oct 2025 | [Snapshot](https://snapshot.box/#/s:rbnt.eth/proposal/0xf2a05384e37a710c1600db1abbac9b4dc66444a56a1ed49df7f0e3dbfd7570e7) |
| Constitution v1.3 | Current. Supersedes v1.2 (ratified 20 Sep 2025) | [PDF](https://cdn.jsdelivr.net/gh/hildecorp/redbellydaotask25@main/website/constitutionv1.3.pdf) |
| DAO Guild Structure Consolidation | Merged 2 of the DAO's 5 pods into the other 3, passed 20 Sep 2025 | [Snapshot](https://snapshot.box/#/s:rbnt.eth/proposal/0x901e2873e7907d2ee87de5a79beae4fd602e75d053cd9fc6489e97d2547dd039) |
| Code of Conduct v1.0 | Snapshot proposal #9, passed 6 Oct 2025, 92.97% For | [PDF](https://firebasestorage.googleapis.com/v0/b/redbelly-community-dao.firebasestorage.app/o/resources%2F1762476540292-Redbelly%20Community%20DAO%20Code%20of%20Conduct%20-%20Ratified.pdf?alt=media&token=84ca2c33-a502-4991-9720-4e6154847416) |

## The 11 criteria

| # | Criterion | Constitution anchor |
|---|---|---|
| 01 | Budget Alignment & Limits | Section 5.7 |
| 02 | Payment & Payout Structure | Section 6 |
| 03 | Strategic Fit | No Constitution anchor |
| 04 | Feasibility & Timeline | No Constitution anchor |
| 05 | Oversight & Accountability | Section 5.6 |
| 06 | Impact & Measurement | No Constitution anchor |
| 07 | Risk & Mitigation | No Constitution anchor |
| 08 | Co-Funding & Leverage | No Constitution anchor |
| 09 | Contribution Equity | Section 4 |
| 10 | Compliance & Ethical Standards | Code of Conduct v1.0 |
| 11 | Community Involvement | Section 7 |

Full pass and flag conditions for each criterion are in the [rubric document](https://cdn.jsdelivr.net/gh/hildecorp/redbellydaotask25@main/website/TASK-25Proposal-Evaluation-Rubric.pdf), not repeated here.

## Known discrepancies

Two places where the ratified text does not resolve itself. Both are surfaced, not silently resolved.

**Three working groups, five pods, then none.** The ratified checklist names three working groups: Community, Marketing, Developers/Builders. Constitution v1.2 ratified five pods for this: Marketing, Builder/Develop, Researcher, Community, Partnerships. The DAO Guild Structure Consolidation vote, passed 20 September 2025, merged 2 of those 5 into the other 3, leaving the same three the checklist names. Constitution v1.3 then removed the pod structure section outright. No section defines working groups or pods anymore. Pre-screening still checks alignment against the three named groups, since that is the ratified checklist text; it just has no Constitution section left to cite. A flag on Strategic Fit is the expected outcome for any submission today, not a sign of a broken tool.

**Criterion 11 has no ratified flag condition.** Every other criterion pairs a pass condition with an explicit flag rule. Community Involvement does not. Any flag raised there is informational only and never marks a proposal as failing pre-screening on its own.

## Working pre-screening flow

Section 05 of the live site holds the submission form and the pre-screening engine. It covers all 11 criteria, runs entirely client-side, and sends no data anywhere. Two buttons load real proposals from the archive so the flow can be demonstrated without typing anything in by hand:

- Load Proposal #26, rejected, fills the form from the real "Continuation of Long-Term Marketing and PR Campaign with FINPR" submission.
- Load Proposal #20, passed, fills the form from the real "Marketing Press Only: FINPR Agency" submission.

Clicking Run Pre-Screening produces a pass or flag for each of the 11 criteria, a one-line reason on every flag, and the same Constitution or Code of Conduct citation used in Section 03. Reasons are substance checks: missing fields, amounts over a ratified cap, a group outside the ratified list, never a word count. Criteria 08 and 11 are always labelled informational and never contribute to a fail state. A summary line reads "X of 11 passed." The tool never issues an overall accept or reject verdict, that stays with the council.

## Demo proposals

The rubric runs against one passed and one rejected proposal from the same campaign, the task's own suggested pair.

**#20, "Marketing Press Only, FINPR Agency."** Passed 85.42% For, 6mo ago. USDT 2,890 to FINPR, 50,000 RBNT to Rainbowmagician for coordination and research. Upfront-weighted payment, 70 percent on booking. Loads into Section 05 as a worked example.

**#26, "Continuation of Long-Term Marketing & PR Campaign with FINPR."** Rejected, Against 71.36%, Abstain 28.64%, For 0%. Voting ended 4 Jul 2026, 12:35 PM. Sought three more months continuing #20. Loads into Section 05 as a worked example.

## Documentation

Section 06 of the live site covers three things a council member needs: how the pre-screening flow works, which proposals have already superseded Constitution text without a full re-ratification, and how to run a pre-screening check day to day with no technical background required.

## Deliverables

- [x] Rubric document mapping all 11 criteria to pass/flag conditions and Constitution sections, PDF and Word
- [x] Structured submission form, Section 05 of the live site
- [x] Working pre-screening flow, runnable end to end, client-side, no external calls
- [x] Demo run against #20 and #26, both loadable and runnable from the live site
- [x] Documentation: how it works, what already supersedes prior text, day-to-day non-technical operation, Section 06 of the live site

## Repo structure
```website/
├── TASK-25-Proposal-Evaluation-Rubric.pdf
├── TASK-25-Proposal-Evaluation-Rubric.docx
├── constitutionv1.3.pdf
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

Deployed on Vercel. Dark theme, Kinetic Consensus design language from the Redbelly DAO Task Board brand kit: Be Vietnam Pro for headings and body, JetBrains Mono for machine-generated values, one accent color, #EF5350, no second accent anywhere.

Six sections: how pre-screening works, known discrepancies, the 11 criteria with clickable Constitution citations, the full report embedded inline, the submission form and pre-screening engine, and documentation.

Copy follows the board's voice rules: plain hyphens, no em or en dashes, no emoji beyond the board's own check and cross glyphs, no filler verbs, exact numbers instead of "a few," answer before reasoning.
