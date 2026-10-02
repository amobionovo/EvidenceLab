# Lesson 05 notebook and scientific QA

Status: notebook and supporting still assets passed local release checks. Video work is tracked separately.

- Template: approved EvidenceLab notebook scaffold and learning flow.
- 25 cells: 13 Markdown and 12 code cells.
- Two fresh Jupyter kernels: 2.73 and 2.7 seconds; zero cell errors or cell warnings after compatibility fixes.
- Every exported file is SHA-256 identical across both runs, including all six charts and 15 CSV tables. No numerical tolerance was required.
- Local runtime launch emitted Windows event-loop and local-kernel TCP diagnostics; these were infrastructure messages, not notebook warnings.
- Python/package versions and seed are recorded in outputs/analysis_manifest.json.
- Raw inputs unchanged; one verified correction; campaign retained; no future data in baseline fitting; MAD-zero handling and IQR arithmetic assertions passed.
- Chart review: all six figures inspected at notebook width. No overlap or clipping observed.
- QR: native PNG, print PNG and standalone QR decoded to the exact Colab notebook target with ZXing. PDF rendering inspected. Only the authorized QR square changed in the native artwork.
- Supplied infographic has small text at whole-page mobile size; zoom is necessary. Its graphs remain conceptual, the six-step workflow is condensed, and its 850 example is synthetic. These distinctions are stated in the lesson README.
- The editable infographic SVG preserves the supplied raster artwork with an independently editable vector QR layer. It does not invent an unavailable fully editable source.
- The print PNG is an upscale of the owner's image, not a claim of new image detail.
- No external downloads, prompts, uploads, installation cells, API keys or widgets in the notebook's default execution path.
- Hosted Colab execution: not yet verified. Local runs do not establish a hosted run.
- GitHub public-link verification: see Release_Log.json after publication.
- Video caption/narration QA: pending video completion; no YouTube/LinkedIn posting performed.
