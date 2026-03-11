# Project Title — Hospital Admission Records Analysis

## Team Members
    1- Bashar Albdour
    2- Rayan Albdour
    3- Ahmed Saleh

---

## Project Overview

This project sets up the development environment for the hospital admission data analysis project.  
It defines the required dependencies and configuration so that all team members can reproduce the same Python environment.  
The setup ensures that the project can run correctly before data analysis begins.

---
## Data Source
Data is not tracked in this repository. See the setup instructions below for how to obtain and place the data files before running any analysis:

 Before running analysis, datasets should be placed locally in the following directory:
 `data/raw/admissions.csv`

 Raw datasets must never be committed to the repository.

---

## Setup Instructions

Complete these setup steps to setup : 

1-Clone the repository:
    `git clone <repo-url>`
    `cd <repo-name>`

2-Create the Python virtual environment:
    `python -m venv .venv`

3- Activate the environment depending on your platform:

Mac / Linux
`source .venv/bin/activate`

Windows Git Bash
`source .venv/Scripts/activate`

Windows CMD
`.venv\Scripts\activate.bat`

Windows PowerShell
`.venv\Scripts\Activate.ps1`

## Install project dependencies:

`pip install -r requirements.txt`

## Verify that the environment works correctly:

`python test_environment.py`
    Expected output:
    `Environment OK` 

## You can also run the automated setup script:

`./setup.sh`

Expected output:
`Setup complete.`

---
## Project Structure
m1-l1-git-workflows-BasharAlbdour/ 
│ 
├── .github/ `GitHub configuration files `
├── .venv/ # `Local Python virtual environment (not tracked) `
├── tests/ # `Automated test files` 
│ 
├── .gitignore # `Files ignored by Git` 
├── AGENTS.md # `AI contribution policy ` 
├── CHANGELOG.md # `Project change history `
├── README.md # `Project documentation `
│ 
├── requirements.txt # `Python dependencies` 
├── setup.sh # `Automated environment setup script`
└── test_environment.py # `Script to validate environment configuration`

---

## Contributing

Branch naming conventions:

feature/<description> 
fix/<description> 
setup/<description>

Contribution workflow:

1-Create a new branch from main
2-Implement the change
3-Run the environment validation
4-Commit changes with clear messages
5-Open a Pull Request for review


On Windows systems, `setup.sh` should be executed using Git Bash, since it does not run directly in CMD or PowerShell.

