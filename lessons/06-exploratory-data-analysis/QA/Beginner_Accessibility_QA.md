# Beginner accessibility QA — 7 October 2026

The revised notebook has 163 cells, including 47 code cells. Two fresh local kernels completed with zero notebook errors. All 17 scientific PNG/CSV/JSON exports are byte-identical to the prior validated interactive release. The inherited dataset, model formula, calculations and scientific charts are preserved. The feature preview and regression summary remain visible when success messages are printed.

The top guide explains explanation/code cells, Run all, completion, chart controls, automatic loading and troubleshooting. Step 0–9, a 25-term glossary, guide blocks, setup folding, optional advanced labels, success messages and two guarded TRY IT cells were added. Existing “What to look for” and “What this does NOT tell us” passages remain unchanged. Apparent performance and inference-versus-prediction imbalance guidance are retained.

Kaleido is absent from mandatory startup dependencies. Its installation is attempted only when optional EXPORT_PLOTLY_IMAGES is True; package-install and image-render failures are caught with a friendly continuation message. Standard Matplotlib exports and interactive Plotly charts do not require Kaleido.

Hosted Colab validation completed on 7 October 2026. A newly created runtime completed all 47 code cells without a traceback and loaded framingham.csv automatically: 4,240 rows, 16 columns, approved SHA-256. Setup cells expose native Show code controls. Live dropdown selection changed glucose in all three distribution panels; the forest-plot hover displayed OR, 95% CI and p-value. A DOM check of all 36 rich-output frames found all 61 interactive plots rendered, 14 static images loaded, zero broken images and zero tracebacks. The code tested at 0aa30d2 is identical to the final notebook code; later edits only move/expand the glossary and document recovery instructions.

Colab intermittently reported that JavaScript output files could not load. Page reload followed by Edit → Clear all outputs and Run all resolved this browser-session problem; all figures then rendered. No browser privacy settings were changed. The beginner troubleshooting guide includes this observed recovery. Hosted library deprecation warnings remain visible and did not stop execution.

The numerical claim ledger and adjusted odds-ratio table match the original release exactly. A separate core-only fresh-kernel run skipped 3D, scatter matrix, parallel coordinates and clustered heatmap cells and completed with zero errors. An assertion verified df_raw equals its unchanged analytical copy; the approved local CSV SHA-256 remains unchanged. Unsupported TRY IT choices print allowed choices without calling analytical helpers.

Full executed Plotly JSON notebooks remain in local QA. Public copies contain static chart previews; Run all creates live interactive output. Prior source/public copies are archived locally under Notebook/Before_Beginner_Accessibility. Original source notebook and dataset are preserved.


Opening ownership cover added on 7 October 2026: the final notebook now contains 164 cells, still 47 code cells. The approved episode thumbnail and author credit precede START HERE. Code, outputs and execution counts are unchanged; notebook schema validation passed. The cover uses the verified public PNG pinned to asset revision 8d07f00. This markdown-only change does not require repeating the scientific runtime tests.
