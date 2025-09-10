<div align="center">

<a href="onto-engine.png">
  <img src="onto-engine.png" alt="Seer–Scribe Ontological Engine logo" width="180">
  
</a>

# The Seer–Scribe Ontological Engine

[![status: concept](https://img.shields.io/badge/status-concept-blueviolet)](#)
[![contributions: welcome](https://img.shields.io/badge/contributions-welcome-brightgreen)](#contributing)

<em>A two-part framework for building systems that don’t just process information — they begin to understand.</em>

</div>

## Table of Contents

- [Concept](#concept)
- [Why It Matters](#why-it-matters)
- [How It Works](#how-it-works)
- [Architecture](#architecture)
- [Next Steps](#next-steps)
- [Contributing](#contributing)

## Concept

The Seer–Scribe Ontological Engine separates geometric understanding from linguistic expression so the system can discover, name, and refine cross-domain patterns.

- **Seer:** Unsupervised perception (inspired by JEPA/DINO) that infers the geometry of meaning — shapes, flows, and relations that repeat across domains.
- **Scribe:** A language model that translates those shapes into words, metaphors, and boundaries using its linguistic prior.
- **Conductor:** Orchestrates a simple loop: Sense → Say → Check.
- **Castle (Memory):** A growing store of “bricks” (motifs) with labels, boundaries, examples, and where they break.

## Why It Matters

- **Today’s gap:** LLMs are fluent but often shallowly grounded. World-model efforts (LeCun, Schmidhuber, DeepMind) advance grounding, yet geometry and language remain entangled.
- **Key idea:** Separate them. Let one model see geometry and another speak it. Refine meaning through contrast: know what a thing is by knowing what it is not.
- **Outcome:**
  - Discover principles (branching, flow, feedback) without labels.
  - Express them in natural language.
  - Transfer them zero-shot across domains (rivers ↔ traffic ↔ vasculature).

## How It Works

Example: rivers → “branching flow”

1. **Sense (Seer)**
   - Input: images of river deltas.
   - Output: exemplars, relation sketches, contrasts (e.g., braided river vs. looped canal), and simple transformations.
2. **Say (Scribe)**
   - Reads Seer summaries.
   - Proposes candidate names (e.g., “branching flow,” “tree-like fan-out”).
   - States a boundary: “breaks when paths form closed loops.”
   - Asks clarifying questions: “Show a loop-heavy case.”
3. **Check (Conductor)**
   - Seer returns the contrast (canal loops).
   - Scribe revises the label accordingly.
   - If stable: reinforce and store as a brick.
4. **Memory (Castle)**
   - Brick format: `{sketch, label, essence, examples, where-it-breaks}`.
   - Over time: an encyclopedia of motifs — foundations of a world model.

## Architecture

- **Seer:** Geometry-first perception engine (self-supervised; e.g., DINO/JEPA). Produces sketches, exemplars, contrasts, and simple invariances.
- **Scribe:** LLM or VLM. Anchors shapes to language, proposes names and boundaries, and refines via contrast.
- **Conductor:** Lightweight controller implementing the loop Sense → Say → Check and writing stable bricks to memory.
- **Castle:** A persistent store of bricks (motifs) with cross-domain references and failure cases.

## Next Steps

This is a conceptual prototype — collaboration welcome.

1. **MVP**
   - Seer: DINO/JEPA via API.
   - Scribe: ChatGPT or a vision–language model.
   - Controller: a simple script for the loop.
   - Dataset: small paired domains (rivers, traffic, vasculature).
2. **Publish & refine**
   - Add examples and diagrams.
   - Document early tests (even toy demos).
3. **Collaborate**
   - Open-source contributors: experiment with real models.
   - Cognitive scientists/philosophers: help shape the theory.

## Contributing

Contributions, questions, and critiques are welcome. Please open an issue to discuss ideas or a PR with proposed changes. If you have strong views on representation learning, grounding, or analogy, we’d love your perspective.

## Open Source & License

This project is intentionally open-source and collaborative. We welcome ideas, critiques, experiments, and extensions from researchers, engineers, and artists.

- Content (docs, text, diagrams): Creative Commons Attribution 4.0 International — CC BY 4.0. See `LICENSE-CC-BY-4.0.md`.
- Code samples and scripts: MIT License. See `LICENSE`.
- By contributing, you agree to license your contributions under the same terms.

Badges: [![CC BY 4.0](https://img.shields.io/badge/content-CC%20BY%204.0-lightgrey)](https://creativecommons.org/licenses/by/4.0/) [![MIT](https://img.shields.io/badge/code-MIT-blue)](LICENSE)

---

> In essence: The Seer understands without words. The Scribe gives words to what is perceived. Together they build an engine of insight, analogy, and cross-domain resonance — a growing, testable world model.
