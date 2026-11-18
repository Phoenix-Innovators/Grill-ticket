# Grill Lab product requirements

November 18, 2026

## What we’re building

Grill Lab is one Jira assistant that helps people work through a ticket from beginning to end. It helps users understand the work, find missing details, make better decisions, and move toward completion without searching through endless documentation.

Grill Lab should assess the user’s plan and raise useful concerns, explain its reasoning, suggest alternatives, and leave the user in control.

Grill Lab has two connected functions:

- Grill My Ticket helps the user clarify what needs to be done. It reviews relevant information, asks purposeful questions, spots gaps or related work, and helps draft clear acceptance criteria (the checks used to determine whether a ticket is done).
- Context Lab helps the user figure out how to do the work. It offers practical guidance, explanations, troubleshooting, examples, and proposed code, with links to the information it relied on.

Users can open either function whenever they need it, in any order. Both share relevant ticket context and saved decisions, subject to access controls.

## How a user works with Grill Lab

1. Open a Jira ticket and launch Grill Lab from its issue panel.
2. Choose Grill My Ticket or Context Lab. A two-tab panel is the proposed layout. Frontend and UX/UI will refine it.
3. Click to start a review or request help. Grill Lab reads the relevant sources the user is authorized to access.
4. Review the AI's questions, concerns, suggestions, or next steps. The user can ask follow-up questions, change direction, skip, or request more detail.
5. When useful, generate or revise acceptance criteria. An authorized user reviews and approves the exact wording before it becomes shared.
6. Return later and resume work without having to restart. The user can request a fresh review if things have changed.

Context Lab is available even when acceptance criteria are unfinished or not yet approved. It should explain how incomplete information affects confidence in its guidance.

## How the AI should behave

- Challenge respectfully. Point out a likely problem, duplicate, dependency, or stronger alternative. Explain why it matters and let the user decide.
- Ask only useful questions. Ask one at a time when clarification helps. Do not force a five-question limit or ask questions just to continue a script.
- Focus on clarity and progress. Consider the ticket's goal, intended behavior, dependencies, constraints, and definition of done. Show what is clear and what still needs attention without requiring a perfect score or exhaustive checklist.
- Keep conversations flexible. Allow quick reviews or deeper discussion. Users can skip, revisit, pause, resume, and draft criteria at any point. Skipping does not count as answering.
- Know when to stop asking. Offer a useful next step or draft when sufficient information exists, and let the user end the review at any time.
- Separate facts from ideas. Cite real, permitted sources for claims about existing code, documentation, and related tickets. Make assumptions, incomplete coverage, and recommendations visible.
- Make guidance easy to use. Prefer concise steps and relevant examples over lengthy documentation dumps. Frontend and UX/UI will decide the final result presentation.
- Keep the user in control. AI cannot approve shared requirements or make changes to shared work without appropriate authorization and explicit approval.

## What the first release includes

- A Grill Lab panel within a Jira issue, with both functions accessible on demand and able to share authorized context.
- User-triggered AI reviews. Opening the panel can display saved work and check availability, but does not automatically launch a new AI analysis.
- Review of the current ticket, relevant Jira work, agreed Confluence content, and selected official Forge guidance. Use relevant development information from tools already connected to Jira where permitted. Support source-file review when authorized access is proven.
- Flexible ticket clarification, editable acceptance criteria, explicit approval, and readable approval history.
- Context Lab explanations, implementation steps, troubleshooting help, and proposed code or examples, even if criteria have not been approved.
- Saved progress, clear errors, and visible warnings when source access or freshness changes.

Work with existing connections first. Grill Lab should fit the tools the team already uses, such as GitHub, GitLab, or Bitbucket. Reuse existing access where it is sufficient. Jira and Confluence permissions remain in force, and source-file access must also respect the repository provider’s permissions. A Jira development link may expose branches, commits, or pull requests. Verify access to the underlying code separately. If source-file access is unavailable, explain the limitation and require explicit authorization for any broader access. The first release must prove a usable, authorized way to access development context. Provider-specific coverage remains open for engineering research.

## Requirements

| ID | Grill Lab must… |
| --- | --- |
| FR01 | Reuse existing Jira, Confluence, and connected development context where authorized. Respect the current user’s permissions and any required app or provider authorization. Show which sources were checked, unavailable, or incomplete. Avoid unnecessary reconnection. |
| FR02 | Use relevant ticket, documentation, and code information to identify meaningful gaps, conflicts, and related work. Distinguish verified facts from suggestions. |
| FR03 | Support flexible, user-triggered conversation without a fixed five-question limit. Allow skipping, revisiting, pausing, resuming, and drafting at any point. Keep individual AI operations within safe usage limits. |
| FR04 | Let users add, edit, and remove clear, testable acceptance criteria, while keeping assumptions and unresolved decisions separate. |
| FR05 | Require explicit permission-based approval before criteria are shared. Preserve exact approved versions, prevent duplicate saves, and warn about conflicting edits. |
| FR06 | Provide useful Context Lab guidance with or without approved criteria. Offer practical next steps and relevant source references, and label uncertainty. |
| FR07 | Show when saved guidance may be outdated because related requirements or sources changed, or when freshness cannot be verified. Let users request an updated review. |
| FR08 | Save and restore relevant progress across visits, handle failed operations clearly, and protect the last good approval. The technical team selects the storage approach. |
| FR09 | Keep unapproved drafts, conversations, and restricted source content private. Share approved criteria only with users allowed to view the ticket. Recheck access before showing saved work. |
| FR10 | Control AI access, output validation, costs, and sensitive actions on the backend. AI cannot approve its own output or perform unapproved changes. |

## What comes later

Automatic monitoring of ticket creation, updates, closures, pull requests, or merges belongs in the backlog. In the first release, users request reviews from the panel.

Deferred work also includes building additional direct integrations for every repository host, automatic Jira description changes, autonomous issue creation, exhaustive scanning of connected services, and direct AI editing or execution of repository code. Hands-off implementation remains part of the broader vision.

## What success looks like

- A new teammate can explain the product and open either function without a technical walkthrough.
- Both functions are useful individually and work together without forcing an order.
- Users can recognize clear requirements, remaining questions, and worthwhile next steps without being forced through a lengthy interview.
- Acceptance criteria are editable, explicitly approved, saved without duplication, and recoverable with their versions.
- Claims about existing work have real supporting sources. Gaps and uncertainty are visible.
- Representative tests cover each function, their combined use, accessibility, permissions, failure/recovery, and measured AI responsiveness and spending.

The MVP plan and release checks track the pilot scenarios and thresholds for these release goals.

## Ownership and open questions

Brie is Product Lead and owns product scope, priorities, and acceptance. The [team roster](team-areas.md) identifies current functional owners, including unfilled areas. Technical owners research and recommend implementation approaches, record decisions, and estimate their work.

The [gap review](gap-review.md) tracks unresolved decisions, including the conversation name, panel and result layout, access through existing connections and repository authorization, storage ownership and approach, model configuration, safe usage limits, retention, and direct code-editing scope. Team poll results and agreed design choices can be incorporated in later revisions.

The [MVP plan](mvp.md) defines delivery work, while [implementation decisions](implementation-decisions.md) and [release checks](acceptance-and-evidence.md) contain technical research and evidence. The PRD governs product requirements.
