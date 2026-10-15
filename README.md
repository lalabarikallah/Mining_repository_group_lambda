# AI-Authored vs Human-Authored Pull Requests: A Repository Mining Study

Course project for **LOG6307E** (Group Lambda).

This project compares **pull requests (PRs) written by AI coding agents** with **PRs written by humans** on GitHub, using the AIDev dataset. We study two research questions:

- **RQ1:** How do merge rates differ between AI-authored and human-authored pull requests?
- **RQ2:** How does the size of AI-authored pull requests relate to their likelihood of being merged?

## Repository Structure

```
.
├── 01_data_collection.ipynb    # Part 1: data collection / raw tables
├── 02_cleaning_and_analysis.ipynb     # Part 2: cleaning, metrics, and analysis (RQ1 & RQ2)
├── data/
│   ├── raw/                     # Raw tables exported in Part 1
│   └── clean/                   # Cleaned datasets used for the analysis
├── figures/                     # Plots produced by the analysis
└── README.md
```

## Data

The raw tables (exported in data collection Part 01, stored in `data/raw/`) are:

| File | Content |
|---|---|
| `agent_pr.parquet` | 33,596 AI-authored PRs (OpenAI Codex, Copilot, Devin, Cursor, Claude Code) |
| `human_pr.parquet` | 6,618 human-authored PRs |
| `pr_commit_details.parquet` | 711,923 file-level commit records (additions, deletions, changes) |
| `overlap_urls.csv` | 56 PRs that appear in both the AI and human tables |

The cleaned datasets (in `data/clean/`) are:

| File | Content |
|---|---|
| `agent_pr_clean` (`.parquet` / `.csv`) | 31,233 closed AI PRs (RQ1) |
| `human_pr_clean` (`.parquet` / `.csv`) | 5,065 closed human PRs (RQ1) |
| `merge_rate_table.csv` | Merge rate for AI vs Human PRs |
| `agent_pr_size_clean` (`.parquet` / `.csv`) | 30,793 AI PRs with size metrics (RQ2) |


## Team (Group Lambda)

- [Sara Boubekri]
- [Leila Rouga]
- [Lala Barik Allah]
- [Yassine Mohamed Taha Abassi]
