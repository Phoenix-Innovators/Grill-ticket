# Grill Lab team gap tracker

November 18, 2026

Use this tracker for unanswered questions, decisions the team needs to make, and work that still needs evidence.

New teammates can find their area below, pick an open question, and post what they learn. Ask in the team channel if ownership is unclear.

## How to use this document

1. Find your question in the tables below before starting a duplicate discussion.
2. Claim or confirm an owner in the related GitHub issue or team thread. Treat the listed people and roles as suggested leads until someone claims the work.
3. Research or discuss it. Post a brief answer, the recommended next step, and a link to any evidence (docs, test result, mockup, or GitHub issue).
4. Update the status. Link a test result for real behavior or a recorded decision for a settled question.
5. Found a new gap? Add the next ID (starting with G21) using the short template at the bottom. Flag product scope changes to the Product Lead before adding them to the MVP.

## Status key

| Status | Meaning |
| --- | --- |
| Open | Needs an answer, a decision, an owner, or a real test. |
| Agreed → verify | The direction is agreed. Design, implementation, or testing remains. |
| Verified | The decision or test is complete and linked to evidence. |
| Backlog | Revisit after the core MVP workflow works. |

This tracker holds questions and short decisions. The [PRD](prd.md) defines the user experience. The [MVP plan](mvp.md) defines the first release and work packages. Put detailed technical findings and implementation tasks in the GitHub issues, then link them here.

## What is covered and what remains

### Start here — access, ownership, and connections

These can block or significantly shape the first implementation. Work on independent items in parallel.

| ID | Question to answer | Suggested lead | Status | What closes the gap? |
| --- | --- | --- | --- | --- |
| G19 · Jira access | Can every new teammate actually open the project and its issues? | Shashi (Scrum Master) + Jira admin | Open | Teammates confirm they can open the project and issues. Each remaining blocker has an owner. |
| G10 · Unassigned roles | Who owns Database Management, DevOps, and Testing? | Shashi + team | Open | Names confirmed in [team roster](team-areas.md) and relevant issues. |
| G05 · Saving work | What must persist when a user leaves and comes back, and how will we store it? | Database Management — TBD + Michael (Backend) | Open | Owner proposes a storage approach (evaluate Forge-hosted options first) that supports conversations, progress, approved versions, privacy, and conflict recovery. |
| G01 · Source connections | What can Grill Lab actually read from Jira, Confluence, and connected development tools? | Michael (Backend) | Open | Demonstrate real reads, an AI response, and save and reload. Show which sources are unavailable. |
| G02 · Repository access | Does a Jira-connected repo provide file contents or only issue/branch/PR metadata? | Michael (Backend) + Dan (Security) | Open | Confirm the available access, any required extra authorization, and a denied-access case. Verify source-file access separately from metadata access. |
| G16 · Repo provider | Which existing code connection should the pilot use? | Michael + Dan | Open | Test actual permitted access and record the chosen pilot path. Keep the product provider-neutral (GitHub, GitLab, Bitbucket, etc.). |

### Product and design — agree on the user experience

| ID | Question to answer | Suggested lead | Status | What closes the gap? |
| --- | --- | --- | --- | --- |
| G13 · Panel & results | How will the two functions and Context Lab's results appear inside Jira? | Brie + Kandis (Frontend) + Shannan (UX/UI) | Open | Agree on a simple panel flow or mockup. Tabs are proposed. Both functions stay available anytime. Backend reviews data needs before the design is locked for build. |
| G14 · Conversation name | What should we call the current “interview”? | Brie + team | Open | Review the Discord poll and team input. The Product Lead records the chosen term. |
| G15 · Ticket clarity | How does the AI know when it's helped enough without taking forever? | Brie + Gabba (AI Lead) | Agreed → verify | Define and test quick vs. deeper review, useful clarity signals, and how the user can stop, skip, revisit, or draft anytime. Let the number of questions follow the user’s needs. |
| G07 · Missing information | What happens when a ticket or source doesn't answer everything? | Gabba + Kandis | Agreed → verify | Show honest gaps and partial suggestions. Test a missing-source example. |
| G04 · Private vs. shared | Which drafts and answers stay private, and what exactly is shared on approval? | Brie + Dan + Michael | Agreed → verify | Verify that answers and drafts stay private and permitted ticket viewers can see the explicitly approved criteria. |
| G08 · Old guidance | How does the user know advice needs another look? | Michael + database owner (TBD) | Agreed → verify | Demonstrate outdated/unknown status when sources or requirements change, without silently overwriting saved work. |

### Engineering and release — validate as we build

| ID | Question to answer | Suggested lead | Status | What closes the gap? |
| --- | --- | --- | --- | --- |
| G03 · AI data access | What project information may be sent to the chosen AI service? | Gabba + Dan | Open | Document permitted data, provider requirements, and one approved inference route. |
| G06 · AI cost & retries | How do we avoid surprising charges and unnecessary repeated calls? | Gabba + Backend | Open | Agree on usage limits and budget ownership. Test errors, retries, and unknown paid outcomes. |
| G09 · Quality tests | How will we know each function is useful and accurate? | Gabba + Testing (TBD) + Brie | Open | Agree on representative examples and acceptance tests for each function independently and together. Record evidence, response time, and cost. |
| G11 · Retention & deletion | How long is private work saved, and can it actually be deleted? | Database Management (TBD) + Dan | Open | Agree on retention and verify cleanup, including late/background jobs. |
| G12 · Accessibility | Can someone use the full panel without a mouse or visual-only cues? | Shannan + Kandis + Testing (TBD) | Agreed → verify | Test keyboard, screen-reader labels, error states, progress, and tabs. |
| G20 · MCP | Do we need MCP for a specific pilot use case? | Michael + Gabba | Open — not blocking | Document any concrete benefit of existing tools. A custom MCP server is optional for the MVP. |

### Later — backlog

| ID | Future idea | Status | Revisit when… |
| --- | --- | --- | --- |
| G17 · Automatic monitoring | React to ticket creation/updates/closure, pull requests, or merges. | Backlog | The user-triggered workflow works and the team can identify which events warrant a review. |
| G18 · AI changes to code | Let Context Lab modify or run code with appropriate user permission and approval. | Backlog | The team has evaluated security, execution limits, human approval, and the benefit over proposed code/guidance. |

## Agreed product direction

- Grill My Ticket and Context Lab are connected parts of one product.
- Users can use either function at any time. Context Lab can help before or after criteria approval.
- Users start AI reviews from the Jira panel. Automatic event monitoring stays in the backlog.
- The AI asks purposeful questions, challenges assumptions respectfully, and helps users move forward as soon as they have enough clarity.
- Reuse authorized Jira, Confluence, and development context. Verify access to source files separately from access to a Jira repository link.
- AI can recommend and draft work. Authorized users approve shared requirements and changes to project work.

## Add a new gap

Copy this entry into the relevant section and share it in the team channel.

**G21 · [Short name]**

- **Question:** What exactly do we need to decide or prove?
- **Suggested lead / claimed owner:** Role or @handle (TBD if unclaimed)
- **Status:** Open
- **Needed for:** MVP / later / not sure
- **Answer or next step:** One or two sentences
- **Link:** GitHub issue, discussion, mockup, docs, or test evidence

When a gap is resolved, add Decision / result, date, and evidence link, then change its status to Verified. If it changes product behavior, update the [PRD](prd.md) and affected [MVP work](mvp.md) as well.

Whoever resolves a gap updates its row. Alex (Documentation) can help maintain the tracker. Brie confirms product scope decisions, and Shashi helps with ownership and access blockers.
