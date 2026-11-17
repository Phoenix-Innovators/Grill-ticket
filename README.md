# Grill Lab

Grill Lab helps the team turn unclear Jira tickets into clear requirements and useful build guidance.

- **Grill My Ticket:** asks clarifying questions and drafts acceptance criteria. A user with ticket edit access reviews and approves the criteria before they are shared.
- **Context Lab:** uses those approved criteria, team documents, and code to suggest next steps and ways to check the work.

**Current status:** planning documents are ready for team review. The app has not been built or tested.

## How we work

1. **Find or reuse a GitHub issue.** Check the [PRD](docs/prd.md#requirements) for the required behavior and the [MVP work packages](docs/mvp.md#work-packages) for where it fits. Create an issue if the work is uncovered.
2. **Confirm the outcome and owner.** Agree on dependencies and two or three observable completion checks. Use the [team roster](docs/team-areas.md) to find the right role.
3. **Plan and estimate the work.** The owner chooses the approach and writes the tasks. For a sub-issue, link it to its Epic in GitHub and estimate it separately. Use the [ticket standard](docs/mvp.md#owner-responsibilities-and-ticket-standard).
4. **Run the relevant checks and attach evidence.** Record the app version, observed results, and evidence link in the issue. Keep credentials and private source content out of evidence.
5. **Close the issue when the checks pass.** Finish any required review or merge, then update the docs if a decision or requirement changed. GitHub is where the team tracks work. Automation handles matching Jira records. [GitHub working guide](docs/Github-Jira-guide.md#everyday-workflow)

## Reference code legend

Use these codes to find the requirement, work package, decision, or check referenced in a GitHub issue.

| Code | Meaning | Where to look |
| --- | --- | --- |
| `FR01–FR10` | Functional requirements | [PRD requirements](docs/prd.md#requirements) |
| `B01–B10` | MVP work packages | [MVP work packages](docs/mvp.md#work-packages) |
| `D01–D07` | Implementation recommendations | [Build recommendations](docs/implementation-decisions.md) |
| `G01–G12` | Gaps and open decisions | [Gap review](docs/gap-review.md#what-is-covered-and-what-remains) |
| `J01–J10` | User journey checks | [Workflow checks](docs/acceptance-and-evidence.md#ten-workflow-checks) |
| `C01–C07` | Additional release checks | [Extra checks](docs/acceptance-and-evidence.md#seven-extra-checks) |

## Which doc should I use?

- **Product scope and priorities.** Start with the [PRD](docs/prd.md) for required behavior and the [MVP plan](docs/mvp.md) for build order. The Product Lead owns scope and acceptance. The Scrum Master coordinates dependencies and blockers.
- **Implementation and open decisions.** Check the relevant [build recommendation](docs/implementation-decisions.md) and [gap](docs/gap-review.md). Record the chosen approach and trade-offs in the GitHub issue.
- **Testing and release.** Use the [release checks](docs/acceptance-and-evidence.md) to plan evidence. The workflow checks, ten-ticket pilot, and model comparison are separate activities.

## First milestone

Start with **B01**. Prove the app can read a real ticket, Confluence page, and repository file, call AI, save and reload a result, and deny access to an unauthorized user. Backend leads the connection checks, the AI Lead checks AI behavior, and the storage assignee researches persistence. Use the results to agree on the shared interfaces in **B02**.
