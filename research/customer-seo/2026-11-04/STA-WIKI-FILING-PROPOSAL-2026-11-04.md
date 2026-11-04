# Proposed STA wiki filing

Prepared November 4, 2026. Status: awaiting the required proposal approval.

Shared existing wiki: `/Users/cmp/.codex/.chatgpt-projects/g-p-68be10cec4708191bd135e0f95e8bf86/wiki`.

The wiki helper's ingest command was run against the complete research report. It writes nothing. Its closest matches were general Hormozi reference pages, including free content and proof quality. Those pages are source-specific summaries, so mixing STA business hypotheses into their framework summaries would weaken source boundaries.

## New source record

Create a new immutable source copy of the complete report under `raw/sta-2026-11-04/`, preserving the existing raw files unchanged. Add the provenance document alongside it. The repository archive remains the complete reviewable deliverable.

## New pages

1. `topics/sta-customer-buying-friction.md`: Twelve buyer scenarios, comparison dilemmas, own-brand implications and the need to validate hypotheses with actual STA customer evidence.
2. `topics/sta-search-content-opportunities.md`: Twenty-one English queries, two Spanish candidates, eight conversational prompts, five priority articles and required original evidence.
3. `topics/sta-blog-production.md`: Blog workflow, Mermaid flowchart, editorial review, tracker fields, cadence and measurement. Clearly distinguish a proposed workflow from a working automation.
4. `topics/sta-editorial-outreach.md`: Urban Pitch, SoccerBible, VERSUS and ABC7 prospects, dated contact evidence, story angles, press-kit needs and limits of authority/ranking claims.

## Existing page changes

1. `INDEX.md`: Add an explicit STA research entry point and index the four new pages. Preserve the Hormozi library's own scope statement while clarifying that the wiki also holds separately sourced STA research.
2. `LOG.md`: Append a dated ingestion entry identifying the source, pages created and evidence limitations.

No existing framework topic text or existing raw source would be edited. New pages would link to relevant framework pages and each other without presenting hypotheses as decisions.

## Validation after approval

Each page will have title, updated, status and sources frontmatter; dated changeable claims; links to source files; and no prose dash glyphs. Run the wiki index command, append the ingestion log, and run lint. Report existing unrelated lint findings separately.

## Why approval is pending

The explicitly invoked skill at `/Users/cmp/.codex/skills/wiki/SKILL.md` states: “Get a yes before writing” and “Never skip the proposal step.” The user has authorized the repository commit; this proposal asks only for the separate required wiki filing approval. Nothing in this document claims that the shared wiki has already been changed.
