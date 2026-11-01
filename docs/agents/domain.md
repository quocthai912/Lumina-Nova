# Domain docs

Use a single-context documentation layout for Lumina-Nova.

## Discover relevant context

Before exploring domain behavior or proposing terminology or architectural changes:

1. Read root GLOSSARY.md if it exists.
2. Discover ADRs under docs/adr/ if that directory exists, and read decisions
   relevant to the work.
3. Follow relevant references into approved Specifications and Plans as needed.

If the glossary or ADR directory is absent, proceed silently. Their absence
alone is not a reason to create files or directories.

## Authoritative locations

- GLOSSARY.md at the repository root: authoritative domain vocabulary.
- docs/adr/: approved Architecture Decision Records.
- This file: discovery and consumption rules for those sources.

Populate domain documents incrementally as terms and decisions are resolved
and their documentation is authorized. Do not create an empty glossary,
placeholder ADRs, or unnecessary documentation directories.

Use Progressive Disclosure: read relevant decisions and follow their references.
Keep definitions in the glossary and architectural decisions in ADRs; reference
them from other artifacts instead of reproducing their contents.

## Use consistent terminology

Use glossary terms consistently in code, tests, Specifications, Plans, Tasks,
Issues, and reports. Respect explicitly discouraged synonyms.

When a necessary concept is undefined, check existing project usage. Surface
meaningful terminology gaps for owner resolution or the domain-modeling skill.
Distinguish proposed language from approved vocabulary.

## Respect approved decisions

Follow relevant approved ADRs. Distinguish proposed or superseded records from
currently approved decisions.

If a request, proposal, or implementation conflicts with an approved ADR,
identify the record, explain the conflict and its consequences, and obtain
explicit owner approval before changing the decision or implementing a
contradictory approach.

Use the domain-modeling skill when authorized to develop glossary entries or
ADRs. Before reporting domain or architectural work complete, identify any
unresolved terminology questions or ADR conflicts.
