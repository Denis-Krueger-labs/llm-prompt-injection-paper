# LLM Prompt Injection Defences

Seminar paper for the course **Expertise & Communication**
THWS Würzburg-Schweinfurt · Summer Semester 2026

**Authors:** Denis Krüger · Sebastian Mautner

---

## Topic

This paper examines prompt injection attacks in Large Language Model (LLM)
systems and evaluates the effectiveness and limitations of current defence
mechanisms. Since modern LLM-integrated applications process trusted
instructions and untrusted external data within the same context window, they
lack a structural boundary between instructions and data, creating a unique
class of vulnerabilities.

The paper focuses on:

* the structural origin of prompt injection vulnerabilities
* semantic separation approaches such as **StruQ** and **SecAlign**
* architectural and system-level defences
* evaluation methodologies and benchmark suites
* the impact of adaptive attacks on current defences
* the trade-off between robustness, utility, and deployment complexity

---

## Research Question

> How effective is the separation of instructions and data as a defence strategy
> against prompt injection attacks, and what do the limitations of current
> defences imply for the secure deployment of LLM-integrated systems?

---

## Main Findings

The analysis suggests that:

* prompt injection is fundamentally a structural problem caused by the absence
  of a hard boundary between instructions and data;
* fine-tuning approaches such as **StruQ** and **SecAlign** significantly
  improve robustness, but remain vulnerable to adaptive attacks;
* architectural approaches based on information flow control and capability
  isolation provide stronger guarantees, although at the cost of increased
  complexity;
* current evaluation methodology remains a challenge, as robustness often
  depends strongly on the attacks and benchmarks used;
* defence in depth is currently the most practical strategy for deploying
  LLM-integrated systems securely.

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
│   ├── 06_weitere_defences.tex
│   ├── 07_benchmarks_und_metriken.tex
│   ├── 08_grenzen_aktueller_defences.tex
│   ├── 09_praxis_und_management.tex
│   └── 10_fazit.tex
├── figures/
└── references.bib
```

---

## Key References

### Fine-Tuning Defences

* Chen et al. (2025), *StruQ: Defending Against Prompt Injection with Structured Queries*
* Chen et al. (2025), *SecAlign: Defending Against Prompt Injection with Preference Optimization*

### Architectural Defences

* Wu et al. (2024), *System-Level Defense against Indirect Prompt Injection Attacks: An Information Flow Control Perspective*
* Zhong et al. (2025), *RTBAS: Defending LLM Agents Against Prompt Injection and Privacy Leakage*
* Debenedetti et al. (2025), *Defeating Prompt Injections by Design*

### Evaluation and Adaptive Attacks

* Debenedetti et al. (2024), *AgentDojo*
* Jia et al. (2025), *A Critical Evaluation of Defenses against Prompt Injection Attacks*
* Yang et al. (2025), *Checkpoint-GCG*
* Pandya et al. (2025), *ASTRA*

---

## Building the Paper

Requires a LaTeX distribution with `pdflatex` and `biber`.

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```
