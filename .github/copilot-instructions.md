<!-- .github/copilot-instructions.md - Guidance for AI coding agents working on this repo -->
# Copilot instructions for SOVRIN-IMO-P4-FINAL-TRACELOCK

Purpose: give an AI coding agent the exact, actionable knowledge needed to be productive in this repository.

1) What this repository is
- This repo is primarily a research/documentation deliverable for the SOVRIN-KAIROS audit-grade AI project (see `README.md`).
- It documents a modular SOVRIN-KAIROS M1–M13 architecture, forensic audit trails (SHA-256 based), and an IMO 2020 Problem 4 case study.

2) Big-picture architecture (from README.md)
- Modular research stack: references to "SOVRIN-KAIROS M1–M13" indicate a modular, layered design. There are no compiled components detected in the repo — it's a documentation artifact.
- Data/trace flow concept: reasoning outputs are expected to be hash-locked with SHA-256 to create an immutable audit trail. The README is the canonical source describing this approach.

3) Developer workflows & quick commands (discovered / inferable)
- There is no build system or test harness in the repository root. Treat edits as documentation changes.
- To generate / verify SHA-256 audit hashes (macOS):
```
shasum -a 256 path/to/file
```
- To preview docs locally, open `README.md` in your editor or render it as markdown in a browser or VS Code preview. The README references an interactive CodePen for the live forensic view.

4) Project-specific conventions and patterns (explicitly discoverable)
- Focus is on forensic-grade traceability and verifiable provenance. When adding or editing content, include: the explicit SHA-256 digest of any artifact you describe, the date/time (ISO 8601), and an authoritative citation (ORCID/email present in README).
- Citations: use the exact citation block from `README.md` when summarizing or reusing research text.
- Licensing: repository is CC BY 4.0 (see `LICENSE.md`). Preserve license header when reusing significant text.

5) Integration points & external dependencies (what to look for)
- Interactive research view hosted on CodePen (external link in README). Changes to documentation that affect the interactive view should include notes about the CodePen URL and any exported artefacts.
- No package.json, pyproject.toml, Makefile, Dockerfile, CI config, or source code files were found at the time of analysis — do not add code that assumes a particular language/toolchain without first confirming by adding matching config files and tests.

6) Typical edits an AI agent should perform (with examples)
- Update wording, add clarifying sections, or add small reproducible examples of hashing the audit trail.
- Example: when adding an explanation of how to compute an audit hash, include the command and a one-line example using `README.md` itself:
```
shasum -a 256 README.md  # produces the SHA-256 digest for README.md
```

7) Constraints and safe-guards
- Don’t invent source files, build commands, or CI pipelines that are not present in the repo. If you add new tooling/config, also add a minimal README addition explaining how to run it and a tiny verification step.
- Preserve academic attribution and license text when copying content from `README.md`.

8) Where to look next (key files and links)
- `README.md` — canonical description of architecture, methodology, and external links (CodePen, ORCID).
- `LICENSE.md` — licensing rules to follow when reusing text.

If anything in these instructions is unclear or you want the agent to perform edits (for example: add an example audit-trace file, or scaffold a minimal preview pipeline), tell me which change to make and I will update or extend these instructions.
