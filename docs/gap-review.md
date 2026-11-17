# Grill Lab remaining gaps

Reviewed November 4, 2026 · PRD and MVP remain v1

## High-level result

The team has a clear product plan and recommended answers to the main build questions. Three parallel research reviews, a second challenge pass, and a final review helped remove weak assumptions.

**The app is not built or tested yet.** Research has clarified the approach; real connections, team decisions, and passing tests are still needed.

## What is covered and what remains

**Decided** means the product rule or team practice is agreed and still needs the follow-up shown. **Open** means a design or planning decision remains. Owners record decisions and test evidence in the relevant GitHub issue.

| Gap | Status | Current direction | Still needed |
| --- | --- | --- | --- |
| G01 · Connections | Open | Start with direct Jira, Confluence, and repository access. | Confirm pilot sources and prove real reads, AI, saving, and reload. |
| G02 · Repository permissions | Open | Tie read-only access to each user and the selected repository. | Confirm the sign-in approach and prove renewal, disconnect, and denied access. |
| G03 · AI data sharing | Open | Start with one approved route. Keep graph/MCP out of the first external route. | Confirm permitted data, provider settings, prices, and budget. |
| G04 · Shared criteria privacy | Decided | Keep answers and drafts private. Let ticket editors approve criteria for ticket viewers. | Test preview, approval permissions, and visibility. |
| G05 · Safe saving | Open | The PRD requires conflict protection and safe retries. | The storage assignee researches the design and tests concurrent saves, old retries, and deletion. |
| G06 · Spending | Open | Reserve cost before calls and avoid automatic retries with uncertain paid outcomes. | Set limits and a budget owner, then test concurrent calls and refunds. |
| G07 · Missing information | Decided | Show gaps and partial guidance. Use available evidence for factual claims. | Build and test missing-source states. |
| G08 · Outdated guidance | Decided | Flag changed criteria or sources, show unknown freshness when needed, and recheck access. | Test changed code or documents, failed checks, and revoked access. |
| G09 · Quality | Open | The PRD requires a ten-ticket pilot. Fixed model examples and human evidence review are proposed for evaluation. | Confirm the comparison cases and run the comparison and pilot. Measure cost and response time. |
| G10 · Ownership | Decided | Each issue has one accountable owner and can have collaborators. | Fill TBD roles, estimate work, and agree dates. |
| G11 · Deletion | Open | Hide expired work and stop late jobs from restoring deleted content. | Confirm retention and prove cleanup behavior. |
| G12 · Accessibility | Decided | The full journey must work with keyboard and screen reader. | Complete the usability and accessibility checks. |

## Important lessons from the review

- The storage assignee will compare viable options against the approval and recovery requirements.
- A connected GitHub account does not prove the app can read files for the current user.
- A timeout does not prove an AI call was free or stopped.
- Approving text does not automatically make private facts safe to share.
- A working link does not prove a claim is supported.
- A partial guide is useful, but cannot count as the complete release workflow.

The [build recommendations](implementation-decisions.md) explain these choices and link to official sources. The [release checks](acceptance-and-evidence.md) explain how to prove them.

## What happens next

Backend proves the connections, the storage assignee researches persistence, and the AI Lead checks AI behavior and compares models. Frontend helps agree the contracts. The Product Lead sets priorities, and the Scrum Master coordinates shared decisions and unassigned roles. Owners then build and test both features.

The team must supply actual source selections, access, data-sharing rules, spending limits, retention choices, role coverage, estimates, and release date. Confirm each before the work that depends on it.

**Don't forget you can use Shashi's app to check models and prices.** Its link/access was not supplied, and no winning model was selected in this review.
