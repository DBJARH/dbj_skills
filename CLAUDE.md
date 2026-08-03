# CLAUDE.md

DBJ's C23 code examples.

## Conversation protocol

- Be very brief in your answers 
  - If you think you know longer answer is required make it longer
- Use simple terminology
  - Move explaining of complex and necessary stuff into footnote section of the document
    - Call it "Vocabulary"
- Do not over explain "in line"
  - Instead use the "Vocabulary" section
    - And point to external sources if any
- Do not assume anything, if in doubt ask


## Document versioning

- Every markdown file **SHOULD** (not must) carry a decimal `version:` key in its front matter:

```yaml
---
version: 0.1
---
```

- `0.1` .. `1.0` — pre-releases leading up to release 1
- `1.1` .. `2.0` — releases 1.1 through 2.0
- and so on by the same pattern

SHOULD, not MUST: skip it where this repo forbids front matter, and where front matter already exists just add the `version` key without disturbing the rest.
