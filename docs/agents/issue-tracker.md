# Issue tracker: GitHub

Use GitHub Issues in quocthai912/Lumina-Nova for execution and coordination.
Specifications, Plans, and Tasks remain repository artifacts.

Use the gh CLI or a connected GitHub tool with equivalent capabilities.
Explicitly target quocthai912/Lumina-Nova and verify the target before writes.
Never publish into a skill's source repository.

## Workflow and sources of truth

Project Phase → Specification → Plan → Tasks → GitHub Issues →
Implementation → Verification and Acceptance.

- Project-level phases are named PHASE 1, PHASE 2, and so on. Each may contain
  one or more Specifications.
- Project phases are distinct from internal phases in Spec Kit tasks.md files.
  A Specification directory's numerical prefix does not identify its project Phase.
- Each approved implementation Task maps to exactly one GitHub Task Issue.
- The originating tasks.md is authoritative for Task definitions, identifiers,
  dependencies, and completion status.
- Issues track execution, coordination, dependencies, and verification evidence.
  Link authoritative artifacts instead of copying lengthy specifications.

Create Task Issues only after the Tasks have been defined and explicitly
approved, and the owner has authorized publication. Task approval alone does
not authorize Issue creation.

## Task identity and publication

Title format:

[PHASE N][Txxx] <Concise task description>

Identify a Task by its originating Specification directory plus Task ID.
Task IDs and Issue titles alone are insufficient because Task IDs may repeat
across Specifications. Preserve the ID assigned in tasks.md, including IDs
longer than three digits.

Before publishing or synchronizing:

1. Confirm the approved project Phase, Specification, tasks.md location,
   Task definitions, dependencies, and authorization. Ask for missing Phase
   assignments rather than inferring them from branches or directory prefixes.
2. Inspect open and closed Issues, following pagination as needed. Match the
   Specification reference and Task ID in their bodies.
3. Reuse the existing matching Issue. Resolve ambiguous or duplicate mappings
   before creating another Issue.
4. Publish only missing approved Tasks, with blockers first. Record each mapping
   in the Issue's traceability references. Add links to tasks.md only when
   authorized, preserving its Task definitions and IDs.
5. Verify that every Task selected for publication has exactly one matching
   Issue and that its references and dependencies match the approved artifacts.
   Report any unresolved mapping or failed update.

## Required Task Issue content

Preserve these sections in every Task Issue.

### Approved Task and traceability references

Include the project Phase, Task ID, originating Specification directory,
links to spec.md and the relevant tasks.md Task location, and relevant plan.md
references. Record or link the owner approval covering the Task.

### Scope

Describe the approved outcome and details needed for independent execution.
Identify relevant boundaries without expanding the approved Task.

### Dependencies

List each approved prerequisite by Specification and Task ID, with its Issue
reference. State "None" when there are no approved dependencies.

Mirror these dependencies using GitHub's native issue dependencies where
available. Otherwise, use explicit "Blocked by: #..." references here.
Preserve this section even when native dependencies exist.

Issue hierarchy or membership in a project Phase does not imply a dependency.
A prerequisite is satisfied when its authoritative Task status and completion
evidence support completion. Surface discrepancies before proceeding.

### Acceptance criteria

Provide checkable criteria derived from the approved Task, Specification, and
Plan. Link supporting detail. Seek approval for missing or changed criteria
rather than inventing requirements.

### Implementation and verification evidence

When available, record implementation references, checks and observed results,
remaining limitations, and acceptance-criterion outcomes. Until evidence exists,
state that implementation or verification is pending.

## State, labels, and synchronization

- Incomplete Tasks remain open.
- Blocked Tasks remain open. Document the actual blocker, its effect, and the
  action or decision required to resolve it.
- Complete a Task only after satisfying its acceptance criteria and recording
  appropriate implementation and verification evidence.
- For successful completion, update the authoritative tasks.md checkbox,
  apply the existing completed label, and close the Issue as completed within
  the authorized completion workflow.
- When approved work becomes incomplete again, reopen the Issue, remove its
  completed label, and clear its tasks.md checkbox.
- Verify both artifacts after synchronization. Resolve mismatches using the
  approved Task and evidence; a closed Issue alone does not justify checking
  off a Task. Report any update that could not be completed.
- Cancellation or duplicate closure does not establish successful completion.
  Record the reason and obtain approval for any Task disposition change;
  leave unfinished work unchecked and without completed.

The completed label already exists. Do not create, recreate, rename, or modify
its definition. Do not introduce issue-type, status, priority, or triage labels.

Closing every Task Issue does not establish acceptance of a Specification or
project Phase. Report verification results and obtain explicit owner acceptance.

## Other Issue categories and skill compatibility

Bug reports, research questions, and exploratory decision tickets may exist
independently of implementation Tasks. Explicitly identify their category in
the title or body without adding labels. They do not authorize implementation
scope; route resulting specification-governed implementation through the
approved SDD workflow.

All Task-to-Issue publishing mechanisms must follow this document's approved
title format, Specification-scoped Task identity, deduplication, traceability,
and authorization requirements. Tool or skill defaults do not replace them.

When a skill says "publish to the issue tracker", apply these rules before
creating anything. When it says "fetch the relevant ticket", read the Issue
body and relevant comments together with its authoritative Task artifacts.

For to-tickets, proposed slicing changes must first be reflected in tasks.md
and approved. Publish one Issue per approved Task and omit ready-for-agent.

Wayfinder's label-dependent map workflow conflicts with the minimal label
conventions above. Do not run it unchanged or create its labels. Obtain owner
approval for a compatible adaptation before using that workflow.

## Operational safeguards

- Retrieve all relevant open and closed Issues before deduplicating; default
  list limits may omit matches.
- Check installed tool capabilities before using dependency operations. Use
  supported native relationships or the body-reference fallback above.
- For multiline gh bodies and comments in PowerShell, use a UTF-8 temporary
  file and --body-file to preserve content and avoid shell interpolation.
- Record evidence before closing. Add evidence to an already-closed Issue
  through a separate comment rather than relying on another close operation.

## Pull requests as a triage surface

PRs as a request surface: no.

## GitHub Projects

The owner will configure GitHub Projects manually later. Do not create,
configure, or modify Projects. Projects are not a prerequisite for this workflow.
