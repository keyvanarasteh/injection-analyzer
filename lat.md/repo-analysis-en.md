# Repository analysis template (EN)

This page is a concise, reusable checklist for mapping documented injection techniques to repository code.

**Language:** [EN](repo-analysis-en.md) | [TR](repo-analysis-tr.md) · [[lat.md#Repository injection analysis workflow|Workflow diagram]]

## 1. Select and acquire the repository

Record what was analyzed and where it came from.

- Repository URL: `[URL]`
- Revision (commit/tag): `[revision]`
- Acquisition date: `[date]`
- Scope and exclusions: `[directories, generated or vendored code]`
- Provenance notes: `[clone/archive source and constraints]`

## 2. Identify languages and frameworks

Use manifests, lockfiles, build configuration, and source files as evidence; record versions where available.

| Technology | Version evidence and source | Official site | Documentation URL(s) |
|---|---|---|---|
| `[name]` | `[file and version]` | `[URL]` | `[version-matched URL and section]` |

## 3. Find documented injection techniques

Use official, version-matched documentation. Record its terminology, conditions, relevant APIs or configuration, and mitigations.

| Technique | Documentation evidence | Conditions / recognizable patterns | Version scope |
|---|---|---|---|
| `[technique]` | `[URL, section, concise paraphrase]` | `[conditions and APIs]` | `[versions]` |

Separate what the documentation states from your interpretation.

## 4. Map techniques to source

Search for documented APIs, sinks, configuration patterns, and related data flows. Record each relevant source location; a text match alone does not prove exploitability.

| Technique | Source path and line/symbol | Role and data flow | Evidence status |
|---|---|---|---|
| `[technique]` | `[path:line or symbol]` | `[source → transformation → sink]` | `[confirmed / partial / not found]` |

## 5. Trace functions and callers

For each match, identify the containing function, callers, and entry point. Follow whether untrusted input can reach the relevant operation.

| Source symbol | Containing function | Caller chain / entry point | Input and reachability evidence |
|---|---|---|---|
| `[path#symbol]` | `[function/class]` | `[caller chain]` | `[source and reasoning]` |

If reachability or a call path is unverified, state that limit explicitly.

## 6. Write human-readable findings

Explain the code behavior, input, data/control flow, and match to documentation in plain language.

- Finding: `[short title and affected component]`
- Conditions and impact: `[when it matters]`
- Confidence: `[high / medium / low, with reason]`
- Evidence: `[source locations and documentation URLs]`
- Assumptions or gaps: `[items]`

Keep facts, analysis, and assumptions distinct. Report negative searches with their scope and search patterns; no match is not proof of absence.

## 7. Handoff

Capture what the next analysis stage needs.

- Confirmed findings: `[summary and references]`
- Partial mappings or evidence gaps: `[items]`
- Techniques searched but not located: `[scope and terms]`
- Questions and next steps: `[items]`
