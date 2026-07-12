---
title: "Honesty-Oriented Prompting and the Reliability–Utility Trade-off: A Controlled Evaluation of LLM Hallucinations"
shortTitle: "LLM reliability–utility trade-off"
date: 2026-07-06
draft: false
description: "A 600-response controlled benchmark measuring how honesty-oriented prompting changes hallucination, accuracy and abstention across three lightweight LLMs."
summary: "Across 600 responses, honesty prompting reduced observed hallucinations from 21.3% to 7.3%, but raised overall and unnecessary abstention."
area: "AI Evaluation · Reliability Research"
image: "/images/research/hallucination/provider-hallucination.png"
imageAlt: "Hallucination rates by model provider under normal and honesty-oriented prompts"
badges: ["LLM Evaluation", "Benchmark Design", "Bootstrap CI", "Paired Testing"]
glance:
  - label: "Benchmark"
    value: "100 questions · 8 categories"
  - label: "Models"
    value: "3 lightweight API models"
  - label: "Evaluated outputs"
    value: "600 responses"
  - label: "Core trade-off"
    value: "Fewer fabrications · more refusals"
---

## The problem

Factual reliability is not captured by accuracy alone. A useful model must avoid unsupported claims, abstain when evidence is missing and still answer straightforward questions. This controlled study tested whether a short honesty-oriented instruction improves that calibration or merely makes models more cautious.

## Research approach

<div class="process-grid" aria-label="Research workflow"><div class="process-step"><b>01 · Design</b>Create a 100-question adversarial benchmark across eight failure modes.</div><div class="process-step"><b>02 · Generate</b>Query three models under normal and honesty prompt conditions at temperature 0.</div><div class="process-step"><b>03 · Annotate</b>Manually label correctness, hallucination, severity and overconfidence.</div><div class="process-step"><b>04 · Compare</b>Use paired tests and question-level bootstrap confidence intervals.</div></div>

### Benchmark and models

The benchmark covered clear facts, common misconceptions, error-prone facts, fake papers or citations, correct-abstention cases, missing context, time-sensitive facts and false presuppositions. Each of three lightweight API models—`gpt-4o-mini`, `gemini-2.5-flash-lite` and `claude-haiku-4-5-20251001`—answered every item twice, producing **300 responses per condition**.

<figure class="research-figure"><img src="/images/research/hallucination/category-rate.png" alt="Hallucination rate across eight benchmark categories, highest for fabricated citations" loading="lazy"><figcaption>Fabricated citations, time-sensitive queries and missing context were the most failure-prone categories in this stress test.</figcaption></figure>

## Modelling and data analysis

Responses were manually labelled against predefined ground truth. Abstention was reconstructed through deterministic phrase detection, with a row-level audit trail. The final dataset was checked for six valid responses per question. Because each model answered the same question under both prompts, outcomes could be compared as **paired observations** rather than as unrelated samples. Exact binomial McNemar-style tests evaluated the responses that changed outcome, while question-level bootstrap resampling estimated 95% confidence intervals.

Because this is an adversarial 100-question benchmark, results are exploratory and should not be generalized to overall provider accuracy.

## Key results

<div class="result-callout"><div><strong>21.3% → 7.3%</strong>Observed hallucination rate decreased by 14.0 percentage points.</div><div><strong>79.7% → 88.3%</strong>Accuracy increased within this controlled benchmark.</div><div><strong>10.3% → 25.0%</strong>Overall abstention rose, revealing the utility cost.</div></div>

| Metric | Normal prompt | Honesty prompt | Difference |
|---|---:|---:|---:|
| Hallucination rate | 21.3% | 7.3% | −14.0 pp |
| Abstention rate | 10.3% | 25.0% | +14.7 pp |
| Accuracy rate | 79.7% | 88.3% | +8.6 pp |

<figure class="research-figure"><img src="/images/research/hallucination/provider-hallucination.png" alt="Provider-level hallucination rates falling under the honesty prompt for all three evaluated models" loading="lazy"><figcaption>Observed hallucinations decreased across all three model providers under the honesty-oriented prompt.</figcaption></figure>

The change was therefore not a universal improvement. On items where refusal was appropriate, correct abstention rose from **46.7% to 73.3%**. On answerable items, however, unnecessary abstention rose from **1.7% to 14.2%**.

<figure class="research-figure"><img src="/images/research/hallucination/provider-abstention.png" alt="Provider-level abstention rates increasing under the honesty prompt" loading="lazy"><figcaption>Higher factual caution also increased refusal behavior, including on answerable questions.</figcaption></figure>

## What the results mean

Within this benchmark, honesty-oriented prompting reduced fabrication but behaved as a blunt calibration tool: it raised the apparent threshold for answering and induced excessive caution. A stronger intervention would distinguish unverifiable claims from stable facts through more granular verification or confidence mechanisms.

### Limitations

The study used only 100 adversarial questions, three lightweight models and one manual annotator. Inter-rater agreement was not measured, phrase-based abstention detection can miss subtle uncertainty, and the findings do not represent everyday query distributions.

## Skills demonstrated

<div class="skills-grid"><div class="skill-chip">Benchmark design</div><div class="skill-chip">API experimentation</div><div class="skill-chip">Manual annotation</div><div class="skill-chip">Paired hypothesis testing</div><div class="skill-chip">Bootstrap intervals</div><div class="skill-chip">Data auditing</div><div class="skill-chip">Error analysis</div><div class="skill-chip">Scientific communication</div></div>
