# Grill Lab remaining gaps

Reviewed November 4, 2026 · PRD and MVP remain v1

## High-level result

The team has a clear product plan and recommended answers to the main build questions. Three parallel research reviews, a second challenge pass, and a final review helped remove weak assumptions.

**The app is not built or tested yet.** Research has clarified the approach; real connections, team decisions, and passing tests are still needed.

## What is covered and what remains

| Gap | Recommended answer | Still needed |
| --- | --- | --- |
| G01 · Connections | Start with direct Jira, Confluence, and repository access. | Prove real reads, AI, saving, and reload on the selected site. |
| G02 · Repository permissions | Tie read-only access to each user and the selected repository. | Prove sign-in, renewed access, disconnect, and denied access. |
| G03 · AI data sharing | Use one approved route; keep graph/MCP out of the first external route. | Confirm permitted data, provider settings, prices, and budget. |
| G04 · Shared criteria privacy | Separate private context from information approved for sharing. Leave the optional Jira-property copy off. | Agree publication policy and test for leaks. |
| G05 · Safe saving | Protect competing edits and make repeated submissions return the same result. | Prove races, old retries, and deletion cannot corrupt approvals. |
| G06 · Spending | Reserve cost before calls and do not automatically retry uncertain paid outcomes. | Set limits and a budget owner; test concurrent calls and refunds. |
| G07 · Missing information | Show gaps and partial guidance; never invent context. | Build and test the missing-source states. |
| G08 · Outdated guidance | Check access and source changes separately. | Test changed code/docs, failed checks, and revoked access. |
| G09 · Quality | Use fixed examples, human evidence review, and the ten-ticket pilot. | Run the comparison and pilot; measure cost and response time. |
| G10 · Ownership | Each issue has one responsible owner and can have collaborators. | Fill TBD roles, estimate work, and agree dates. |
| G11 · Deletion | Hide expired work and stop late jobs restoring deleted content. | Confirm retention and prove cleanup behavior. |
| G12 · Accessibility | Review the full journey with keyboard and screen reader. | Complete the usability and accessibility checks. |

These are recommended approaches, not claims that the gaps have passed testing. Owners keep their research and decisions with the relevant issues.

## Important lessons from the review

- SQL is not the only storage option. Forge's conditional saving can be a simpler starting point.
- A connected GitHub account does not prove the app can read files for the current user.
- A timeout does not prove an AI call was free or stopped.
- Approving text does not automatically make private facts safe to share.
- A working link does not prove a claim is supported.
- A partial guide is useful, but cannot count as the complete release workflow.

The [build recommendations](implementation-decisions.md) explain these choices and link to official sources. The [release checks](acceptance-and-evidence.md) explain how to prove them.

## What happens next

Alan and Michael prove the connections and saving; Kandis checks AI behavior and compares models. Together they agree how the parts fit. Brie coordinates priorities, shared decisions, and unassigned roles. Owners then build and test both features.

The team must supply actual source selections, access, data-sharing rules, spending limits, retention choices, role coverage, estimates, and release date. Confirm each before the work that depends on it.

**Don't forget you can use Shashi's app to check models and prices.** Its link/access was not supplied, and no winning model was selected in this review.

No Jira issues, deployments, external messages, or paid AI calls were created by this research.
