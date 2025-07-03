# Insurance Risk Analytics

This repository contains code and analysis for the 10 Academy Week 1 Challenge, focusing on insurance risk analytics using Python, with exploratory data analysis (EDA), data versioning, hypothesis testing, and predictive modeling.

## Setup
1. Clone the repo: `git clone https://github.com/Bisrath1/Insurance-risk-analytics.git`
2. Create virtual environment: `python3 -m venv venv`
3. Activate:
   - On Unix/Linux/MacOS: `source venv/bin/activate`
   - On Windows: `venv\Scripts\activate`
4. Install dependencies: `pip install -r requirements.txt`

## Structure
- **.dvc/**: Configuration for DVC local remote storage.
- **SM/data/**: Synthetic claims dataset managed with DVC.
- **data/**: Insurance datasets (`insurance.csv`, `insurance_v2.csv`) versioned with DVC.
- **figures/**: Visualizations from modeling and analysis (e.g., SHAP plots).
- **notebooks/**: Jupyter notebooks for EDA and analysis.
- **results/**: Outputs from regression and classification models with SHAP analysis.
- **src/**: Python scripts for reusable code (e.g., modeling, data processing).
- **task_3_hypothesis_testing/**: Scripts and results for A/B testing.
- **.dvcignore**: Files/folders excluded from DVC tracking.
- **LICENSE**: MIT License for the project.
- **requirements.txt**: Python dependencies, including DVC.

## Progress
- **Task 1: Git and EDA**
  - Set up repository: `https://github.com/Bisrath1/Insurance-risk-analytics`.
  - Performed EDA on `insurance.csv`, analyzing charges by region, sex, and smoker status (branch: `task-1`).
- **Task 2: DVC**
  - Initialized DVC for data version control.
  - Versioned `insurance.csv` and `insurance_v2.csv` using DVC.
  - Configured local DVC remote storage.
  - Added synthetic claims dataset to `SM/data/` (commit: 3 weeks ago).
- **Task 3: A/B Testing**
  - Conducted hypothesis testing on insurance charges by region and sex (branch: `task-3`).
  - Findings: Significant differences in charges observed in the southeast region (details in `task_3_hypothesis_testing/`).
- **Task 4: Modeling**
  - Built regression and classification models for claim severity, premium, and claim probability (branch: `task-4`, merged in commit: 3 weeks ago).
  - Best model: XGBoost (RMSE: X, R²: Y).
  - SHAP analysis: Smoker status and age identified as most influential features (visualizations in `figures/`).

## Usage
- Run Jupyter notebooks for EDA and visualizations:
  ```bash
  jupyter lab
  ```
- Fetch versioned data with DVC:
  ```bash
  dvc pull
  ```
- Execute modeling scripts:
  ```bash
  python src/models.py
  ```
- Run hypothesis tests:
  ```bash
  python task_3_hypothesis_testing/run_tests.py
  ```

## Recommendations
- Adjust insurance premiums for smokers and high-risk regions based on EDA and modeling insights.
- Implement claim probability model for risk-based pricing strategies.

## Contributing
1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-branch`
3. Commit changes: `git commit -m "Add feature"`
4. Push to the branch: `git push origin feature-branch`
5. Open a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

## Contact
Maintained by [Bisrath1](https://github.com/Bisrath1). For questions or feedback, open a GitHub issue or contact the owner directly.
