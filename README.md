# LLM Prompt Injection Defences

Seminar paper for the course **Expertise & Communication**
THWS Würzburg-Schweinfurt · Summer Semester 2026

**Authors:** Denis Krüger · Sebastian Mautner

---

## Topic

This paper examines prompt injection attacks in Large Language Model (LLM)
systems. It uses StruQ and SecAlign as focused case studies of learned
instruction--data separation, compares their original evaluations with broader
and defence-adaptive studies, and derives system-level deployment implications.

The paper focuses on:

* the conditions that enable prompt injection vulnerabilities
* semantic separation approaches such as **StruQ** and **SecAlign**
* a taxonomy of model-, application-, and system-level defences
* evaluation methodology and cross-benchmark limitations
* the impact of adaptive attacks on current defences
* the trade-off between robustness, utility, and deployment complexity

---

## Research Question

> How effectively do learned instruction--data separation approaches mitigate
> prompt injection under the evaluated attacker models, and what system-level
> controls are required when they do not provide an independently enforced
> security boundary?

---

## Main Findings

The analysis suggests that:

* learned separation can substantially reduce attack success under the tested
  conditions, but remains model-mediated and probabilistic;
* adaptive white-box studies bypass the evaluated **StruQ** and **SecAlign**
  models, without proving that all model-level defences are impossible;
* results from different papers are not directly comparable when their models,
  attacks, budgets, datasets, success rules, or utility baselines differ;
* externally enforced authorisation, least privilege, containment, monitoring,
  and incident response are needed to limit the consequences of model failure;
* stronger architectural guarantees remain conditional on correct policies,
  labels, wrappers, and trusted enforcement components.

---

## Structure

```text
paper/
├── main.tex
├── sections/
│   ├── 00_titlepage.tex
│   ├── 00_abstract.tex
│   ├── 01_einleitung.tex
│   ├── 02_llms_und_prompting.tex
│   ├── 03_prompt_injection.tex
│   ├── 04_bedrohungsmodell.tex
│   ├── 05_struq.tex
│   ├── 06_limits_of_current_defences.tex
│   ├── 09_praxis_und_management.tex
│   └── 10_fazit.tex
├── images/
└── references.bib
```

---

## Key References

### Fine-Tuning Defences

* Chen et al. (2025), *StruQ: Defending Against Prompt Injection with Structured Queries*
* Chen et al. (2025), *SecAlign: Defending Against Prompt Injection with Preference Optimization*

### Architectural Defences

* Wu et al. (2024), *System-Level Defense against Indirect Prompt Injection Attacks: An Information Flow Control Perspective*
* Debenedetti et al. (2025), *Defeating Prompt Injections by Design*

### Evaluation and Adaptive Attacks

* Debenedetti et al. (2024), *AgentDojo*
* Jia et al. (2025), *A Critical Evaluation of Defenses against Prompt Injection Attacks*
* Yang et al. (2025), *Checkpoint-GCG*
* Pandya et al. (2025), *ASTRA*

---

## Building the Paper

Requires a LaTeX distribution with `pdflatex` and `biber`. Run the commands from
the `paper/` directory because the input and bibliography paths are relative to
that directory.

```bash
cd paper
pdflatex -interaction=nonstopmode -halt-on-error -file-line-error main.tex
biber main
pdflatex -interaction=nonstopmode -halt-on-error -file-line-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error -file-line-error main.tex
```
