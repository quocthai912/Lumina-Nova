# Agent guidance

Lumina-Nova is a personal AI-powered learning assistant based on
Retrieval-Augmented Generation (RAG).

## Start here

1. Read this file and any applicable directory-level agent guidance.
2. Inspect the working branch, working tree, and files relevant to the request.
   Preserve existing user changes.
3. For specification-governed work, read the originating spec.md, plan.md, and
   tasks.md as relevant. Consult the project constitution when populated;
   template placeholders are not approved requirements.
4. Before using an installed skill, read its SKILL.md and apply the repository
   conventions when adapting its defaults.

Use Progressive Disclosure: load supporting documentation when the task needs
it. Keep each rule or fact in its authoritative source and reference that source
instead of duplicating it.

Follow additional context pointers when established and relevant. Do not invent
Context Package files or require reading files that do not exist.

## Authority and scope

For specification-governed implementation, follow:

Project Phase → Specification → Plan → Tasks → GitHub Issues →
Implementation → Verification and Acceptance.

New feature development and substantial changes to application behavior are specification-governed by default, unless the owner explicitly authorizes an exception.

Approved Tasks are mandatory for specification-governed implementation.
Explicitly authorized repository setup, maintenance, bug investigation,
research, and documentation work may proceed without an originating tasks.md.
These activities remain bounded by the owner's authorized scope and must not
silently expand approved implementation scope.

Obtain explicit owner approval before changing consequential scope,
requirements, architecture, dependencies, or acceptance criteria. Surface
conflicts between approved artifacts rather than resolving them through
undocumented assumptions.

Skill defaults do not authorize scope expansion or external actions. Commits,
pushes, Issue creation, and other consequential repository or GitHub mutations
require owner authorization covering those actions. Review-only requests permit
inspection and proposals only. Keep changes limited to the authorized work.

## Agent skills

### Issue tracker

Before publishing, synchronizing, updating, or executing Issue-backed work, read
docs/agents/issue-tracker.md for Task mapping, authorization, and completion rules.

### Domain docs

Before domain exploration, terminology changes, or architectural work, read
docs/agents/domain.md for glossary and ADR discovery and consumption rules.

## Verification and reporting

Verify work against approved Task acceptance criteria or, for authorized work
outside tasks.md, the requested outcome. Report what changed, checks actually
run and their observed results, checks not run, and remaining blockers or
limitations. Link evidence where available.

Claim passing tests or completed implementation only when supported by observed
evidence. Follow the tracker rules for Task completion and Phase acceptance.
