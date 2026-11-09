# Swedish openEHR archetype translation - Copilot instructions

## Mandatory reference material

Before any translation or translation review, read BOTH repository files in full:
- `translation-guidelines/swedish-guidelines.md`
- `translation-guidelines/standard-translations.md`

Treat these as authoritative project guidance. Do not claim to have read linked external documents unless you actually accessed them. If either local file cannot be read, stop and report the issue. Follow mandatory rules and approved translations, while treating context-dependent recommendations as context-dependent.

## Source and scope

Use the openEHR MCP to retrieve the requested archetype. If MCP is unavailable, explicitly say so; do not silently substitute another source. If a local source is proposed instead, request the user's approval before proceeding. Identify the source archetype ID and version.

Preserve the original archetype ID, node IDs, codes, constraints, data types, structure, terminology bindings and all non-Swedish translations. Only create or update human-readable Swedish translation content and associated Swedish translation metadata. Never silently fix source-language errors or alter technical meaning.

## Determine existing Swedish translation status

An archetype may be untranslated, partially translated, or completely translated. Inspect the actual source at the field, metadata, description, and coded-value level before deciding how to proceed. The existence of an `sv` language block alone does not establish completeness.

- **No Swedish translation:** Create a complete Swedish translation of all applicable human-readable content.
- **Partial Swedish translation:** Identify missing content, retain accurate and guideline-compliant Swedish translations, complete missing translations, and correct substantiated errors. Avoid unnecessary rewrites.
- **Complete Swedish translation:** Review against the English source and project guidance, retain correct wording, and correct identified errors or inconsistencies. Do not rewrite merely for stylistic preference.

Never assume that existing text is correct simply because it is present, or that it should be replaced simply because a different wording is possible.

## Translation principles

Ensure all applicable human-readable content has a correct and complete Swedish translation, preserving existing translations that already meet project guidance.

Translate and localise: use natural, concise, clinically appropriate Swedish rather than literal English syntax, without changing clinical meaning. Reuse approved standard translations consistently. Apply context-dependent choices only after examining the clinical context. Do not turn examples or recommendations into absolute rules.

For terminology decisions, consider the original English label and description, the archetype's clinical context, any associated coded values, and approved Swedish terms. Prefer short, clear, consistent field labels. Do not change an existing Swedish term solely because another expression sounds more natural or specific. Retain accurate, understandable, compliant existing terms.

Adapt examples and keywords for Swedish clinical use. Do not automatically remove alternative keyword spellings that may be useful for searching, even if they are not the preferred spelling in clinical prose.

## Review and change control

When proposing a terminology change, provide the node ID or location, original English text, existing Swedish text, proposed Swedish text, and a concise reason tied to a specific guideline or clinical meaning.

Classify findings as:
- **Error:** incorrect translation, grammatical mistake, or violation of a mandatory guideline.
- **Recommended improvement:** a substantiated improvement in clinical precision, clarity, or consistency.
- **Optional suggestion:** a stylistic alternative not required for correctness.

Do not edit files when the user has requested review only. For a translation/update task, create the requested output file, not just a report. Do not overwrite an existing archetype file without explicit user authorization. Use the repository's established output location and naming convention; if an output name conflicts with an existing file, use a distinct filename or ask the user.

## Swedish translation author metadata

When creating a new Swedish translation, check whether the `language.translations["sv"]` section contains translator metadata.

If translator metadata is missing, ask the user to provide the translator's name, organisation, and email address before finalising the ADL file.

Do not assume that the current user is the translator. Never invent or hardcode translator details.

When updating an existing Swedish translation, preserve existing translator metadata unless the user explicitly requests a change.

Do not copy translator metadata from other languages.

## Validation and final response

Before exporting, independently check the Swedish content against both guideline files. Check completeness, standard terms, field and archetype references, and consistency. Compare technical identifiers, codes, constraints and structure with the original source. Distinguish checks actually performed from checks not possible in the current environment. Do not claim CKM import validity without validating it.

Report:
- Source archetype ID and version, and how it was retrieved.
- Reference files actually consulted.
- Initial Swedish translation status: none, partial, or complete.
- Whether Swedish content was created, completed, or revised.
- Output file path, or an explicit explanation if no file was created.
- Significant changes, remaining terminology uncertainties, and source issues.
- Validation results and limitations.

A human must review the translated archetype before CKM publication.
