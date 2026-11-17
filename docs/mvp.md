# Grill Lab MVP plan

Version 1 · November 4, 2026 · Team review

## The goal

Build both Grill My Ticket and Context Lab inside one Jira panel. The [PRD](prd.md) defines the required behavior. This plan explains the order of work.

**Current status:** no application code or verified integrations are in this repo. The supplied plan says the Jira–GitHub connection was restored; the app's own access still needs testing.

## Build in this order

1. **Prove the connections.** Read a real ticket, Confluence page, and repository file; call AI; save and reload the result. Confirm that a user without access cannot see it.
2. **Agree how the parts work together.** Frontend, Backend, the AI Lead, and the storage assignee agree what the screens, backend, AI, and saved records need from each other.
3. **Build the full journey.** Add context review, questions, editable criteria, approval, and build guidance. Frontend work can use clearly labeled sample data while connections are being proved.
4. **Test and release together.** Test failures and permissions throughout the build. Release both features after the real-source checks pass.

## Work packages

These are planning references. Owners create or reuse GitHub issues for the work, and automation creates matching records. Use the [team roster](team-areas.md) to find current role owners.

| ID | Outcome | Contributors | PRD |
| --- | --- | --- | --- |
| B01 | Prove real connections, AI, saving, and denied access. | Backend, AI Lead, storage assignee | FR01, FR09, FR10 |
| B02 | Agree what each part sends, receives, and saves. | Frontend, Backend, AI Lead, storage assignee | FR01–FR10 |
| B03 | Retrieve relevant permitted sources and show coverage. | Backend, AI Lead | FR01, FR02, FR07 |
| B04 | Deliver useful AI output within quality and spending limits. | AI Lead, Backend | FR03, FR04, FR06, FR10 |
| B05 | Build the short interview with saved progress. | Frontend, Backend | FR02, FR03, FR08 |
| B06 | Let ticket editors revise and explicitly approve criteria, and preserve version history. | Frontend, Backend, storage assignee | FR04, FR05, FR08 |
| B07 | Create guidance linked to criteria and sources. | Frontend, Backend, AI Lead | FR06, FR07 |
| B08 | Keep saved work private, current, recoverable, and removable. | Storage assignee, Backend | FR07, FR08, FR09 |
| B09 | Check access, evidence, errors, and accessibility. | Testing, Security, UX/UI, Scrum Master | FR01–FR10 |
| B10 | Review results, deploy, and finish the handoff. | DevOps, Product Lead, Documentation | FR01–FR10 |

## Owner responsibilities and ticket standard

Owners research their areas, choose approaches within scope, estimate effort, and record decisions and test results in their issues. One person is responsible for each issue; others can contribute. Roles can change, so issues name the owner and the role area; write "TBD" until someone is assigned, and update the issue when ownership changes.

- **Epic:** One product outcome, one accountable lead, and contributors across roles as needed. Record the high-level scope, dependencies, and overall acceptance checks. Link the child issues in GitHub.
- **Sub-issue:** One deliverable, one primary role, and one accountable owner. Additional assignees can collaborate. The owner writes the implementation tasks and gives the child its own story-point estimate during planning.

Each GitHub issue includes these fields.

- **Outcome:** the single deliverable it adds.
- **Ownership:** one accountable person and any contributing areas. For a sub-issue, also name the primary role.
- **Dependencies:** linked prerequisite issues or decisions, or "None."
- **PRD:** the requirement IDs and release checks that apply. See the [reference code legend](../README.md#reference-code-legend).
- **Done when:** two or three observable checks.

Link useful existing research. Create a separate investigation only when the uncertainty warrants one. When a decision changes PRD behavior, update the PRD first, then the affected issues and checks.

The Product Lead sets priorities and owns product acceptance. The Scrum Master coordinates dependencies and blockers and helps fill unassigned roles. Owners review decisions together when they affect cost, access, other roles, or product behavior.

## AI choices and spending

Start with one approved AI connection and configurable settings for questions, code analysis, and guidance. OpenRouter is the preferred starting option; a native Forge connection remains an alternative.

The research shortlist includes GPT 6 Luna, Gemini 3.6 Flash, and Claude Sonnet 4.6. These are candidates, not tested winners. The AI Lead compares quality, supported output, response time, data handling, and full-workflow cost before choosing a default.

**Don't forget you can use Shashi's app to check models and prices.**

Set spending limits and a budget owner before paid calls. No hidden paid fallback or automatic recharge. A timed-out call may still have cost money; do not automatically repeat it when the outcome is unknown.

## Recommended starting choices

Start with direct source connections and keep private context separate from approved criteria. The storage assignee researches and recommends an approach that supports access checks, approval history, safe retries, and conflicting-edit recovery.

Suggested starting limits are at most two automatic AI attempts, seven days for unfinished drafts, one day for completed private job data, and thirty days for private guides. These are proposals for the owners to confirm, not platform limits. An uncertain paid attempt must not be retried automatically.

See the [build recommendations](implementation-decisions.md) for the reasons and official references.

## Before release

Pass the [release checks](acceptance-and-evidence.md), complete ten representative pilot tickets with both features, and meet the PRD's four-of-five usefulness target. The proposed eighteen-case model comparison is a separate exercise.

Record the deployed version, sources and AI settings used, test results, limitations, and remaining decisions. Keep the PRD, issues, and release checks aligned.

Revision 1 · November 4, 2026: Simplified delivery plan; scope and package IDs retained.
