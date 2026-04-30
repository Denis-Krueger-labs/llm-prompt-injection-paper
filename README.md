# LLM Prompt Injection Defences

Seminar paper for the course **Expertise & Communication**  
THWS Würzburg-Schweinfurt · Summer Semester 2026

**Authors:** Denis Krüger · Sebastian Mautner

---

## Topic

This paper analyzes **prompt injection attacks** in Large Language Model (LLM)
systems and evaluates current defence mechanisms. LLMs are increasingly deployed
in applications that process external, untrusted data emails, documents, web
pages, API responses and this integration introduces a critical vulnerability:
the inability to structurally separate instructions from data.

The paper focuses on:

- the underlying vulnerability caused by the instruction/data boundary problem
- structured query approaches such as **StruQ** and **SecAlign**
- detection-based and system-level defences
- evaluation using recent benchmarks (AgentDojo, OpenPromptInjection, AlpacaFarm)
- the limits of current protection mechanisms under adaptive attacks

---

## Research Question

> How effective is the separation of instructions and data as a defence strategy
> against prompt injection, and where do the limits of current LLM prompt
> injection defences lie?

---

## Sources

### Core Papers

| Key | Title | Authors | Venue |
|-----|-------|---------|-------|
| StruQ | *StruQ: Defending Against Prompt Injection with Structured Queries* | Chen et al. | USENIX Security 2025 |
| SecAlign | *SecAlign: Defending Against Prompt Injection with Preference Optimization* | Chen et al. | ACM CCS 2025 |
| AgentDojo | *AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents* | Debenedetti et al. | NeurIPS 2024 |
| Critical Evaluation | *A Critical Evaluation of Defenses against Prompt Injection Attacks* | Jia et al. | arXiv 2025 |
| Checkpoint-GCG | *Checkpoint-GCG: Auditing and Attacking Fine-Tuning-Based Prompt Injection Defenses* | Yang et al. | arXiv 2025 |
| ASTRA | *May I Have Your Attention? Breaking Fine-Tuning Based Prompt Injection Defenses Using Architecture-Aware Attacks* | Pandya et al. | arXiv 2025 |

### Foundational

| Key | Title | Authors | Venue |
|-----|-------|---------|-------|
| Perez & Ribeiro | *Ignore Previous Prompt: Attack Techniques for Language Models* | Perez & Ribeiro | arXiv 2022 |
| Greshake et al. | *Not What You've Signed Up For: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection* | Greshake et al. | AISec 2023 |
| Zou et al. | *Universal and Transferable Adversarial Attacks on Aligned Language Models* | Zou et al. | arXiv 2023 |
| Wallace et al. | *The Instruction Hierarchy: Training LLMs to Prioritize Privileged Instructions* | Wallace et al. | arXiv 2024 |
| Liu et al. | *Prompt Injection Attack against LLM-Integrated Applications* | Liu et al. | arXiv 2023 |

### Defences

| Key | Title | Authors | Venue |
|-----|-------|---------|-------|
| PromptArmor | *PromptArmor: Simple yet Effective Prompt Injection Defenses* | Shi et al. | arXiv 2025 |
| RTBAS | *RTBAS: Defending LLM Agents Against Prompt Injection and Privacy Leakage* | Zhong et al. | arXiv 2025 |
| f-secure / IFC | *System-Level Defense against Indirect Prompt Injection Attacks: An Information Flow Control Perspective* | Wu et al. | arXiv 2024 |
| Spotlighting | *Defending Against Indirect Prompt Injection Attacks With Spotlighting* | Hines et al. | arXiv 2024 |
| Defeating by Design | *Defeating Prompt Injections by Design* | Debenedetti et al. | arXiv 2025 |
| A-MemGuard | *A-MemGuard: A Proactive Defense Framework for LLM-Based Agent Memory* | Wei et al. | arXiv 2025 |

### Benchmarks & Evaluation

| Key | Title | Authors | Venue |
|-----|-------|---------|-------|
| InjecAgent | *InjecAgent: Benchmarking Indirect Prompt Injections in Tool-Integrated LLM Agents* | Zhan et al. | arXiv 2024 |
| InjectBench | *InjectBench: An Indirect Prompt Injection Benchmarking Framework* | Kong | Master's Thesis, Virginia Tech 2024 |
| FSPIB | *Prompt Injection Benchmark for Foundation Model Integrated Systems* | Anonymous | Under review, ICLR 2025 |
| MPIB | *MPIB: A Benchmark for Medical Prompt Injection Attacks and Clinical Safety in LLMs* | Lee et al. | arXiv 2025 |

### Real-World & Survey

| Key | Title | Authors | Venue |
|-----|-------|---------|-------|
| P2SQL | *Prompt-to-SQL Injections in LLM-Integrated Web Applications: Risks and Defenses* | Pedro et al. | ICSE 2025 |
| Survey | *Prompting for LLM Security and RAG: A Survey* | Ruparel et al. | IEEE ICAIC 2026 |
| Mathew | *Enhancing Security in LLMs: A Comprehensive Review of Prompt Injection Attacks and Defenses* | Mathew | Preprint 2024 |

---

## Project Structure

```text
paper/
├── main.tex
├── sections/
│   ├── 00_titlepage.tex
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

## Building the Paper

Requires a LaTeX distribution with `biber` and `pdflatex`.

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```
