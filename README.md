ACIS Insurance Risk Analytics & Predictive Modeling


This repository contains the end-to-end analysis for the B5W3 Insurance Risk Analytics challenge. The project analyzes a historical car insurance dataset from AlphaCare Insurance Solutions (ACIS) to optimize marketing strategies, identify low-risk customer segments, and build predictive models for premium calculation.
🎯 Business Objective

The primary goal is to leverage data analytics to enhance ACIS's marketing and pricing strategies in the South African car insurance market. This involves:

    Analyzing historical claim data to understand risk drivers.

    Discovering "low-risk" customer segments where premiums could be competitively reduced to attract new clients.

    Building a predictive modeling framework to estimate claim probability and severity, forming the basis for a dynamic pricing system.

📊 Key Insights from Exploratory Data Analysis (Task 1)

Our initial exploration of the dataset (Feb 2014 - Aug 2015) has already revealed several actionable insights:

    Geographic Risk Disparity: There is a significant variation in the Loss Ratio (Total Claims / Total Premium) across different provinces. Certain provinces are far more profitable than others, suggesting a need for region-specific premium adjustments.

    High-Risk Vehicle Profiles: Specific vehicle makes are associated with a much higher Loss Ratio than the portfolio average. This provides a clear opportunity to refine underwriting rules and premium calculations based on the vehicle being insured.

    Highly Skewed Financials: Both TotalPremium and TotalClaims distributions are heavily right-skewed, with high-value outliers. This confirms that a small percentage of policies and claims have a disproportionately large financial impact, a typical characteristic of insurance data.

🛠️ Tech Stack & Tools

    Data Manipulation & Analysis: Python, Pandas, NumPy

    Data Visualization: Matplotlib, Seaborn

    Development Environment: Jupyter Lab, Visual Studio Code

    Version Control: Git, GitHub

    Data Versioning: DVC (Data Version Control)

    CI/CD: GitHub Actions

    Modeling (Planned): Scikit-learn, XGBoost, SHAP

📂 Project Structure

The project follows a modular and reproducible structure:

      
acis-insurance-analytics/
├── .dvc/                   # DVC metadata
├── .github/
│   └── workflows/
│       └── ci.yml          # CI/CD workflow for automated code quality checks
├── data/
│   ├── processed/          # Cleaned and transformed data
│   └── raw/                # Original, immutable raw dataset
├── models/                 # Saved (serialized) machine learning models
├── notebooks/              # Jupyter notebooks for analysis
│   ├── 01_EDA.ipynb
│   └── ...
├── reports/
│   └── figures/            # Plots and charts for the final report
├── src/                    # Reusable Python source code (e.g., data processing)
├── .gitignore              # Files to be ignored by Git
├── README.md               # This file
└── requirements.txt        # Python package dependencies

    

IGNORE_WHEN_COPYING_START
Use code with caution.
IGNORE_WHEN_COPYING_END
⚙️ Setup and Installation

To get a local copy up and running, follow these simple steps.

    Clone the repository:

          
    git clone https://github.com/foziyaa/acis-insurance-analytics.git
    cd acis-insurance-analytics

        

    IGNORE_WHEN_COPYING_START

Use code with caution. Bash
IGNORE_WHEN_COPYING_END

Create and activate a Python virtual environment:

      
# Create the environment
python -m venv .venv

# Activate it (on Windows Git Bash)
source .venv/Scripts/activate

# On MacOS/Linux
# source .venv/bin/activate

    

IGNORE_WHEN_COPYING_START
Use code with caution. Bash
IGNORE_WHEN_COPYING_END

Install the required dependencies:

      
pip install -r requirements.txt

    

IGNORE_WHEN_COPYING_START
Use code with caution. Bash
IGNORE_WHEN_COPYING_END

Retrieve the data (using DVC):
Note: This step will be implemented in Task 2. DVC must be configured first.

      
dvc pull

    

IGNORE_WHEN_COPYING_START

    Use code with caution. Bash
    IGNORE_WHEN_COPYING_END

🚀 How to Run

All analyses are conducted within the Jupyter notebooks located in the notebooks/ directory.

    Launch Jupyter Lab from your terminal:

          
    jupyter lab

        

    IGNORE_WHEN_COPYING_START

    Use code with caution. Bash
    IGNORE_WHEN_COPYING_END

    Navigate to notebooks/ and open the desired notebook (e.g., 01_EDA.ipynb) to view and run the analysis.

📈 Next Steps

This project is being developed in stages:

    Task 1: Foundational EDA & Project Setup

    Task 2: Data Versioning with DVC

    Task 3: A/B Hypothesis Testing

    Task 4: Predictive Modeling & Interpretation

Author: Foziya Fetudin

   github.com/foziyaa