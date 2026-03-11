# AGENTS.md — Hospita Admission Records Analysis AI Agent Governance
This file defines the rules for AI-assisted contributions in this repository.

AI agents must follow the policies in this document before reading, modifying, or generating any code or documentation in the repository.

Last updated: 2026-03-11


## Testing Requirements
All changes must pass the environment validation before committing.

Run: `python test_environment.py`

The script must output:
`Environment OK`

Any new code added to `src/` (data processing or analysis modules) must include a corresponding test in the `tests/` directory.

All tests must pass when running:
`pytest tests/ -v`
If tests fail, the change should not be committed.

## Secrets Policy
This project simulates analysis of hospital admission data, which may represent sensitive medical information.

The following must never appear in prompts, code, or commits:

    1-API keys
    2-database passwords
    3-.env files
    4-private credentials
    5-raw datasets

Never commit:

`.env`, `*.key`, `*.pem`, or any dataset files such as `*.csv`, `*.xlsx`, or `*.parquet`.

Raw datasets must remain outside version control and stored only in:
`data/raw/`

## Scope Boundaries
AI agents may modify:
    1- `src/` — Python modules for data analysis
    2- `notebooks/` — exploratory analysis notebooks
    3- `tests/` — automated tests

Human review is required before modifying , DO NOT MODIFY WITHOUT HUMAN REVIEW:
    1- `requirements.txt`
    2- `setup.sh`
    4- `AGENTS.md`

AI agents may NEVER modify `.gitignore`

Changes to environment configuration or dependency management must be tested locally before committing.

## Reproducibility Standard
All AI-assisted changes must follow a local-first verification workflow.

Before committing or pushing code:

1- Run `bash setup.sh` to verify the environment.
2- Run `python test_environment.py` and confirm it prints `Environment OK` .
3- Ensure that `.venv/`, `data/raw/`, or other ignored files are not staged for commit.

A change is considered complete only if another contributor can clone the repository, run the setup steps, and reproduce the environment successfully.

"The AI generated it" is not a substitute for running and verifying the code locally.