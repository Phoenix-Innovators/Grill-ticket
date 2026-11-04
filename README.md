# Grill Lab

Grill Lab helps the team turn unclear Jira tickets into clear requirements and useful build guidance.

- **Grill My Ticket:** asks up to five questions, then helps the author edit and approve acceptance criteria—the checks that show the work is done.
- **Context Lab:** uses those approved criteria, team documents, and code to suggest next steps and ways to check the work.

**Current status:** planning documents are ready for team review. The app has not been built or tested.

## Do we need all seven starter files?

We do not need to read or update all seven for every task. The PRD, MVP, and team responsibilities are the core planning documents. This README is the guide to using them. The other three documents preserve research, open questions, and release checks so owners can use them when needed.

Keeping them separate is useful while we build: product requirements, suggested approaches, and test results have different purposes. Keep them for now. Once decisions are settled, the team can shorten or combine supporting documents without losing the requirements or release evidence.

## How to use each file

### 1. README — start here

Use this file when joining the project or deciding where to find something. It explains the product, current status, and document workflow. Update it when the project status or document structure changes. Detailed requirements and task results belong in the files below or their related Jira issues.

### 2. [PRD v1](docs/prd.md) — understand what we must build

Everyone should read this first. It defines the users, both features, required behavior, scope, and success measures. Brie owns product scope; area owners contribute changes affecting their work.

Use the PRD to answer “Does the product need to do this?” Its requirement IDs, FR01–FR10, let issues and tests point to a specific behavior. Update it when an agreed product decision changes the experience, scope, or acceptance target. A build recommendation does not override a PRD requirement.

### 3. [MVP v1](docs/mvp.md) — turn the product into work

Read this after the PRD. It gives the build order, work packages B01–B10, contributors, and ticket standard. Each area owner uses it to estimate and create small Jira issues. The package IDs are planning references; they are not issues already created.

Each issue should state the outcome, one responsible owner, relevant PRD requirement, scope, dependencies, and two or three checks that show it works. Update the MVP when the delivery plan or an adopted starting choice changes. Keep day-to-day progress and detailed decisions in the owning issues.

### 4. [Team responsibilities](docs/team-areas.md) — know who to involve

Use this when assigning an issue, asking for help, or identifying a missing role. It explains each person's area and shows roles still marked TBD. People can collaborate across areas; each actual issue still needs one responsible owner.

Brie coordinates filling unassigned roles. Update this file when assignments or area status change, using actual work as evidence. Creating a plan does not mean implementation has started.

### 5. [Build recommendations](docs/implementation-decisions.md) — choose an approach

Owners consult the relevant section when designing access, privacy, saving, AI spending, or cleanup. Sections D01–D07 explain the recommended approach and link to official sources. Nobody needs to read every section before starting unrelated work.

These are recommendations for owner review. Record the chosen approach and why in the related issue. If the team adopts a different approach, update the recommendation so it reflects that choice. Changes affecting product behavior, cost, permissions, or other roles need the relevant team review.

### 6. [Release checks](docs/acceptance-and-evidence.md) — prove the work is ready

Use this while defining issue checks, during implementation, and before release. It contains ten workflow checks, J01–J10, and six additional checks, C01–C06. It also explains model comparison, accessibility, and the pilot.

Owners attach results to their issues: what was tested, app version, observed outcome, reviewer, and evidence link. Testing coordinates coverage once that role is assigned; Brie leads product acceptance. Update the checks when required behavior changes, and record results before calling work complete.

The ten workflow checks are separate from the ten representative pilot tickets that must complete both features. The suggested eighteen model examples are a third, separate comparison exercise.

### 7. [Remaining gaps](docs/gap-review.md) — track unanswered questions

Use this during planning and when an issue depends on an unresolved choice. G01–G12 identify the main gaps, recommended answers, and proof still needed.

The relevant owner works through the gap in their implementation issue. Update its row when a decision is adopted or evidence changes its status, and link the issue or result. A recommendation alone does not close a gap; say whether it is decided, implemented, or verified. Brie coordinates blockers and questions affecting several areas.

## A simple workflow for each task

1. Find the required behavior in the **PRD**.
2. Find its work package in the **MVP** and choose an issue owner using **team responsibilities**.
3. Read only the relevant **build recommendation** and **gap**. Record the approach and unresolved dependencies in the issue.
4. Build the change and run the relevant **release checks**. Attach results to the issue.
5. Update any affected requirements, plan, recommendations, or gaps before closing the issue. Change only the documents affected by the work.

For example, an issue about safely approving criteria can link **FR05** (required behavior), **B06** (work package), **D04** (saving recommendation), **G05** (remaining proof), and **J05/C03** (checks). The issue holds the detailed implementation and results; those links explain why the work exists and how to assess it.

## What to do next

Start with B01: prove the app can read a real ticket, Confluence page, and repository file, call AI, and save and reload a result. Also prove denied access. Alan and Michael lead that work, with Kandis checking AI behavior. Then agree the shared boundaries in B02 and build both features.

Keep the PRD and MVP at v1 until the team agrees to change their version labels. Keep private source content and credentials out of documentation and test evidence.
