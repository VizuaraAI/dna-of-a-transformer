# The DNA of a Transformer 🧬

**An interactive visual guide to the inner workings of a GPT — built entirely from scratch.**

🔗 **Live Demo:** [vizuaraai.github.io/dna-of-a-transformer](https://vizuaraai.github.io/dna-of-a-transformer/)

---

## About

This project is a tribute to [Andrej Karpathy's MicroGPT](https://github.com/karpathy/microgpt) — a 243-line, zero-dependency Python implementation of a complete GPT (training + inference). No PyTorch. No NumPy. Just pure Python and math.

We built an interactive, animated educational experience that walks you through every layer of the transformer architecture, line by line. Each section pairs a live diagram with the actual source code, highlighting the exact lines being visualized in real time.

---

## What's Inside

### Guided Code Walkthrough (Sections 01–07)

Each section covers a core component of the GPT architecture with synchronized animations — the diagram on the left animates through stages while the corresponding code lines highlight on the right.

| Section | Component | What You'll See |
|---------|-----------|-----------------|
| **01 — Data** | Tokenization | Character-level tokenizer mapping `hello` → `[7, 4, 11, 11, 14]` with BOS tokens |
| **02 — Autograd** | Autograd Engine | Computation graph building → forward pass → backward pass with gradient flow |
| **03 — Architecture** | GPT Data Flow | Full 7-layer data flow: Embeddings → RMSNorm → Attention → Residual → MLP → Logits |
| **04 — Attention** | Multi-Head Attention | Live causal attention matrix with pulsing weights and Q/K/V projections |
| **05 — Training** | Training Loop | Animated loss curve drawing in real-time over 60 steps |
| **06 — Inference** | Text Generation | Autoregressive character-by-character name generation |

Every section includes:
- Actual line numbers from the 243-line source (e.g., `L106–142 / 243`)
- Play/pause controls and adjustable animation speed (0.3x – 2.5x)
- Prose explanations and technical detail callouts

### Interactive Playground (Section 08)

Seven hands-on tools that let you experiment with every building block — ordered to follow the transformer's data flow:

| Tool | What It Does |
|------|-------------|
| **Live Tokenizer** | Type text, see character → integer mapping in real time |
| **Token & Position Embeddings** | Pick a token and position, watch two vectors sum element-wise |
| **RMS Normalization** | Drag input bars, see normalization math live (mean, RMS, scale) |
| **Attention Pattern Explorer** | Type text, hover a causal attention heatmap with per-cell weights |
| **ReLU Activation** | Visualize which neurons survive (active vs. killed) |
| **Feed-Forward Network** | Full MLP pipeline: Input(4) → fc1 → Hidden(16) → ReLU → fc2 → Output(4) |
| **Temperature & Softmax** | Slider from 0.1–3.0 reshaping a probability distribution bar chart |

---

## Design

- **Apple-style minimalism** — dark theme (`#0a0a0a`), Figtree font, subtle purple accent (`#c8a2ff`)
- **Scroll-triggered animations** — sections fade in as you scroll (IntersectionObserver)
- **Code panels** — macOS-style window chrome with syntax-highlighted, line-numbered code
- **Zero build step** — single `index.html`, loads React + Babel from CDN

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | React 18 (CDN, no build) |
| Styling | Inline styles (no CSS framework) |
| Animations | CSS keyframes + JS intervals |
| Charts | Hand-drawn SVG |
| Font | [Figtree](https://fonts.google.com/specimen/Figtree) (Google Fonts) |
| Deployment | GitHub Pages |

**Total dependencies: 0** (just like MicroGPT itself)

---

## Run Locally

```bash
git clone https://github.com/VizuaraAI/dna-of-a-transformer.git
cd dna-of-a-transformer
open index.html
```

No install. No build. Just open the file.

---

## Credits

- **MicroGPT** by [Andrej Karpathy](https://github.com/karpathy) — the 243-line GPT that inspired this project
- **Visualization** by [Vizuara AI](https://github.com/VizuaraAI)

---

## License

MIT License — free to use, modify, and share.

---

<p align="center">
  <strong>243 lines — the most atomic GPT implementation possible.</strong><br/>
  <em>Every line is the algorithm. Everything else is just efficiency.</em>
</p>
