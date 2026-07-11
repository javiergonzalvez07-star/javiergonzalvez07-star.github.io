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
