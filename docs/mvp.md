# Grill Lab MVP plan

Version 1 · November 4, 2026 · Team review

## The goal

Build both Grill My Ticket and Context Lab inside one Jira panel. The [PRD](prd.md) defines the required behavior. This plan explains the order of work.

**Current status:** no application code or verified integrations are in this repo. The supplied plan says the Jira–GitHub connection was restored; the app's own access still needs testing.

## Build in this order

1. **Prove the connections.** Read a real ticket, Confluence page, and repository file; call AI; save and reload the result. Confirm that a user without access cannot see it.
2. **Agree how the parts work together.** Kandis, Michael, and Alan agree what the screens, backend, AI, and saved records need from each other.
3. **Build the full journey.** Add context review, questions, editable criteria, approval, and build guidance. Frontend work can use clearly labeled sample data while connections are being proved.
4. **Test and release together.** Test failures and permissions throughout the build. Release both features after the real-source checks pass.

## Work packages

These are planning references, not Jira issues already created. Owners split them into smaller issues.

| ID | Outcome | Contributors | PRD |
| --- | --- | --- | --- |
| B01 | Prove real connections, AI, saving, and denied access. | Alan, Michael; Kandis checks AI | FR01, FR09, FR10 |
| B02 | Agree what each part sends, receives, and saves. | Kandis, Michael, Alan | FR01–FR10 |
| B03 | Retrieve relevant permitted sources and show coverage. | Michael; Kandis helps select evidence | FR01, FR02, FR07 |
| B04 | Deliver useful AI output within quality and spending limits. | Kandis, Michael | FR03, FR04, FR06, FR10 |
| B05 | Build the short interview with saved progress. | Kandis, Michael | FR02, FR03, FR08 |
| B06 | Edit, approve, and safely save criteria. | Kandis, Michael, Alan | FR04, FR05, FR08 |
| B07 | Create guidance linked to criteria and sources. | Kandis, Michael | FR06, FR07 |
| B08 | Keep saved work private, current, recoverable, and removable. | Alan, Michael | FR07, FR08, FR09 |
| B09 | Check access, evidence, errors, and accessibility. | Testing, Security, UI/UX owners TBD; Brie coordinates | FR01–FR10 |
| B10 | Review results, deploy, and finish the handoff. | Alan deploys; Brie leads acceptance; Documentation TBD | FR01–FR10 |

## Owner responsibilities and ticket standard

Owners research their areas, choose approaches within scope, estimate effort, and record decisions and test results in their issues. One person is responsible for each issue; others can contribute.

Each issue needs an outcome, owner, PRD requirement, scope, dependencies, and two or three observable checks. Link useful existing research. Create a separate investigation only when the uncertainty warrants one.

Brie sets priorities, coordinates blockers, and helps fill unassigned roles. Owners review decisions together when they affect cost, access, other roles, or product behavior.

## AI choices and spending

Start with one approved AI connection and configurable settings for questions, code analysis, and guidance. OpenRouter is the preferred starting option; a native Forge connection remains an alternative.

The research shortlist includes GPT 6 Luna, Gemini 3.6 Flash, and Claude Sonnet 4.6. These are candidates, not tested winners. Kandis compares quality, supported output, response time, data handling, and full-workflow cost before choosing a default.

**Don't forget you can use Shashi's app to check models and prices.**

Set spending limits and a budget owner before paid calls. No hidden paid fallback or automatic recharge. A timed-out call may still have cost money; do not automatically repeat it when the outcome is unknown.

## Recommended starting choices

Use direct source connections first, keep private context separate from shared criteria, and leave the optional Jira-property copy off initially. Use saving rules that prevent conflicting edits and duplicate operations. Owners can choose alternatives that meet the same requirements.

Suggested starting limits are at most two automatic AI attempts, seven days for unfinished drafts, one day for completed private job data, and thirty days for private guides. These are proposals for the owners to confirm, not platform limits. An uncertain paid attempt must not be retried automatically.

See the [build recommendations](implementation-decisions.md) for the reasons and official references.

## Before release

Pass the [release checks](acceptance-and-evidence.md), complete ten representative pilot tickets with both features, and meet the PRD's four-of-five usefulness target. The proposed eighteen-case model comparison is a separate exercise.

Record the deployed version, sources and AI settings used, test results, limitations, and remaining decisions. Keep the PRD, issues, and release checks aligned.

Revision 1 · November 4, 2026: Simplified delivery plan; scope and package IDs retained.
