# Project Management Data Analysis

This repository contains a synthetic dataset and an analysis notebook aimed at showcasing business analytics, data analytics, and program management skills. The project demonstrates how to generate realistic project management data, explore it visually, and build predictive models to classify project outcomes.

## About the Project

Modern organisations collect a wealth of data about their projects: budgets, timelines, team sizes, risk assessments and stakeholder feedback. Analysts and program managers use this information to understand what drives success and where interventions are needed. This repository offers a complete, ready‑to‑use example that you can run locally or in a hosted environment to practice:

* Generating a realistic dataset for project management scenarios.
* Performing exploratory data analysis (EDA) with tables and visualisations.
* Building and evaluating predictive models to classify project outcomes.

The repository is designed to be accessible to beginners while also offering opportunities to extend the analysis or experiment with more advanced techniques.

## Dataset

The data in `project_data.csv` consists of **500 synthetic projects** and the following fields:

| Column                   | Description                                                |
|-------------------------|------------------------------------------------------------|
| `Project_ID`            | Unique identifier for each project (e.g. `PRJ0001`).       |
| `Project_Type`          | Category of project (`Software Development`, `Marketing`, `Data Analytics`, `Infrastructure`, `Research`). |
| `Start_Date`            | Start date of the project.                                 |
| `End_Date`              | End date of the project.                                   |
| `Duration_Days`         | Project duration in days.                                  |
| `Budget_KUSD`           | Planned budget in thousand USD.                            |
| `Actual_Cost_KUSD`      | Actual cost in thousand USD (may differ from budget).      |
| `Team_Size`             | Number of people assigned to the project.                  |
| `Risk_Score`            | Overall risk score from 1 (low) to 10 (high).              |
| `Stakeholder_Satisfaction` | Stakeholder satisfaction score from 1 (low) to 10 (high). |
| `Outcome`               | Binary label indicating project success (`1`) or failure (`0`). |

These values were generated using parametric distributions and heuristics to capture realistic relationships (for example, overspending often leads to lower satisfaction, and high risk increases failure probability). The dataset can be regenerated programmatically; the code used to create it is documented in the notebook.

## Repository Structure

- `project_data.csv` – synthetic dataset described above.
- `analysis.ipynb` – Jupyter notebook that loads the dataset, performs EDA, visualises distributions and correlations, and fits logistic regression and random forest models.
- `requirements.txt` – Python dependencies needed to run the notebook.
- `README.md` – this file.

## Getting Started

To run the analysis on your own machine:

1. **Clone this repository** or download the files.

2. **Install dependencies** using `pip`. It is recommended to use a virtual environment.

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows use .\.venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Start Jupyter** and open the notebook.

   ```bash
   jupyter notebook analysis.ipynb
   ```

4. **Run the notebook cells** sequentially to reproduce the figures and model results.

## Usage and Next Steps

The analysis notebook guides you through loading the data, inspecting it, visualising distributions, and building baseline predictive models. The logistic regression and random forest classifiers provide starting points for classification tasks. Here are some ideas to extend the project:

- **Feature engineering** – derive additional features such as cost overrun percentage, average budget per team member, or encode temporal information like year and quarter.
- **Hyper‑parameter tuning** – experiment with grid search or cross‑validation to optimise the random forest or try gradient boosting methods.
- **Regression analysis** – predict continuous outcomes such as stakeholder satisfaction using linear regression or more advanced algorithms.
- **Dashboard development** – build an interactive dashboard using Plotly Dash, Streamlit or a BI tool to visualise project metrics and predictions.
- **Deploy models** – wrap the model into an API or integrate it into a business workflow to support program management decisions.

This repository serves as a portfolio‑ready example for business analyst, program manager and data analyst roles. Feel free to fork it, extend it and showcase your own improvements.

## License

This project is released under the MIT License.
