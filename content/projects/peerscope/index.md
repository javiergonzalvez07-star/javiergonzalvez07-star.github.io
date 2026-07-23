---
title: "PeerScope — Competitive Intelligence Platform"
description: "PeerScope is a tested competitive-intelligence platform combining financial KPIs, peer-group benchmarking, interpretable scoring, private data imports, grounded AI analysis and versioned executive reporting."
summary: "End-to-end analytics platform turning financial data into peer benchmarks, interpretable scores, grounded AI diagnostics and versioned reports."
date: 2026-07-23
draft: false
slug: "peerscope"
translationKey: "peerscope"
layout: "peerscope"
tags: ["Python", "FastAPI", "Supabase", "OpenAI API", "Financial Analytics", "Decision Support"]
badges: ["Python", "FastAPI", "Supabase", "OpenAI API", "Financial Analytics"]
image: "/images/projects/peerscope/peerscope-landing.webp"
featuredImage: "/images/projects/peerscope/peerscope-landing.webp"
images: ["/images/projects/peerscope/peerscope-landing.webp", "/images/projects/peerscope/peerscope-benchmark.webp", "/images/projects/peerscope/peerscope-ai-analyst.webp", "/images/projects/peerscope/peerscope-report.webp"]
imageAlt: "PeerScope public landing page presenting the competitive-intelligence product"
status: "Functional private beta"
eyebrow: "Engineering & product case study"
subtitle: "An end-to-end platform for turning company financial data into fair peer comparisons, interpretable competitive diagnostics and executive reports."
liveLabel: "Open live beta"
backLabel: "Back to projects"
coldStart: "Hosted on Render; the beta may take a few seconds to wake after inactivity."
heroCaption: "PeerScope public landing page. The analytical views below come from the product's static public demo."
metricsLabel: "Verified project metrics"
metrics:
  - value: "1,777"
    label: "companies in the data pipeline"
  - value: "1,164"
    label: "companies with valid competitive scores"
  - value: "6"
    label: "interpretable scoring dimensions"
  - value: "194"
    label: "automated tests passed"
  - value: "11"
    label: "additional subtests passed"
  - value: "1"
    label: "production-like Sector Pack: chemical manufacturing"
finalEyebrow: "Explore the product"
finalTitle: "From financial records to a reviewable diagnosis"
finalText: "The public site and static demo demonstrate the product flow without presenting its outputs as definitive financial advice."
---

## From financial records to decision support

PeerScope is designed for boutique consultancies, analysts, strategy teams and company-diagnostic projects that need to turn financial records into a structured, presentable reading. It connects data ingestion, normalization, KPIs, comparable-company selection, percentiles, deterministic scoring, diagnostics, grounded AI and reporting in one traceable workflow.

> The difficult part is not displaying financial data. It is deciding what each value means relative to comparable companies, communicating the uncertainty and turning the result into a traceable recommendation.

The platform supports professional judgement; it does not replace expert financial review or guarantee a correct decision.

## The problem

<div class="ps-grid">
<section class="ps-card"><h3>Data without context</h3><p>An isolated ratio does not establish whether a company is well positioned. Its meaning depends on scale, leverage, productivity, coverage and sector context.</p></section>
<section class="ps-card"><h3>Unfair comparisons</h3><p>Directly comparing incompatible companies can mislead. Peer groups use variables such as company size, employees, revenue and sector context, while limited samples are surfaced.</p></section>
<section class="ps-card"><h3>Manual reporting</h3><p>Turning analysis into an executive document requires repetitive work, methodological consistency, review and a clear distinction between evidence and interpretation.</p></section>
</div>

PeerScope is neither a stock-prediction tool nor a system that promises correct decisions. It structures evidence for a human analyst.

## End-to-end workflow

<div class="ps-workflow">
<section class="ps-step"><span class="ps-step-number">1</span><h3>Search or import a company</h3><p>Search the base dataset or optionally upload CSV/XLSX data associated with an account or organization.</p></section>
<section class="ps-step"><span class="ps-step-number">2</span><h3>Normalize and validate</h3><p>Convert formats and fields into a canonical structure, validate them before analysis and export normalized data where appropriate.</p></section>
<section class="ps-step"><span class="ps-step-number">3</span><h3>Build a relevant peer group</h3><p>Use scale, revenue and context to avoid incompatible comparisons, and disclose when the available sample is limited.</p></section>
<section class="ps-step"><span class="ps-step-number">4</span><h3>Calculate KPIs and percentiles</h3><p>Produce financial and operating ratios, relative positions and explicit strong, weak or missing-data signals.</p></section>
<section class="ps-step"><span class="ps-step-number">5</span><h3>Generate the competitive score</h3><p>Combine six weighted blocks into an interpretable tier. The method is deterministic, not an AI algorithm or black box.</p></section>
<section class="ps-step"><span class="ps-step-number">6</span><h3>Produce diagnostics and levers</h3><p>Trace strengths, alerts, gaps, next areas of focus and improvement levers back to concrete values.</p></section>
<section class="ps-step"><span class="ps-step-number">7</span><h3>Use the AI Analyst</h3><p>Ask grounded questions, explain results for financial or non-financial audiences, synthesize risks and prioritize KPIs.</p></section>
<section class="ps-step"><span class="ps-step-number">8</span><h3>Create and version the report</h3><p>Preview, review and export successive HTML/PDF versions, keeping internal and client-facing content separate.</p></section>
</div>

AI therefore appears after a defined analytical chain; it does not replace ingestion, comparability, scoring or professional review.

<figure class="ps-demo-figure">
  <img src="/images/projects/peerscope/peerscope-benchmark.webp" alt="PeerScope static public demo showing company benchmark and competitive scoring results" loading="lazy" width="1065" height="720">
  <figcaption>Static public demo: peer-group benchmark and interpretable scoring view using demonstration data.</figcaption>
</figure>

## Interpretable scoring methodology

| Dimension | Weight |
|---|---:|
| Profitability | 25% |
| Financial strength | 25% |
| Productivity | 20% |
| Growth | 15% |
| Operations | 10% |
| Efficiency | 5% |

Each block groups related KPIs and interprets them inside a peer group. Percentiles express relative position; the global score summarizes the evidence but never replaces its detail. Strengths and alerts remain traceable to values. Missing data is distinguished from a negative result, and small peer groups or poor coverage must not be presented with false precision.

The weights are a product methodology, not a universal financial truth. They are explicit so they can be challenged, validated and evolved.

> **Why this matters:** two companies can report the same margin and still have a different competitive interpretation when scale, leverage, productivity and sector context are considered.

## Sector Packs: controlled depth

Different sectors need different KPIs, rules, thresholds and priorities. PeerScope keeps a common scoring core and controlled sector extensions so new methods do not become scattered copies of logic. The first production-like pack is for **chemical manufacturing**. Adding and validating further packs is a next step; the product does not claim deep coverage of every industrial sector today.

## AI Analyst: what it actually does

### Questions about a company

Users can ask about the overall position, principal risks, priority KPIs, comparison with similar companies, strengths, improvement levers or an explanation for a non-financial client. The allowed context is limited to visible and authorized data, calculated KPIs, available benchmarks, account-permitted imports and approved methodology.

OpenAI keys stay in the backend. Responses are grounded in system values, verified claims are separated from hypotheses, missing figures must not be invented, and data limitations must be communicated. Usage can be limited by plan.

<figure class="ps-demo-figure">
  <img src="/images/projects/peerscope/peerscope-ai-analyst.webp" alt="PeerScope AI Analyst static public demo grounded in company KPIs and benchmark context" loading="lazy" width="1065" height="720">
  <figcaption>Static public demo: AI Analyst interface for grounded questions about the company analysis.</figcaption>
</figure>

### Assistance during report preparation

The analyst can request a specific observation, a different emphasis, an anomaly explanation, an adapted tone or reasoning supplied by the human reviewer. AI does not blindly overwrite the document: preview, human control, traceability, an approved structure, versioning, and the internal/client boundary remain intact. It is an interaction and writing layer over a real analytical system—not the data source of truth.

## Reporting as a deliverable

The report flow covers a company profile, main KPIs, block benchmarks, strengths, alerts, levers, conclusions and next areas of focus. It supports HTML/PDF, preview before sharing, successive versions per company, reusable templates and standard comments, internal methodology, and separation between client deliverables and internal observations.

> Reports are treated as versioned analytical deliverables, not disposable AI responses.

The objective is not to export a table, but to create a consistent document that can be reviewed and presented.

<figure class="ps-demo-figure">
  <img src="/images/projects/peerscope/peerscope-report.webp" alt="PeerScope static public demo showing the preview of a versioned executive report" loading="lazy" width="1065" height="720">
  <figcaption>Static public demo: report preview before review, versioning and HTML/PDF export.</figcaption>
</figure>

## Private imports and data separation

<div class="ps-grid">
<section class="ps-card"><h3>Base dataset</h3><p>Company data used for general search, comparison, KPI calculation and scoring.</p></section>
<section class="ps-card"><h3>Imported data</h3><p>User CSV/XLSX files linked to their account or organization, stored separately with persistent history.</p></section>
</div>

Imports are normalized, can be exported in normalized form and may feed secondary modules such as an opportunity radar. They do **not** silently modify SABI and do **not** enter scoring or benchmarking automatically while that integration is not enabled. Any future scoring integration must be explicit, authorized and controlled.

<figure class="ps-architecture">
  <img src="/images/projects/peerscope/peerscope-architecture.svg" alt="Architecture diagram showing SABI data flowing to deterministic scoring and reports while private imports remain isolated behind an explicit integration boundary" loading="lazy" width="1200" height="760">
</figure>

## Technical architecture

<div class="ps-grid">
<section class="ps-card"><h3>Product interface</h3><p>HTML/CSS/JavaScript landing, authentication and workspace for search, diagnostics, KPIs, benchmarks, levers, imports, reports, AI Analyst and settings.</p></section>
<section class="ps-card"><h3>API and business logic</h3><p>Python and FastAPI endpoints for validation, authorization, peer groups, scoring, diagnostics, reporting and AI-usage control.</p></section>
<section class="ps-card"><h3>Data layer</h3><p>Supabase, PostgreSQL and Supabase Auth for the base data, application tables, private imports, saved analyses, templates, versions and configuration.</p></section>
<section class="ps-card"><h3>AI layer</h3><p>OpenAI API with controlled prompts, allowed context, grounding in calculated results and explicit claim-versus-hypothesis handling.</p></section>
<section class="ps-card"><h3>Deployment and validation</h3><p>Render, environment configuration, pytest, Python import checks, builds and a security checklist. CSV/XLSX processing and HTML/PDF generation complete the pipeline.</p></section>
</div>

No claim is made here about microservices, queues, Kubernetes or proprietary trained models: the architecture reflects the implemented beta.

## Security and privacy

Authentication, protected sessions and sensitive endpoints, backend-only OpenAI keys, account/organization-scoped imports, access controls, plan-based AI limits, and no frontend secrets form the security baseline. Supabase Row Level Security policies are required for relevant tables; the latest known validation specifically covers **14 tables**.

RLS is not treated as a configuration checkbox. Tests verify expected secure behavior and detect unsafe RLS configurations. A pre-demo checklist supports controlled use, and the beta exposes pricing plans without real payment processing.

<div class="ps-note"><strong>Scope of the claim:</strong> this is a functional beta with real controls and ongoing hardening—not an externally audited, certified system or an unrestricted production environment for highly sensitive financial information.</div>

## Testing and reliability

The last verified suite completed **194 automated tests plus 11 additional subtests**. Coverage includes endpoints, configuration, scoring, security, unsafe RLS detection, report preview and safe behavior when configuration is missing. Validation also included Python import checks, `py_compile`, and confirmation that the FastAPI application can be imported.

The public static demo creates no data, executes no AI and changes no imports. It is a safe way to inspect benchmark/scoring, imports, AI Analyst and reporting concepts.

> The test suite protects not only individual functions, but also product assumptions such as data isolation, access control and scoring consistency.

**Current readiness:** ready for a controlled demo and product validation, not yet for unrestricted production use.

## Product and engineering decisions

<div class="ps-decisions">
<section class="ps-card"><h3>Peer groups before scoring</h3><p>A score without suitable comparables can mislead.</p></section>
<section class="ps-card"><h3>Interpretable scoring before generative AI</h3><p>AI explains calculated results; it does not invent the method.</p></section>
<section class="ps-card"><h3>Private imports remain isolated</h3><p>User data is not mixed into the base dataset for convenience.</p></section>
<section class="ps-card"><h3>Reports are versioned</h3><p>An important deliverable must be reviewable and able to evolve.</p></section>
<section class="ps-card"><h3>Internal differs from client-facing</h3><p>Consultancy observations can remain outside the final report.</p></section>
<section class="ps-card"><h3>Claims differ from hypotheses</h3><p>AI uncertainty and data limitations must be communicated.</p></section>
<section class="ps-card"><h3>Security is enforced through tests</h3><p>Supabase safety is verified, not merely assumed.</p></section>
<section class="ps-card"><h3>Beta pricing without payments</h3><p>Plans test positioning, limits and experience before premature billing.</p></section>
<section class="ps-card"><h3>Sector depth over fake breadth</h3><p>One real chemical pack is more honest than superficial multi-sector claims.</p></section>
</div>

## My role and development process

PeerScope began as my own project and reached this beta in less than one month. I defined the problem and target user, designed the benchmarking concept, chose the scoring dimensions and weights, specified the product workflow, decided how base and imported data remain separate, and designed the role of AI. I reviewed audits, prioritized security issues, validated iterations and directed the architecture and evolution.

I used Codex intensively to accelerate implementation, review, tests and refactors, while evaluating outputs and making final product and engineering decisions.

> I designed the product, analytical methodology and engineering requirements, and used Codex as an implementation and review agent. Development followed repeated cycles of auditing, implementation, testing and correction rather than a single generated prototype.

## Results and current state

The functional beta includes a public landing, authentication and protected workspace; company search; a 1,777-company pipeline and 1,164 valid scores; peer groups, KPIs, percentiles and scoring across six blocks; diagnostics, strengths, alerts and levers; AI Analyst; CSV/XLSX imports, normalization, isolated history and normalized exports; an opportunity radar; recent or saved analyses; report templates, standard comments and internal methodology; client/internal separation, preview, versioned HTML/PDF reports; beta plans and limits; security controls; a public Render deployment; and the automated suite.

## Current limitations

- The product remains a private beta with methodology concentrated on chemical manufacturing.
- Further Sector Packs and validation across more sectors and companies are pending.
- Coverage and quality depend on the source dataset; small peer groups reduce comparison robustness.
- Private imports do not automatically alter scoring while explicit integration is unavailable.
- AI is constrained by available, authorized data and cannot replace expert financial judgement.
- Results support analysis; they are not definitive financial advice.
- Pricing plans have no real payments, production hardening is incomplete, and more validation with real users is required.

## Roadmap

- Add Sector Packs based on the KPIs already designed and validate them across more companies.
- Improve peer-group quality assessment and integrate private imports only under explicit rules.
- Extend organization and team collaboration while reinforcing permissions and security.
- Improve template personalization, claim traceability, observability and error tracking.
- Measure usefulness with real users and prepare the product for controlled production use.

These are development priorities, not commercial promises.

## What this project demonstrates

PeerScope combines technical product design, data engineering, financial analytics, KPI modelling, interpretable systems, APIs, databases, authentication and permissions, grounded AI, testing, security, deployment and technical communication. It also reflects an iterative way of directing development agents while retaining responsibility for the method and result.

> PeerScope demonstrates my ability to move from an ambiguous business problem to a structured analytical methodology, a tested software architecture and a usable decision-support product.
