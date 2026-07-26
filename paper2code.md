# paper2code

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
The rest of the README remains unchanged from the original repository.
---

**Open Arsenal Hub**  
[https://gitlab.com/Roxanne_Ardary/open-arsenal-specs](https://gitlab.com/Roxanne_Ardary/open-arsenal-specs)
