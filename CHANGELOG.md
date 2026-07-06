# Changelog — Repository Selection Decision Tree

All notable changes to this tool are documented here.  
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

> **Note on versioning:** Development versions 0.1.0–0.3.0 were published by replacing `index.html` directly on GitHub. The first tagged GitHub/Zenodo releases were **v1.0.0** and **v1.0.1** (metadata-only: added the Zenodo DOI to `README.md` and `CITATION.cff`), both corresponding to the 0.3.0 tool content. **v1.1.0** is the first tagged release to add new tool functionality.

---

## [1.1.0] — 2026-07-06

A feature release adding a dedicated genomic-data decision branch, official NIH repository lists, visual decision-node icons, and a round of accessibility improvements. Backward-compatible: no existing question, route, or recommendation was removed or changed in meaning.

### Added — Genomic data decision branch
Based on input from **Seonyoung Kim**, drawing on the NIH Genomic Data Sharing (GDS) Policy and the FASEB DataWorks! repository-selection framework:

- New **Step 4 — Genomic data** decision node ("Does your project generate genomic data?"). Answering **No** continues to the data-type step; answering **Yes** proceeds to a human/non-human sub-question.
- New **Step 4a — Human genomic data** sub-question routing to human vs. non-human genomic results.
- **Human genomic result** lists the full set of NIH-designated human genomic repositories from [Where to Submit Genomic Data](https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/gds/where-to-submit) (AnVIL, ArrayExpress, BioData Catalyst, dbGaP [controlled access], dbSNP, dbVar, DDBJ, ENA, GenBank, GEO, NCI Genomic Data Commons, NCI FireCloud, NCI ISB Cancer Genomics Cloud, NCI Seven Bridges, NIMH Data Archive, NIAGADS, SRA). The green summary box explains GDS applicability and the plan → Institutional Certification → dbGaP registration → submit workflow, linking to the GDS Policy [applicability](https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/gds/overview#applicability) and [planning/submitting/accessing](https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/gds/overview#planning,-submitting,-and-accessing-genomic-data) sections and [IC-specific expectations](https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/gds/expectations-by-ics).
- **Non-human genomic result** lists the full non-human genomic repository set (ArrayExpress, DDBJ, ENA, FlyBase, GenBank, GEO, IRD, MGI, RGD, SRA, WormBase, Xenbase, ZFIN), notes that GDS applicability should be checked, links to the [non-human genomic submission guidance](https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/gds/where-to-submit#submitting-non-human-genomic-data), and points to the NLM [Submission Portal](https://submit.ncbi.nlm.nih.gov/).
- Removed **Bionimbus** from the human genomic list — the site is unreachable and its function is superseded by the NCI Genomic Data Commons and NCI Cloud Resources already listed.

### Added — Visual and navigational improvements
- **Decision-node icons** on every step eyebrow (⚠️ funder, 🏛️ domain, 🧬 genomic, 🗂️ data type, 🏢 institutional, 🔒 sensitive data, 📊 size, 💻 software, 📋 curation, 📄 license) and a ✅ on each recommendation, so questions are visually distinguishable from results.
- **FAIRsharing.org** added to the Additional Tools & Resources panel (after re3data.org).

### Changed — Data-type step (now Step 5)
- Reorganized the data-type-specific step and its result into scannable categories: 🔬 Imaging, 🧪 Omics, 🩸 Flow cytometry, 👤 Human research, and 💻 Software & code.
- The result's summary box now notes it is not possible to list every repository and directs users to search by keyword in [re3data.org](https://www.re3data.org/) or [FAIRsharing.org](https://fairsharing.org/databases).
- Expanded the **Software & code** guidance to explain that hosting code on GitHub and connecting it to Zenodo automatically archives each tagged release with a citable DOI; the data-type result now includes a Software & code category with links to GitHub and a step-by-step guide for archiving a GitHub repository with Zenodo.
- Removed EMDB from the Omics examples; genomic repositories (dbGaP, GEO) moved out of the data-type examples into the new genomic branch.

### Changed — Attribution and citations
- Synced the sources listed in the intro header and the footer/result citations: GREI Repository Selection Flowchart, Becker Medical Library 5-step NIH DMSP repository selection framework, NIH repository selection guidance, and NIH Genomic Data Sharing (GDS) Policy.
- Hyperlinked "NIH Scientific Data Repositories list" in the IC-specific result to the [NIH-supported repositories list](https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/accessing-data/scientific#nih-supported-scientific-data-repositories*).
- Updated all GREI Repository Selection Flowchart references to the concept (all-versions) DOI [10.5281/zenodo.11105429](https://doi.org/10.5281/zenodo.11105429).
- Total step count increased 12 → 13; downstream steps renumbered (data-type 5, IC-specific 6, institutional 7, human subjects 8/8a/8b/8c, size 9, software 10, curation 11, license 12, project management 13). No downstream question, route, or recommendation content changed.

### Accessibility
- **Focus management:** after each answer, keyboard/screen-reader focus moves to the new question or result heading (skipped on initial load so the intro is read first).
- **Progress bar** now exposes `role="progressbar"` with `aria-valuemin/max/now`, updated as the user advances.
- Added `rel="noopener noreferrer"` to all external `target="_blank"` links.
- Marked decorative icons (step-eyebrow icons, Yes/No badges) `aria-hidden="true"` so screen readers announce only the meaningful label.

---

## [1.0.1] — 2026-05-21

### Changed
- Added the Zenodo DOI to `README.md` (DOI badge) and `CITATION.cff`. Metadata only; no change to the tool. Corresponds to the 0.3.0 tool content.

## [1.0.0] — 2026-05-20

### Added
- First tagged GitHub release and Zenodo archive of the tool (0.3.0 content). Concept DOI [10.5281/zenodo.20317424](https://doi.org/10.5281/zenodo.20317424) always resolves to the latest version.

---

## [0.3.0] — 2026-05-20

### Accessibility improvements
Based on an accessibility review of the tool by **Christine Nieman Hislop** (University of Maryland) using the [WAVE Evaluation Tool](https://wave.webaim.org/):

- Increased question title (`step-q`) font size from 18px → 22px (desktop) and 16px → 19px (mobile) to meet accessibility minimums — identified as the most critical issue
- Improved text contrast throughout: footer, citation, progress label, and "Also consider" section labels darkened from gray-400 (#9e9b94) to gray-600 (#6b6860) to better meet WCAG AA contrast standards
- Added semantic heading hierarchy: step questions and result titles now rendered as `<h2>` elements; "Additional Tools & Resources for Finding a Repository" section title changed from `<div>` to `<h2>`
- Fixed outdated OSF project link in footer (updated from osf.io/uadxr to osf.io/d8kzu/overview)

### Content updates
Based on input from **Seonyoung Kim**:

- Added new resource to the Additional Tools & Resources panel: **NIH — Where to Submit Genomic Data**, per the NIH Genomic Data Sharing (GDS) Policy; positioned second in the panel, directly below NIH-Supported Scientific Data Repositories
- Added attribution to footer: "Developed by Seonyoung Kim at the Bernard Becker Medical Library, Washington University School of Medicine in St. Louis, as part of the NIH DMSP Guidance Working Group project"
- Added **"💬 We welcome feedback on this tool"** mailto link in the intro card, pre-addressed to seonyoung.kim@wustl.edu with subject "Repository Selection Tool Feedback"; styled as a pill-shaped button. Note: requires the tool to be served from a web server (e.g., GitHub Pages) to function — mailto links are blocked by Chrome when the HTML file is opened locally as a file
- Added **"💬 Share your feedback"** mailto link in a feedback bar rendered at the bottom of every question and result page; subject line dynamically includes the current step or result, so feedback can be traced to a specific point in the tool
- Added [Becker Medical Library 5-step NIH DMSP repository selection framework](https://wustl.app.box.com/file/1676763033526?s=tr2zehvskpx6s3i27pm9ueb55qaoktvy) as a credited source in both the site footer and the citation line at the bottom of each result card
- Hyperlinked "Seonyoung Kim" in the footer to ORCID profile (https://orcid.org/0000-0002-8854-287X), opening in a new tab

---

## [0.2.0] — 2026-05-18

### Changes

Based on a written revision request from **Seonyoung Kim**, incorporating feedback from two members of the NIH DMSP Guidance Working Group — **Christine Nieman Hislop** (University of Maryland) and **Marla Hertz** (University of Alabama at Birmingham):

**Requested by Seonyoung Kim (with input from Christine Nieman Hislop and Marla Hertz):**
- Added hyperlink (doi.org/10.17605/OSF.IO/D8KZU) to "NIH DMSP Guidance Working Group" in the header and to "View project on OSF" button
- Added "Start Over" button alongside the Back button during question navigation
- Added "Keywords:" label before topic chips in the intro section to reduce confusion
- Made intro paragraph links open in a new tab
- Made all repository example chips (Steps 2–5) clickable links to re3data.org records or direct repository URLs, opening in a new tab
- Added repositories to example chips: Alliance of Genome Resources (Step 2); ADNI Image and Data Archive (Step 3); BioImage Archive (Step 4)
- Corrected Step 3 disease/organ-specific repository examples to TCIA, AD Knowledge Portal, ADNI, and FITBIR only, per the [Becker Medical Library 5-step framework](https://wustl.app.box.com/s/tr2zehvskpx6s3i27pm9ueb55qaoktvy)
- Made IC-specific repository chips (Step 5) clickable, linking to re3data.org records; replaced NCI CRDC with NIA NACC
- Step 7 sub-steps relabeled as 7a, 7b, 7c for clarity
- Removed re3data.org link from "Your institutional repository" recommended card
- Expanded "Also consider" list in institutional repository result to include all 6 GREI generalist repositories
- Result note box moved above "Also consider" section and styled in light pink for visual distinction
- "View project on OSF" button updated to link to osf.io/d8kzu/overview

**Bug fixes (identified during testing):**
- Fixed three incorrect URLs in the Additional Tools & Resources panel: NNLM Data Repository Finder, NICHD Data Repository Finder, and GREI Repositories Comparison Chart
- Fixed JavaScript syntax error (unescaped apostrophe in "Alzheimer's" within a single-quoted JS string) that prevented the tool from loading
- Fixed nested template literal in domain chip renderer that caused JavaScript parse errors

---

## [0.1.0] — 2026-04-27

### Initial release
Developed by **Seonyoung Kim** (Bernard Becker Medical Library, Washington University School of Medicine in St. Louis) using AI-assisted coding (Claude, Anthropic), based on:

- The [GREI Repository Selection Flowchart](https://doi.org/10.5281/zenodo.11105429) (Barbosa et al., 2024)
- The [Bernard Becker Medical Library 5-step NIH DMSP repository selection framework](https://wustl.app.box.com/s/tr2zehvskpx6s3i27pm9ueb55qaoktvy)
- [NIH repository selection guidance](https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/accessing-data/scientific)

**Features:**
- 12-step interactive decision tree following NIH DMSP guidance framework, checking funder mandates and domain-specific repositories first, then institutional options, before recommending GREI generalist repositories
- Covers 7 GREI generalist repositories: Dataverse, Dryad, Figshare, Mendeley Data, OSF, Vivli, Zenodo
- Domain-specific repository examples for Steps 2–5 (organism-specific, disease/organ-specific, data type-specific, IC-specific)
- Human subjects data branch covering managed access, clinical/biomedical routing to Vivli, and de-identification check
- Dataset size branching: under 50 GB / 50–300 GB / over 300 GB
- Breadcrumb trail and progress bar
- Back navigation and Start Over button on result pages
- Additional Tools & Resources panel with curated links
- "View project on OSF" button linking to the NIH DMSP Guidance Working Group OSF project
- Fully self-contained single HTML file — no server, login, or internet connection required after download
- NIH blue color scheme; no institutional branding
- Shared via NIH DMSP Guidance Working Group OSF project: https://osf.io/d8kzu/overview

---

## Contributors
- **Seonyoung Kim** — Bernard Becker Medical Library, Washington University School of Medicine in St. Louis (lead developer)
- **NIH DMSP Guidance Working Group** — content review
- **Christine Nieman Hislop** — University of Maryland (content feedback v0.2.0; WAVE accessibility review v0.3.0)
- **Marla Hertz** — University of Alabama at Birmingham (content feedback v0.2.0)

## References
- Barbosa, S., et al. (2024). *GREI Repository Selection Flowchart*. Zenodo. https://doi.org/10.5281/zenodo.11105429
- Kim, S. (2024). *How to Select a Data Repository* [Video]. FASEB DataWorks! Seminar Series. https://www.youtube.com/watch?v=OO2UEOKhLjQ
- NIH repository selection guidance: https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/accessing-data/scientific
- NIH Genomic Data Sharing (GDS) Policy: https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/gds/overview
- NIH Genomic Data Sharing Policy — Where to Submit: https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/gds/where-to-submit
