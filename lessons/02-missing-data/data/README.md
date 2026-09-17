# Framingham teaching CSV

Companion dataset for EvidenceLab Lesson 02. [Download CSV](https://raw.githubusercontent.com/amobionovo/EvidenceLab/main/lessons/02-missing-data/data/framingham.csv).

- 4,240 rows; 16 columns.
- 388 glucose values missing (9.15%).
- SHA-256: `412c9ea5f0dfb7ad243dfcd1f2b4df500101904a8f443a22f3080394391853e9`.
- Source: the lesson owner's supplied `framingham.csv`, published without altering its bytes.
- Parsed column names and every row were verified equal to the [previously used pinned teaching mirror](https://raw.githubusercontent.com/GauravPadawe/Framingham-Heart-Study/43cda49873de043c4f155e7cde17d6be9a196d0a/framingham.csv); file bytes differ because of file formatting.
- This is a cardiovascular-risk teaching copy, not the full original Framingham Heart Study. Neither its missing percentage nor observed-data diagnostics establish the missingness mechanism.
- This third-party dataset is not relicensed under EvidenceLab's code or educational-material licenses. Upstream rights and source terms remain applicable; no additional dataset license is asserted here.

The notebook checks the repository download against the SHA-256 above. Colab downloads it automatically with the default settings. Local runs can use this file in `data/framingham.csv` relative to the notebook working directory. To use another compatible file, enable `USE_UPLOAD` in Colab.
