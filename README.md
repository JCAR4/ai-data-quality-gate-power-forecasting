## AI-Assisted Data Quality Gate for Power Forecasting

This project implements a deterministic data quality gate for time-series datasets
used in electricity demand forecasting.

The system combines:
- Rule-based data validation in Python
- LLM-assisted contextual review for edge cases (e.g. extreme weather vs data errors)

### Why this matters
In power trading and forecasting workflows, models like XGBoost are highly sensitive
to data quality. This gate enforces hard constraints before training while using
LLMs only for interpretation, not decision-making.

### What it does
- Detects missing values, duplicates, and statistical outliers
- Applies explicit business rules to determine Pass/Fail
- Uses an LLM to suggest targeted cleaning steps and interpret anomalies

### Design Philosophy
- Deterministic logic first
- AI as a reviewer, not a source of truth
- Domain-aware prompts tailored to power trading data

### Tech Stack
- Python (Pandas, NumPy)
- OpenAI API (programmatic, non-chat usage)

### Future Improvements
- Rolling-window anomaly detection for time-series
- Structured JSON outputs from LLM
- Integration into automated model training pipelines
