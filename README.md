# Javier Gonzálvez — Technical Portfolio

Source repository for my personal technical portfolio, built to present projects at the intersection of **mathematical engineering, physics, data science, simulation, AI, IoT, and scientific research**.

The website is designed as more than a list of technologies. Each project page explains the problem, methodology, implementation, results, limitations, and next steps so that technical work can be evaluated in context.

## Live website

https://javiergonzalvez07-star.github.io/

## Portfolio focus

The site documents work across several areas:

- data analysis and interpretable machine learning;
- numerical simulation and physical modelling;
- operations research and queueing theory;
- embedded sensing and IoT;
- structural health monitoring;
- computer vision;
- scientific research;
- technical leadership and student initiatives.

## Selected projects

Examples currently documented in the portfolio include:

- **PeerScope — Competitive Intelligence Platform** — financial KPIs, peer-group benchmarking, interpretable scoring, isolated private imports, grounded AI analysis, and versioned executive reporting;
- **Airport Queue Optimization Platform** — computer vision, M/M/c queueing, simulation, and operational decision support;
- **Railway Structural Health Monitoring Prototype** — ESP32 sensing, vibration analysis, condition indicators, and a Streamlit dashboard;
- **Formula 1 Race-Strategy Simulation** — tyre-degradation modelling and validation with historical race data;
- **Bank Customer Churn Analysis** — exploratory analysis and interpretable classification;
- **Supermarket Operations Analytics** — forecasting, queues, product associations, and refrigeration-energy modelling;
- **Smart Plant Monitoring** — IoT data quality and explainable irrigation criteria;
- **Applied Technical Projects Club** — multidisciplinary technical-project leadership.

## Technology stack

- Hugo
- Hugo Profile theme
- Markdown
- HTML / CSS
- YAML configuration
- GitHub Actions
- GitHub Pages

## Repository structure

```text
.
├── .github/workflows/   # Automated build and deployment
├── content/             # Project pages, articles, and essays
├── static/              # Images, CV, and other public assets
├── assets/              # Source assets and styles
├── themes/              # Hugo theme
├── hugo.yaml             # Site configuration and homepage content
└── README.md             # Repository overview
```

## Run locally

### Prerequisites

- Git
- Hugo Extended

Clone the repository including submodules:

```bash
git clone --recurse-submodules https://github.com/javiergonzalvez07-star/javiergonzalvez07-star.github.io.git
cd javiergonzalvez07-star.github.io
```

Start the development server:

```bash
hugo server -D
```

Open the local URL printed in the terminal.

## Content principles

Project pages aim to be:

- **problem-first** — explain the engineering or analytical question before the tools;
- **evidence-based** — include measured or simulated results where available;
- **honest about limitations** — distinguish prototypes from validated production systems;
- **reproducible** — link to source repositories and describe the technical workflow;
- **accessible** — communicate technical decisions to both specialist and non-specialist readers.

## Deployment

The website is deployed through GitHub Pages. Changes pushed to the deployment branch are built automatically and published to the live site.

## Author

**Javier Gonzálvez Sempere**  
Double Degree student in Mathematical Engineering and Physics at Universidad CEU San Pablo.

- Portfolio: https://javiergonzalvez07-star.github.io/
- LinkedIn: https://www.linkedin.com/in/javier-gonzalvez-sempere-b526552b0/
- GitHub: https://github.com/javiergonzalvez07-star
# Bilingual content maintenance

The site uses Hugo's native multilingual system. English is the default language and keeps the existing root URLs; Spanish equivalents are published below `/es/`.

## Add or update a page

- Leaf bundles use `index.md` for English and `index.es.md` for Spanish in the same directory.
- Regular pages use `name.md` and `name.es.md`; section indexes use `_index.md` and `_index.es.md`.
- Keep both files' slugs and directory structure aligned so Hugo can pair them and the `EN | ES` selector can preserve page context.
- Translate all visible front matter (`title`, `description`, `summary`, image alternative text, labels and metric captions) as well as the full body. Preserve code, official names, URLs, figures and units.
- Reusable interface labels belong in both `i18n/en.yaml` and `i18n/es.yaml`. Language-specific home-page data belongs under `languages.<lang>.params` in `hugo.yaml`.
- Internal template links should resolve a language-aware page (`site.GetPage` followed by `.RelPermalink`) rather than hard-code `/es/` or a root path.

The language selector links to the current page's translation when one exists and safely falls back to the selected language's home page otherwise. `/card/` is the stable English NFC URL and `/es/card/` is its Spanish equivalent; each page links directly to the matching CV and does not depend on JavaScript for language selection.

## Validate

Build to a temporary destination so the versioned `public/` directory is not modified:

```powershell
hugo --cleanDestinationDir --destination <temporary-directory>
```

Confirm that every English HTML route has an `/es/` counterpart, language switchers point to equivalent pages, internal links resolve, and each document has the expected `lang`, canonical, `hreflang`, `x-default`, and Open Graph locale metadata.
