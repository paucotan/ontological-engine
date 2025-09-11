<div align="center">

<a href="onto-engine.png">
  <img src="onto-engine.png" alt="Seer–Scribe Ontological Engine logo" width="180">

</a>

# The Seer–Scribe Ontological Engine

[![status: concept](https://img.shields.io/badge/status-concept-blueviolet)](#)
[![contributions: welcome](https://img.shields.io/badge/contributions-welcome-brightgreen)](#contributing)

<em>A two-part framework for building systems that don’t just process information — they begin to understand.</em>

</div>

## Abstract


We propose a two-part cognitive architecture, the Seer–Scribe Ontological Engine, inspired by the human perception-to-language pipeline. Just as the eye and visual cortex transform photons into shapes before the brain encodes meaning and words, our system separates perception from expression to build a more grounded form of understanding.

Recent advances such as [DINOv3](https://ai.meta.com/dinov3/) demonstrate this perceptual grounding at scale, and the Ontological Engine builds on such models by emphasizing separation of geometry and language, iterative refinement, and structured memory.

- The **Seer** is a self-supervised vision model (e.g., DINO/JEPA) functioning like a synthetic retina–visual cortex. It learns directly from raw inputs (images, video, graphs) without labels, discovering recurring geometric motifs — branching, loops, flows, meshes — encoded as latent structures in its representational space. These motifs live in the Seer’s latent space — a high-dimensional map where similar shapes cluster together (rivers, veins, trees).
- The **Scribe** is a large language or vision–language model playing the role of the linguistic cortex. It interprets the Seer’s latent motifs, attaching words, metaphors, and boundaries (e.g., “branching flow” breaks when paths form closed loops).
- The **Conductor** is a lightweight controller that mirrors attentional circuits, orchestrating a loop of Sense (Seer) → Say (Scribe) → Check (contrast and refinement).
- The **Castle (Memory)** is a growing library of “bricks” (stable motifs), analogous to hippocampal consolidation, each containing a sketch, label, examples, and failure cases.

By mimicking this human-like separation of vision and language, the Seer–Scribe system allows geometry to emerge from light-driven perception before being translated into words. This separation enables discovery of cross-domain principles — rivers and veins converging as “branching flow” — and the construction of an encyclopedia of motifs that resonates across domains. In doing so, the Ontological Engine moves beyond information processing toward anatomies of understanding, grounded in the geometry of the world.

This project is speculative and experimental — an attempt to sketch the anatomy of understanding rather than claim a finished solution.

## Table of Contents

- [Abstract](#abstract)
- [Concept](#concept)
- [Why It Matters](#why-it-matters)
- [How It Works](#how-it-works)
- [What This Builds](#what-this-builds)
- [Next Steps](#next-steps)
- [Contributing](#contributing)
- [In Essence](#in-essence)

## Concept

The Seer–Scribe Ontological Engine is a two-part framework for building machine systems that don’t just process information — they begin to understand.

- **Seer:** Inspired by JEPA/DINO; perceives the geometry of meaning from raw data — shapes, flows, and relations that repeat across domains — without labels.
- **Scribe:** An LLM or vision–language model that translates those shapes into words, metaphors, and boundaries using its prior training on human language.
- **Conductor:** Orchestrates a simple loop: Sense → Say → Check.
- **Castle (Memory):** A growing library of “bricks” (motifs), each with a label, boundaries, and examples across domains.

## Why It Matters

- **AI today:** LLMs are great with words but shallow in grounding. World‑model research (LeCun, Schmidhuber, DeepMind) is advancing, but geometry and language are often entangled.
- **Our idea:** Separate them. Let one model see geometry, and the other speak it. Refine meaning through contrast — know what something is by knowing what it is not.
- **Result:**
  - Discover principles (branching, flow, feedback) without labels.
  - Express them in human language.
  - Transfer them zero‑shot across domains (rivers ↔ traffic ↔ vascular systems).

## How It Works

Example: rivers → “branching flow”

1. **Sense (Seer)**
   - Input: images of river deltas.
   - Output: exemplars + relation sketch + contrasts (e.g., braided river, looped canal) + simple transformations.
2. **Say (Scribe)**
   - Reads the Seer’s shape summaries.
   - Proposes candidate names (“branching flow,” “tree-like fan-out”).
   - States a boundary: “breaks when paths form closed loops.”
   - Asks a clarifying question: “Show a loop-heavy case.”
3. **Check (Conductor)**
   - Seer returns the contrast (canal loops).
   - Scribe revises label → “branching flow” applies to rivers, not canals.
   - If stable: reinforce and store as a brick.
4. **Memory (Castle)**
   - Brick stored: `{sketch, label, essence, examples, where-it-breaks}`.
   - Over time: build an encyclopedia of motifs — the foundations of a world model.


## What This Builds

- **Foundation:** A geometry‑based perception engine (Seer).
- **Walls:** Language anchors and boundaries (Scribe).
- **Towers:** Cross‑domain analogies (traffic, rivers, vasculature).
- **Empire:** A growing, testable world model of patterns and principles.

## The Castle (Dynamic Memory)

The Castle is not a static library, but a dynamic, evolving memory structure:

- Each "brick" is a hypothesis — a motif paired with a label and a boundary.
- Bricks can be reinforced (strengthened), replaced, or revised as new evidence arrives.
- The Castle keeps a version history of motifs (e.g., v1, v2), tracking how concepts evolve.
- Confidence scores determine how stable or tentative a brick is within the Castle.
- Sometimes, foundational bricks are replaced, leading to "castle quakes" — major restructuring of the ontology.
- This dynamic property mirrors human cognition, where knowledge is continually updated, sometimes painfully, when foundational beliefs shift.

## Next Steps

This is a conceptual prototype — we welcome collaboration!

1. **MVP idea**
   - Use a DINO/JEPA model as Seer (via API).
     - Reference: [DINOv3 by Meta](https://ai.meta.com/dinov3/)
   - Use ChatGPT (or a vision–language model) as Scribe.
   - Controller = a lightweight script for the Sense → Say → Check loop.
   - Visualize embeddings with UMAP or t-SNE.
   - Dataset = small paired domains (rivers, traffic, vasculature).
   - Cluster motifs with k-means or DBSCAN, and store results as JSON or SQLite 'bricks.'
2. **Publish & refine**
   - Add examples and diagrams.
   - Document early tests (even toy demos).
3. **Collaborate**
   - Open-source contributors can experiment with real models.
   - Cognitive scientists and philosophers can help shape the theory.

## Contributing

Contributions, questions, and critiques are welcome. Please open an issue to discuss ideas or a PR with proposed changes. If you have strong views on representation learning, grounding, or analogy, we’d love your perspective.

## Open Source & License

This project is intentionally open-source and collaborative. We welcome ideas, critiques, experiments, and extensions from researchers, engineers, and artists.

- Content (docs, text, diagrams): Creative Commons Attribution 4.0 International — CC BY 4.0. See `LICENSE-CC-BY-4.0.md`.
- Code samples and scripts: MIT License. See `LICENSE`.
- By contributing, you agree to license your contributions under the same terms.

Badges: [![CC BY 4.0](https://img.shields.io/badge/content-CC%20BY%204.0-lightgrey)](https://creativecommons.org/licenses/by/4.0/) [![MIT](https://img.shields.io/badge/code-MIT-blue)](LICENSE)

## In Essence

- The **Seer** understands without words.
- The **Scribe** words what is perceived.
- Together, they create an engine of insight, analogy, and cross‑domain resonance — building toward a world model.
- In short: the Seer–Scribe Ontological Engine separates seeing from saying — letting geometry emerge first, and language refine it after.
