---
title: "DBJ.METHOD Skills"
date: 2026-07-01
draft: false
summary: "Direct mapping to AI Readiness — DBJ.METHOD encoded as Claude Skills."
---

## Intent

This site encodes DBJ.METHOD — the enterprise architecture methodology
authored by Dušan Jovanović (DBJ), TOGAF-registered since November 2011 —
as Claude Skills, so that any Claude instance can apply the method
consistently, using official terminology with no reinterpretation, instead
of relying on ad-hoc explanation each time.

Each skill is a self-contained layer of the method, kept deliberately
separate rather than merged, because the source material itself treats
them as distinct:

| Skill | Answers |
|---|---|
| [dbj-taxonomy]({{< ref "dbj-taxonomy" >}}) | Where does a concern sit? (4 Categories × 4 Capabilities) |
| [dbj-bpt]({{< ref "dbj-bpt" >}}) | Who owns delivery? (Business → Product → Technology loop) |
| [dbj-cmm]({{< ref "dbj-cmm" >}}) | Is the org ready? (5-element maturity scoring, L0–L5) |
| [dbj-adm]({{< ref "dbj-adm" >}}) | How are decisions authorized? (5-step governance wheel) |

Authoritative sources for all four: [method.dbj.org](https://method.dbj.org)
(taxonomy_core.html, bpt.html, cmm.html, kb/DBJ_ADM/). If a skill and its
source page ever disagree, the source page governs — flag the discrepancy
rather than silently trusting the skill.

## How to use

**Claude.ai (web/mobile):** Settings → Capabilities/Skills → Upload
custom skill → select one subfolder at a time (dbj-taxonomy, dbj-bpt,
dbj-cmm, dbj-adm). Each upload must point at the folder, not the loose
SKILL.md file, since the folder name is what disambiguates the four
identically-named SKILL.md files.

**Claude API:** upload each SKILL.md as skill_data, then reference the
resulting skill_id via container.skill_ids in a Messages request using
the Code Execution tool.

**Claude Code:** register this repository as a plugin marketplace, then
install each skill individually.

Once installed, no manual invocation is needed — Claude loads a skill's
frontmatter (name + description) automatically and pulls in the full
body only when a request matches its trigger conditions.

## Intellectual Property & Licensing

DBJ.METHOD — including the Taxonomy, B-P-T Operating Model, DBJ CMM, and
DBJ ADM — is the original work of Dušan Jovanović (DBJ), practicing under
DBJ.METHOD / method.dbj.org since 2011.

© Dušan Jovanović. All DBJ.METHOD content, terminology, and structure
originate from method.dbj.org and are the author's intellectual property.
These skill pages are derivative encodings of that source for use with
Claude.

**Individual / non-commercial use:** licensed under
[Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).
You may share and adapt this material for personal, educational, or
non-commercial purposes, provided you give appropriate attribution to
Dušan Jovanović / DBJ.METHOD and distribute any derivative works under
the same license.

**Commercial use:** not covered by the CC BY-SA 4.0 grant above. Any use
within a commercial product, service, consulting engagement, or internal
enterprise deployment requires separate licensing terms and fees. Contact
Dušan Jovanović directly to arrange commercial licensing.

Practice positioning: "High delivery. Low hype." / "Prove first. ROI next."
