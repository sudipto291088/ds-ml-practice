# Agentic Data Science Assistant (SID-ADSA)

## Overview
The Agentic Data Science Assistant (SID-ADSA) is a Python-based, rule-driven data analysis agent that autonomously performs exploratory data analysis (EDA) on a given dataset.

Unlike traditional notebooks that require manual, step-by-step execution, this project demonstrates an **agentic workflow**: the system observes a dataset, plans analysis steps, executes analytical tools, and produces reproducible artifacts such as reports and plots.

---

## What Problem Does This Solve?
Exploratory Data Analysis is often repetitive and manual:
- Inspecting dataset structure
- Checking missing values
- Generating summary statistics
- Creating standard visualizations

SID-ADSA automates these steps in a structured and explainable way, making EDA:
- Faster
- Reproducible
- Easier to audit and review

---

## How the Agent Works (High-Level)
The system follows a simple agent loop:

1. **Observe**
   - Inspect dataset shape, column types, and missing values
2. **Plan**
   - Decide which analyses to run based on dataset characteristics
3. **Act**
   - Execute analysis tools (summaries, plots, correlations)
4. **Remember**
   - Store results and actions in internal memory
5. **Output**
   - Save reports and plots to disk for reuse

The agent is rule-based (no LLM dependency) to keep behavior deterministic and transparent.

---

## Project Structure


- `ADSA.ipynb` — main notebook containing the agent logic
- `outputs/report.md` — auto-generated EDA summary
- `outputs/plots/` — generated visualizations

---

## How to Run
1. Open `ADSA.ipynb` in Jupyter Notebook
2. Run all cells from top to bottom
3. The agent will:
   - Analyze the dataset
   - Generate plots
   - Save results to the `outputs/` directory

---

## Outputs
After execution, the following artifacts are generated automatically:
- A markdown EDA report (`outputs/report.md`)
- Histogram plots for numeric features (`outputs/plots/*.png`)

These outputs are suitable for version control and review.

---

## Future Improvements
- Modularize agent logic into standalone Python modules
- Add configurable analysis strategies
- Integrate LLM-based planning for adaptive decision-making
- Expose the agent via a simple web or API interface

---

## License
This project is intended for educational and portfolio demonstration purposes.

