---
file: contents/02-fundamentals.tex
section: sssec:generative-vs-discriminative
issue_id: "#32"
---

<!-- LTeX: enabled=false -->

# Writing Notes

- outputs can be distinguished into two distinct classes with different properties, particularly regarding outputs
- **discriminative AI** is trained to distinguish two or more classes from each other
	- classic use cases are image classification, anomaly detection, sentiment analysis
	- can be achieved by very simple methods (that are inherently easy to understand for humans)
		- linear regression
		- SVMs, decision trees
	- output is limited to a single bit or at most hundreds of bits from an information theory perspective (*Schneider (2024)*)
- **generative AI** is trained on vast amounts of data to generate new outputs based on an input prompt
	- popular use cases are text (*Brown et al. (2020)*; GPT-3) or image generation (*Rombach et al. (2020)*, Stable Diffusion)
	- enabled by very large, black-box models, that have drastically grown over the last half decade (*Brown et al. (2020)* to *Introducing GPT-4.5|OpenAI (2025a)*)
		- recent boom enabled by sufficiently powerful hardware, to support large models required to generate outputs
		- many recent models are based on transformers (GPT series and derivatives) or diffusion architectures
	- output is virtually unlimited in size, but often tens of thousands of bits of information (*Schneider (2024)*)
- difference leads to massive theoretical shift in XAI methods (*Kumarage & Saarela (2026)*)
	- discriminative models assume deterministic mappings from input to output
		- XAI methods build on that assumption (e.g., feature attribution, counterfactuals)
		- discriminative AI looks for the attribution of **causal responsibility** in the form of features
	- GenAI breaks assumption of determinism
		- outputs are variable in size
		- semantics are encoded in high-dimensional abstract spaces rather than input features
		- question remains "why", but answers lie in the abstract factors within generative models

# Open Questions

- Confirm frontmatter `file` path: notes show `content/02-fundamentals.tex` but repository uses `contents/02-fundamentals.tex`. Please confirm which is correct.
   - yes, I fixed the frontmatter
- Confirm the target subsection label `sssec:generative-vs-discriminative` is the intended insertion point (I found this label in `contents/02-fundamentals.tex`).
   - yes, this is correct
- Please provide preferred draft **tone** and **length** (e.g., 200–400 words, neutral/academic).
    - please aim for a concise, academic tone and a length of around 600 words
    - align the tone with the rest of the thesis, keeping it accessible to readers with a general background in AI
- Which points should be prioritised in the draft (e.g., theoretical contrast, examples, XAI implications)?
   - theoretical contrast is the important part, but the implications for XAI methods should be clearly highlighted as well

# Missing Citations

- [x] Brown2020 (GPT-3; Brown et al., 2020)
- [x] Rombach2020 (Stable Diffusion; Rombach et al., 2020) Replaced with Rombach2022
- [x] OpenAI2025a ("Introducing GPT-4.5" or equivalent OpenAI technical report)
- [x] Kumarage2026 (Kumarage & Saarela, 2026)
- [x] Verify Schneider2024 is present and correct (I found `Schneider2024` in `literature.bib`).

<!-- LTeX: enabled=true -->
