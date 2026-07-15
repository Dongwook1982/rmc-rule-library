# RMC Rule Library — JSON-LD & SHACL

> **Companion repository for:**  
> Kim, D.-W. (2026). "Development and Field Application of a Rule-Based BIM Model Checker for Automated Quality Control in Road Infrastructure." *Journal of Computing in Civil Engineering*, ASCE. (under review)

---

## Overview

This repository contains the complete rule library (68 rules) implemented in the Rule-Based Model Checker (RMC) framework described in the paper above. Rules encode quality requirements derived from:

- **KDS 24 14 21** — Korean Design Standard for Road Bridges and Culverts (MOLIT 2021)  
- **ISO 19650-1:2018** — BIM Information Management, Concepts and Principles

Each rule is provided in two complementary formats:

| Format | Purpose | Location |
|--------|---------|----------|
| **JSON-LD** | Human-readable rule definition with regulatory traceability | `rules/` |
| **SHACL** | Machine-executable constraint for semantic reasoning engine | `shacl/` |

---

## Rule Categories

| Category | Count | Source Standard | Folder |
|----------|-------|-----------------|--------|
| Dimensional Tolerances | 28 | KDS 24 14 21 §4 | `rules/dimensional/` |
| Material Compliance | 15 | KDS 24 14 21 §5, §6 | `rules/material/` |
| Regulatory Requirements | 25 | KDS 24 14 21, ISO 19650-1 | `rules/regulatory/` |
| **Total** | **68** | | |

> **Note:** 3 additional rules (DIM-026, DIM-027, DIM-028) were reviewed but deferred due to unresolvable regulatory ambiguity ("as approved by the engineer"). Their draft definitions are provided in `docs/deferred_rules.md`.

---

## Rule ID Convention

```
[CATEGORY]-[###]
│            └── Sequential number within category
└── DIM = Dimensional | MAT = Material | REG = Regulatory
```

---

## Repository Structure

```
rmc-rule-library/
├── README.md
├── rules/
│   ├── dimensional/          # DIM-001 to DIM-025 (JSON-LD)
│   ├── material/             # MAT-001 to MAT-015 (JSON-LD)
│   └── regulatory/           # REG-001 to REG-025 (JSON-LD)
├── shacl/
│   ├── dimensional_shapes.ttl
│   ├── material_shapes.ttl
│   └── regulatory_shapes.ttl
├── examples/
│   ├── sample_ifc_element.json
│   └── sample_validation_output.json
└── docs/
    ├── rule_traceability_matrix.md
    └── deferred_rules.md
```

---

## Software Stack

| Component | Library | Version |
|-----------|---------|---------|
| IFC parsing | IfcOpenShell | 0.7.0 |
| SPARQL triplestore | Apache Jena Fuseki | 4.9 |
| SHACL execution | PySHACL | 0.23 |
| Point cloud processing | Open3D | 0.17 |
| Language | Python | 3.10 |

---

## Usage

### 1. Run SHACL validation (PySHACL)

```python
from pyshacl import validate
import rdflib

# Load IFC-derived RDF graph (output of IfcOpenShell + ifcOWL conversion)
data_graph = rdflib.Graph()
data_graph.parse("your_ifc_model.ttl", format="turtle")

# Load SHACL shapes
shapes_graph = rdflib.Graph()
shapes_graph.parse("shacl/dimensional_shapes.ttl", format="turtle")

# Validate
conforms, results_graph, results_text = validate(
    data_graph,
    shacl_graph=shapes_graph,
    inference="rdfs",
    abort_on_first=False,
    meta_shacl=False,
    debug=False,
)

print(f"Conforms: {conforms}")
print(results_text)
```

### 2. Load a JSON-LD rule definition

```python
import json

with open("rules/dimensional/DIM-001.json", "r", encoding="utf-8") as f:
    rule = json.load(f)

print(f"Rule ID   : {rule['ruleId']}")
print(f"Severity  : {rule['severity']}")
print(f"Tolerance : ±{rule['parameter']['toleranceMm']} mm")
print(f"Source    : {rule['sourceClause']}")
```

---

## Citation

If you use this rule library in your research, please cite:

```bibtex
@article{kim2026rmc,
  author  = {Kim, Dong-Wook},
  title   = {Development and Field Application of a Rule-Based BIM Model Checker
             for Automated Quality Control in Road Infrastructure},
  journal = {Journal of Computing in Civil Engineering},
  year    = {2026},
  publisher = {ASCE},
  note    = {Under review}
}
```

---

## Data Availability

The **rule library** (this repository) is publicly available and freely reusable under the MIT License.

The **raw project datasets** (BIM models and TLS point clouds from the Yangpyeong–Icheon Section 4 Expressway) are proprietary assets of the project owner (DL E&C Co., Ltd.) and cannot be released due to contractual confidentiality obligations. Researchers wishing to replicate the study should apply the rule library to a comparable PSC bridge project dataset.

---

## License

MIT License — see `LICENSE` for details.

## Contact

Dong-Wook Kim  
Civil Smart Engineering Team, Civil Engineering Division  
DL E&C Co., Ltd., Seoul, Republic of Korea  
ORCID: [0000-0002-0721-5114](https://orcid.org/0000-0002-0721-5114)  
Email: clearup7@nate.com
