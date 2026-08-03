# paper2code

## Overview

The Paper2Code Specification defines an open, modular framework for transforming academic research, technical documentation, and knowledge sources into verified, reproducible, and maintainable software implementations.

The specification enables AI-assisted development systems to analyze research materials, generate implementation plans, produce structured codebases, and maintain traceability between source knowledge and generated software.

The specification is designed around a modular architecture. Core capabilities provide the foundation required for compliant implementations, while optional plugin modules allow organizations, researchers, and developers to extend functionality for specialized workflows.

---

# Modular Architecture

Paper2Code implementations are divided into:

- Core Modules
  - Required functionality that defines the base specification.
  - Must be implemented by compliant systems.

- Plugin Modules
  - Optional extensions that add specialized capabilities.
  - Can be independently developed, distributed, and integrated.

---

# Core Modules

## 1. Research Document Processing Module

Provides the foundation for ingesting and understanding research materials.

Features:

- Academic paper ingestion
- Technical document parsing
- PDF and LaTeX processing
- Section and reference extraction
- Figure and table analysis
- Appendix extraction
- Citation tracking

---

## 2. Knowledge Extraction Module

Converts research content into structured technical knowledge.

Features:

- Methodology extraction
- Algorithm identification
- Architecture discovery
- Dataset identification
- Parameter extraction
- Equation interpretation
- Implementation requirement mapping

---

## 3. Citation Anchoring Module

Maintains traceability between generated implementations and source material.

Features:

- Code-to-paper references
- Section-level citations
- Equation references
- Design decision tracking
- Source provenance records

---

## 4. Ambiguity Analysis Module

Identifies incomplete or unclear implementation details.

Features:

- Specification completeness analysis
- Missing parameter detection
- Contradiction detection
- Uncertainty classification:

  - SPECIFIED
  - PARTIALLY_SPECIFIED
  - UNSPECIFIED

- Alternative implementation suggestions

---

## 5. Code Generation Module

Creates structured, maintainable software implementations.

Features:

- Project scaffolding
- Source code generation
- Configuration generation
- Dependency management
- Documentation generation
- Framework-specific implementation support

Supported targets may include:

- Python
- JavaScript
- Rust
- C/C++
- Machine learning frameworks
- Data processing frameworks

---

## 6. Reproducibility Module

Ensures generated implementations can be tested and recreated.

Features:

- Environment configuration
- Dependency locking
- Experiment configuration
- Dataset references
- Training configuration
- Evaluation workflows

---

## 7. Human-in-the-Loop Control Module

Provides human oversight throughout the generation process.

Features:

- Interactive implementation review
- Architecture approval workflows
- Manual ambiguity resolution
- Generation checkpoints
- Code review approval
- Experiment configuration approval

---

## 8. Verification and Validation Module

Evaluates generated implementations.

Features:

- Automated testing
- Paper-to-code consistency checks
- Runtime validation
- Performance comparisons
- Regression testing
- Implementation deviation reports

---

# Optional Plugin Modules

## 1. Dataset Intelligence Plugin

Adds advanced dataset discovery and preparation.

Features:

- Automatic dataset retrieval
- Dataset validation
- Preprocessing generation
- Data quality analysis

---

## 2. Multi-Paper Research Plugin

Enables combining knowledge from multiple publications.

Features:

- Literature comparison
- Cross-paper architecture analysis
- Hybrid implementation generation
- Research trend discovery

---

## 3. Experiment Optimization Plugin

Provides automated experiment improvement.

Features:

- Hyperparameter optimization
- Experiment scheduling
- Benchmark comparison
- Performance tuning

---

## 4. Deployment Automation Plugin

Extends generated projects into production systems.

Features:

- Docker generation
- Kubernetes deployment
- API generation
- Cloud deployment templates
- Edge deployment support

---

## 5. Framework Translation Plugin

Converts implementations between ecosystems.

Features:

- PyTorch conversion
- TensorFlow conversion
- JAX conversion
- ONNX export
- Hardware accelerator optimization

---

## 6. Research Monitoring Plugin

Tracks new developments after implementation.

Features:

- Literature monitoring
- Related paper discovery
- Implementation update suggestions
- Version comparison

---

## 7. Collaboration Plugin

Supports community development.

Features:

- Contribution workflows
- Review systems
- Shared implementation libraries
- Research project management

---

## 8. Explainability Plugin

Provides deeper understanding of generated systems.

Features:

- Architecture explanations
- Decision history
- Model behavior analysis
- Implementation rationale reports

---

# Compliance Requirements

A Paper2Code Specification implementation must:

- Maintain modular architecture principles.
- Preserve traceability between source material and generated output.
- Provide transparency regarding uncertainty and assumptions.
- Support human review of critical implementation decisions.
- Maintain reproducible development workflows.

---

> arxiv URL in → citation-anchored implementation out

    ┌─────────────────────────────┐         ┌──────────────────────────────────────┐
    │                             │         │  {paper_slug}/                       │
    │  /paper2code                │         │  ├── README.md                       │
    │  https://arxiv.org/abs/     │  ───▶   │  ├── REPRODUCTION_NOTES.md          │
    │  1706.03762                 │         │  ├── requirements.txt               │
    │                             │         │  ├── src/                            │
    │                             │         │  │   ├── model.py     # §3.2 cited  │
    │                             │         │  │   ├── loss.py      # §3.4 cited  │
    │                             │         │  │   ├── train.py     # §4.1 cited  │
    │                             │         │  │   ├── data.py                    │
    │                             │         │  │   ├── evaluate.py                │
    │                             │         │  │   └── utils.py                   │
    │                             │         │  ├── configs/                        │
    │                             │         │  │   └── base.yaml   # all params   │
    │                             │         │  └── notebooks/                      │
    │                             │         │      └── walkthrough.ipynb           │
    └─────────────────────────────┘         └──────────────────────────────────────┘

[placeholder: animated GIF showing the full pipeline — paper fetch → parsing → ambiguity audit → code generation → walkthrough notebook]

---

## Why this exists

The problem: ML papers are vague. Critical hyperparameters are buried in appendices or omitted entirely. Prose contradicts equations. "Standard settings" refers to nothing specific. When you implement a paper, you spend more time detective-working than coding.

What LLMs get wrong: Naive code generation fills in every gap silently and confidently. You get something that runs but doesn't match the paper. Worse, you can't tell which parts are from the paper and which were invented by the model.

What paper2code does differently:

1. Citation anchoring — every line of generated code references the exact paper section and equation it implements (`§3.2, Eq. 4`)  
2. Ambiguity auditing — before writing a single line of code, every implementation choice is classified as `SPECIFIED`, `PARTIALLY_SPECIFIED`, or `UNSPECIFIED`  
3. Honest uncertainty — unspecified choices are flagged with `[UNSPECIFIED]` comments at the exact line where the choice is made, with common alternatives listed  
4. Appendix mining — appendices, footnotes, and figure captions are treated as first-class sources, not ignored  

The result: code you can trust because you can verify every decision against the paper.

---

## Human-in-the-loop Enhancements *(Contributed by Roxanne Ardary, [roxanneardary.com](https://www.roxanneardary.com/))*

These additions allow humans to guide and verify every critical decision in code generation:

- **Interactive code refinement** — approve or modify model architecture, hyperparameters, and pipeline design before final generation  
- **Ambiguity resolution interface** — highlight underspecified paper sections and make manual decisions  
- **Code review assistant** — detect potential runtime issues or logical inconsistencies before committing code  
- **Stepwise generation checkpoints** — approve each phase of code generation: data prep → model → training → evaluation → deployment  
- **Interactive experiment configuration** — configure datasets, training parameters, and experiments to ensure reproducibility  

These features ensure **trustworthy, verifiable, and reproducible code** while keeping a human in control of all final decisions.  

---

## Specification Branding License (SBL)

### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/paper2code/](https://roxanneardary.com/paper2code/)

---

## License & Notice Requirements

paper2code is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- paper2code specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.

## Original Repository

For the original repository and credit to the original author: [PrathamLearnsToCode/paper2code](https://github.com/PrathamLearnsToCode/paper2code)

---

## Install

    npx skills add PrathamLearnsToCode/paper2code/skills/paper2code

You'll be prompted to:

1. Select agents — pick the coding agents you want to use this skill with (e.g., Claude Code)  
2. Choose scope — Global or per-agent  
3. Choose method — Symlink (recommended) or copy
Once installed, open your agent and run the skill 

---
**Open Arsenal Hub**  
[https://gitlab.com/Roxanne_Ardary/open-arsenal-specs](https://gitlab.com/Roxanne_Ardary/open-arsenal-specs)
