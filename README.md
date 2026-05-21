# Repository Selection Decision Tree

An interactive, self-contained decision tree to help researchers select the most appropriate repository for sharing their research data, developed as part of the **NIH Data Management and Sharing Plan (DMSP) Guidance Working Group** project.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20317424.svg)](https://doi.org/10.5281/zenodo.20317424)
[![CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

---

## 🔗 Try it

👉 **[Launch the tool](https://seykim10.github.io/repository-decision-tree)**

No installation, login, or internet connection required. Just click and use in any web browser.

---

## About

This tool guides researchers and research support staff through a structured, step-by-step process for selecting the most appropriate repository for their data. It checks funder mandates and domain-specific repositories first, then institutional options, before recommending from the GREI generalist repositories.

It combines two complementary frameworks:

1. **A 5-step NIH DMSP repository selection framework** ([Becker Medical Library framework](https://wustl.app.box.com/file/1676763033526?s=tr2zehvskpx6s3i27pm9ueb55qaoktvy)) developed at the Bernard Becker Medical Library, Washington University School of Medicine in St. Louis, which prioritizes:
   - Funder/FOA/NOFO-mandated repositories
   - Model organism-specific repositories
   - Disease- or organ-specific repositories
   - Data type- or method-specific repositories
   - NIH IC-specific central repositories
   - Institutional repositories

2. **The GREI Repository Selection Flowchart** (Barbosa et al., 2024; [doi:10.5281/zenodo.11105430](https://doi.org/10.5281/zenodo.11105430)), which guides selection among the seven NIH GREI generalist repositories: Dataverse, Dryad, Figshare, Mendeley Data, OSF, Vivli, and Zenodo.

### Decision points covered

- Funding Opportunity Announcement (FOA) / Notice of Funding Opportunity (NOFO) mandates
- Model organism-specific repository availability
- Disease- or organ-specific repository availability
- Data type- or method-specific repository availability (imaging, genomics, proteomics, metabolomics, qualitative data, and more)
- NIH IC-specific central repository availability
- Institutional repository availability
- Human subjects data, PHI/PII, and managed access requirements
- Dataset size (under 50 GB / 50–300 GB / over 300 GB)
- Software and code outputs
- Data curation needs
- Licensing requirements
- Project management needs

---

## How to use

**Option 1 — Live web version (recommended):**
Click the [launch link](https://seykim10.github.io/repository-decision-tree) above. Works in any modern browser.

**Option 2 — Download and run locally:**
1. Download `index.html` from this repository
2. Open the file in any web browser (Chrome, Firefox, Safari, Edge)
3. No internet connection required after download

> **Note:** The "We welcome feedback" and "Share your feedback" mailto links require the tool to be served from a web server (e.g., the live GitHub Pages link above) to function. They will not open in Chrome when the file is opened locally.

---

## Source documents

This tool was built using the following source materials:

- Barbosa, S., et al. (2024). *GREI Repository Selection Flowchart* (v1). Zenodo. <https://doi.org/10.5281/zenodo.11105430>
- Becker Medical Library 5-step NIH DMSP repository selection framework: <https://wustl.app.box.com/file/1676763033526?s=tr2zehvskpx6s3i27pm9ueb55qaoktvy>
- NIH repository selection guidance: <https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/accessing-data/scientific>
- NIH Genomic Data Sharing (GDS) Policy — Where to Submit: <https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/gds/where-to-submit>
- NIH Controlled Access Data Repositories (CADRs): <https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/accessing-data/requirements>
- NIH-Supported Scientific Data Repositories: <https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/accessing-data/scientific#nih-supported-scientific-data-repositories*>
- BMIC List of Domain-Specific Repositories: <https://www.nlm.nih.gov/NIHbmic/nih_data_sharing_repositories.html>
- BMIC List of Generalist Repositories: <https://www.nlm.nih.gov/NIHbmic/generalist_repositories.html>
- NNLM Data Repository Finder: <https://www.nnlm.gov/resources/finder>
- NICHD Data Repository Finder: <https://data-repository-finder.ll.mit.edu/>
- re3data.org — Registry of Research Data Repositories: <https://www.re3data.org>
- GREI Repository Comparison Chart: <https://zenodo.org/records/17315963>

---

## Development

This tool was developed by Seonyoung Kim using AI-assisted coding (Claude, Anthropic) with iterative refinement based on the source documents listed above. The decision logic, repository descriptions, and content were reviewed and validated by Seonyoung Kim, Senior Support Scientist at the Bernard Becker Medical Library and a member of the NIH DMSP Guidance Working Group.

The tool is built as a single, self-contained HTML file using standard HTML, CSS, and JavaScript — no external frameworks or server required.

---

## Feedback

Feedback on this tool is welcome via the **💬 Share your feedback** link built into every page of the tool, or through the channels below:

- **Open an issue** on this GitHub repository
- **Contact:** Seonyoung Kim | seonyoung.kim@wustl.edu | Bernard Becker Medical Library, Washington University School of Medicine in St. Louis

---

## Credits

**Developed by:** [Seonyoung Kim](https://orcid.org/0000-0002-8854-287X), Bernard Becker Medical Library, Washington University School of Medicine in St. Louis

**Working Group:** NIH DMSP Guidance Working Group

**Content feedback (v0.2.0):** Christine Nieman Hislop, University of Maryland; Marla Hertz, University of Alabama at Birmingham

**Accessibility review (v0.3.0):** Christine Nieman Hislop, University of Maryland (using the [WAVE Evaluation Tool](https://wave.webaim.org/))

**Based on:** Barbosa et al. (2024) GREI Repository Selection Flowchart, the Becker Medical Library 5-step NIH DMSP repository selection framework, and NIH DMSP repository selection guidance

---

## Citation

If you use this tool, please cite it as:

> Kim, S. (2026). *Repository Selection Decision Tree* (v0.3.0). Zenodo. https://doi.org/10.5281/zenodo.20317424

Or use the `CITATION.cff` file in this repository for formatted citations in your reference manager.

---

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0).

You are free to share and adapt this tool for any purpose, provided appropriate credit is given.

[![CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
