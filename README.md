# Salary Prediction with Random Forest Regression

## Problem Statement and Goal of Project
The goal of this project is to predict employee salaries based on their position level using a Random Forest Regressor. The objective is to accurately estimate salaries for given job levels, which can assist organizations in setting fair compensation structures. This model demonstrates the application of regression techniques to a small, non-linear dataset.

## Solution Approach
The solution leverages a **Random Forest Regressor** to predict salaries based on position levels. The approach includes the following steps:
1. **Data Preparation**:
   - Extract the `Level` (independent variable) and `Salary` (dependent variable) from the dataset.
   - The `Position` column is excluded as it is redundant with `Level`.
2. **Model Training**:
   - Train Random Forest Regressor models with varying numbers of trees (10 and 300) to explore the impact of ensemble size on prediction accuracy.
   - Use `random_state=0` for reproducibility.
3. **Prediction**:
   - Predict the salary for a position level of 6.5 to evaluate model performance.
4. **Visualization**:
   - Create a scatter plot of actual data points and a smooth prediction curve to visualize the relationship between position level and salary.
   - The plot helps assess the model's ability to capture non-linear patterns in the data.

## Technologies & Libraries
The project is implemented in Python within a Jupyter Notebook environment, using the following libraries:
- **Pandas**: For data loading and manipulation.
- **NumPy**: For numerical operations and array handling.
- **Matplotlib** and **Seaborn**: For data visualization, including scatter plots and prediction curves.
- **Scikit-learn**: For implementing the Random Forest Regressor.
- **Jupyter Notebook**: For interactive development and visualization.

## Description about Dataset
The dataset, stored in `Position_Salaries.csv`, contains 10 entries with 3 columns:
- **Position**: Job title (e.g., Business Analyst, CEO), not used in modeling.
- **Level**: Position level (1 to 10), used as the independent variable.
- **Salary**: Annual salary in dollars (ranging from 45,000 to 1,000,000), used as the dependent variable.
The dataset has no missing values and is small, making it suitable for demonstrating regression techniques on non-linear data.

## Installation & Execution Guide
To run this project locally, follow these steps:
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/imehranasgari/salary-prediction-random-forest.git
   cd salary-prediction-random-forest
   ```
2. **Set Up a Virtual Environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. **Install Dependencies**:
   Ensure you have Python 3.11 installed, then run:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```
4. **Run the Jupyter Notebook**:
   ```bash
   jupyter notebook "Random Forest (Regression).ipynb"
   ```
5. **Dataset Requirement**:
   - Place the `Position_Salaries.csv` file in the same directory as the notebook.
   - The dataset should match the structure described above.

## Key Results / Performance
- The Random Forest Regressor was trained with 10 and 300 trees to predict the salary for a position level of 6.5:
  - **10 trees**: Predicted salary of $167,000.
  - **300 trees**: Predicted salary of $160,333.33.
- The notebook notes that increasing the number of trees (from 10 to 300) improves prediction accuracy, as the 300-tree model provides a more stable estimate.
- **Note**: The project focuses on exploring the Random Forest algorithm rather than optimizing performance metrics (e.g., RMSE). No train-test split was performed due to the small dataset size, emphasizing model understanding over evaluation.

## Screenshots / Sample Outputs
The notebook generates a scatter plot with a smooth prediction curve:
- **Plot Description**:
  - Red dots represent actual salary data points for each position level.
  - A blue curve shows the Random Forest predictions for a high-resolution grid of position levels (0.01 increments).
  - The plot, titled "Truth or Bluff (Random Forest - Smooth)," visualizes the non-linear relationship between position level and salary.
  - **Note**: The plot may not render correctly on GitHub. Please view the notebook via [nbviewer.org](https://nbviewer.org) for full visualization.

## Additional Learnings / Reflections
This project provided valuable insights into applying Random Forest Regression to a small, non-linear dataset:
- **Model Exploration**: Experimenting with different numbers of trees (10 vs. 300) highlighted the impact of ensemble size on prediction stability, reinforcing the importance of hyperparameter tuning.
- **Non-linear Modeling**: Learned how Random Forest captures complex, non-linear relationships, which is critical for datasets like this where salary does not scale linearly with position level.
- **Visualization Skills**: Gained experience in creating high-resolution visualizations to effectively communicate model predictions.
- **Exploratory Focus**: The project demonstrates my ability to understand and apply machine learning techniques, even with a simple dataset, showcasing my curiosity and technical proficiency in regression modeling.

This work reflects my skills in implementing and interpreting machine learning models, making it a strong addition to my portfolio for data science and AI roles.

## 👤 Author
**Mehran Asgari**  
**Email**: [imehr9@gmail.com](mailto:imehr9@gmail.com)  
**GitHub**: [https://github.com/imehranasgari](https://github.com/imehranasgari)

## 📄 License
This project is licensed under the Apache 2.0 License – see the `LICENSE` file for details.

> 💡 *Some interactive outputs (e.g., plots, widgets) may not display correctly on GitHub. If so, please view this notebook via [nbviewer.org](https://nbviewer.org) for full rendering.*
