# PHITrack
**AI watches. Humans decide.**

PHITrack is an open-source platform for monitoring, analyzing, and visualizing PHI (Protected Health Information) transmissions using AI-driven insights while ensuring human-in-the-loop oversight. The platform is fully HIPAA-safe by using only synthetic or anonymized data. PHITrack provides actionable reports, dashboards, and compliance analytics for healthcare systems.

---

## Features

- **AI-Powered Security Analysis**
  - Crawls system metadata and synthetic logs to detect potential PHI leaks
  - Classifies transmission events by type (email, API, fax, USB)
  - Predictive risk scoring for high-risk systems or users
  - Anomaly detection to identify unusual access patterns
  - Automated HIPAA compliance checks

- **Dashboards & Reporting**
  - Interactive dashboards with drill-down capability
  - Trend graphs and heatmaps showing PHI transmissions over time
  - Exportable reports in PDF, CSV, or JSON formats
  - Alerts for high-risk patterns or repeated incidents

- **Human-in-the-Loop**
  - AI suggests potential violations or risks, humans make final decisions
  - Annotation system for human verification of flagged events
  - Full audit trail of human decisions for compliance and training

- **Synthetic PHI Dataset Generation**
  - Creates realistic synthetic PHI for testing and demonstrations
  - Ensures no real patient data is used
  - Supports anomaly detection and AI training

- **Training & Educational Tools**
  - Gamified breach simulation scenarios
  - Library of HIPAA violation examples (synthetic)
  - Tutorials and best practices for PHI handling and compliance

- **Extensibility**
  - Plugin architecture for new analysis modules or visualizations
  - Secure API access for external dashboards or compliance tools
  - Open-source contributor ecosystem tracked via notice.md

---

## Installation & Setup

1. Clone the repository using GitLab.  
   - Example: `git clone https://gitlab.com/Roxanne_Ardary/PHITrack`  

2. Navigate to the `src/` folder to access AI modules and dashboards.

3. Use synthetic datasets located in `data/synthetic/` to test the system without using real PHI.

4. For integration or API usage, review the instructions in `docs/Workflow.md`.  
   - Example: API endpoints return anonymized event counts, statistics, and risk alerts.

---

## Usage

- **Monitoring**: Load synthetic logs into the ingestion module. The AI will classify events, score risks, and generate alerts.  
- **Reporting**: Use the dashboard module to visualize PHI transmission trends and export reports.  
- **Training**: Simulate breaches using the `training/scenario_sim/` folder and test responses.  

**Example without code blocks**:  
- To generate a synthetic dataset, run the Python script `generate_synthetic.py` from the command line by typing `python generate_synthetic.py`. Output will appear in the `data/synthetic/` folder.

- To view dashboard analytics, open the HTML or web interface located in `src/dashboard/interactive/` and load the synthetic datasets.

---

## Compliance & Safety

- **No real PHI is ever stored or processed**  
- **All examples are synthetic or anonymized**  
- **Human-in-the-loop ensures final decisions** for reporting or alerts  
- Fully AGPL 3.0+ licensed with attribution to **Roxanne Ardary, [roxanneardary.com](https://www.roxanneardary.com/)**  

---

## Contribution

All contributions must follow the **notice.md** template:  
- Name of contributor  
- Website or GitLab/Codeberg link  
- Date of contribution  
- One-sentence description of contribution  

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
  - [https://roxanneardary.com/phitrack/](https://roxanneardary.com/phitrack/)

---

## License & Notice Requirements

PHITrack is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- PHITrack specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`.  
- When submitting a pull request, ensure that any new files maintain the attribution requirements where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
