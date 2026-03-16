# Restoration-Digital-Logbook

# Restoration Logbook Semantic Dataset

## Overview

This repository contains a structured dataset of restoration interventions extracted from restoration logbooks documented in the Italian SICaR system.
The original textual reports have been semantically structured according to the controlled vocabulary and ontology proposed in this study.

Each record corresponds to a single restoration intervention and includes both contextual metadata (site, author, date) and semantic annotations derived from the controlled restoration vocabulary.

The dataset is intended to support research on:

- information extraction from restoration documentation
- ontology-driven metadata structuring
- evaluation of large language models (LLMs) in cultural heritage contexts
- semantic standardization of restoration reports

---

## Dataset Statistics

- **Restoration sites:** 82
- **Total intervention records:** 1063
- **Language:** Italian
- **Format:** JSON

---

## Data Model

Each JSON record includes the following fields:

| Field         | Description                                      |
| ------------- | ------------------------------------------------ |
| `record_id` | Identifier of the intervention (SICaR system)    |
| `cantiere`  | Restoration site                                 |
| `soggetto`  | Restoration subject (when available)             |
| `date`      | Date of the intervention                         |
| `author`    | Author of the restoration logbook entry          |
| `text`      | Original textual description of the intervention |

Additionally, each record contains semantic metadata derived from the controlled vocabulary:

| Ontology Field          | Description                                         |
| ----------------------- | --------------------------------------------------- |
| `materials_used`      | Materials mentioned in the intervention             |
| `technique_used`      | Restoration techniques applied                      |
| `environmental_issue` | Environmental conditions affecting the intervention |
| `working_issue`       | Operational or structural issues encountered        |
| `zone`                | Architectural area where the intervention occurred  |
| `support_type`        | Structural support type of the artifact             |

These fields follow the controlled vocabulary defined in the repository.

---


## Reproducibility and Evaluation

The repository also contains the outputs of the evaluation pipeline used in the associated study.
These files compare the ground-truth annotations with the metadata automatically extracted by the language model.

The evaluation results include:

- global performance metrics
- per-label precision, recall, and F1 scores
- confusion matrices for single-label fields
- error analysis for multilabel predictions

The reported evaluation metrics include:

- Micro Precision
- Micro Recall
- Micro F1-score
- Balanced Accuracy
- Matthews Correlation Coefficient (MCC)
- Exact Match Ratio (subset accuracy)

For the single-label field `support_type`, performance is evaluated using standard multiclass metrics including accuracy and macro-averaged precision, recall, and F1-score.

---

## Intended Use

This dataset is intended to support research on:

- semantic structuring of restoration documentation
- ontology-driven annotation of cultural heritage reports
- information extraction from restoration logbooks
- evaluation of large language models in the cultural heritage domain

The dataset may also support studies in digital humanities, knowledge representation, and documentation standardization.

---

## License

This dataset is released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

You are free to share and adapt the dataset provided that appropriate credit is given to the authors.

---

## Citation

If you use this dataset in your research, please cite the associated publication describing the ontology and the extraction methodology.

A suggested citation format will be provided upon publication of the dataset on Zenodo.

---

## Contact

For questions regarding the dataset or its structure, please contact the authors of the associated publication (under review).
