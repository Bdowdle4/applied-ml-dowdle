# Dowdle's Module 2 Lab Introduction
In this module, we discussed the process of acquiring and evaluating data.  And we learned some common techniques for cleaning data in preparation to training a model. 

[Clickable Link to Notebook](https://github.com/Bdowdle4/applied-ml-dowdle/blob/main/lab01/ml01.ipynb)

## Virtual Enviornment Set Up (Windows Users)
**Task 1. Create .venv** Run the following command from the project root directory. Use PowerShell (not cmd):

```shell
py -m venv .venv
```

**Accept VS Code Suggestions** If VS Code asks: We noticed a new environment has been created. 
Do you want to select it for the workspace folder? Click Yes. 

**Task 2. Activate** Run the following command from the project root directory. Use Powershell:

```powershell
.venv\Scripts\activate
```

## Run Jupyter Notebook Locally
**Before Starting** Ensure the .venv is activated. If it is already active, you don't need to reactivate it.

**Install the Jupyter Extension for VS Code** Open the Extensions view in VS Code by pressing Ctrl+Shift+X (Windows). Search for "Jupyter" and install the official extension.

**Open the Notebook in VS Code** Open the notebook in VS Code. The file will have a .ipynb extension.

**Task 1. Select Notebook Kernel** Open the project notebook in VS Code. The file will have a .ipynb extension.
- If prompted, select a Python interpreter that corresponds to your .venv.  
- If not prompted, click the kernel selector in the top-right corner of the notebook editor and choose the interpreter associated with your Python Environment / .venv.
- Or:
   - From VS Code Menu, select View / Command Palette... (CTRL SHIFT P)
   - Type: Python: Select Interpreter 
   - Choose your .venv from the list

**Task 2. Start and Run a Jupyter Notebook** Open the project notebook in VS Code. The file will have a .ipynb extension.

1. Execute cells:  
   - Click on a cell and press Shift+Enter to execute it and move to the next cell.  
   - Alternatively, use Ctrl+Enter to execute the current cell without moving.

2. Save your notebook periodically to avoid losing progress. Or make sure the File / Autosave option is on.

**ALWAYS: Fully Execute Notebooks before add-commit-push** Keep your notebooks organized and execute them fully before running git add-commit-push to GitHub.

---

## Overview
Businesses and organizations often need to understand the relationships between different factors to make better decisions.
For example, a company may want to predict the fuel efficiency of a car based on its weight and engine size or estimate home prices based on square footage and location.
Regression analysis helps identify and quantify these relationships between numerical features, providing insights that can be used for forecasting and decision-making.

This project demonstrates your ability to apply regression modeling techniques to a real-world dataset. You will:
- Load and explore a dataset.
- Choose and justify features for predicting a target variable.
- Train a regression model and evaluate performance.
- Compare multiple regression approaches.
- Document your work in a structured Jupyter Notebook.

## Project Outline
Machine learning projects follow a structured approach.
We will use this approach throughout the course. 

Start your notebook professionally with:
- a single top-level title
- your name (or alias)
- the date
- a brief introduction that describes the problem and the dataset.
- Import the external Python libraries used (e.g., pandas, numpy, matplotlib, seaborn, sklearn, etc.)

Present your work in clearly numbered second-level and third-level headings

### Section 1. Load and Explore the Data
- 1.1 Load the dataset and display the first 10 rows.
- 1.2 Check for missing values and display summary statistics.

Analysis: What do you notice about the dataset? Are there any data issues?

### Section 2. Visualize Feature Distributions
- 2.1 Create histograms, boxplots, and scatterplots.
- 2.2 Identify patterns or anomalies in feature distributions.

Analysis: What patterns or anomalies do you see? Do any features stand out?

### Section 3. Feature Selection and Justification
- 3.1 Choose two input features for predicting the target.
- 3.2 Justify your selection with reasoning.

Analysis: Why did you choose these features? How might they impact predictions?

### Section 4. Train a Linear Regression Model
- 4.1 Define X (features) and y (target).
- 4.2 Train a Linear Regression model using Scikit-Learn.
- 4.3 Report R^2, MAE, RMSE.

Analysis: How well did the model perform? Any surprises in the results?

See [EXAMPLE_ANALYSIS](./docs/EXAMPLE_ANALYSIS.md) for more.

---

## Repository Checklist

Verify your repository contains:

- [ ] Useful .gitignore (that keeps .venv out of GitHub)
- [ ] Professional Jupyter Notebook with numbered sections   
- [ ] Useful README.md
- [ ] Useful requirements.txt

Include a professional README.md. Include:
- a personalized title
- an introduction to your project
- a clickable link to your notebook file.
- Instructions on how to set up your virtual environment and run your notebook locally.

---

## Dataset 
Housing Prices Dataset (Predict home values based on features like square footage and location)  
- We use the built-in dataset from scikit-learn:  
   - `from sklearn.datasets import fetch_california_housing`  
- Additional dataset available on Kaggle:  
   - [Kaggle Housing Prices](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)  

--- 

## Python Library for Machine Learning: scikit-learn
We use scikit-learn, built on NumPy, SciPy, and matplotlib
   - Read more at <https://scikit-learn.org/>
   - Scikit-learn supports classification, regression, and clustering.
   - This project applies regression.

**Important:** Use a 2-step installation to avoid timeouts and partial installs:  
1. **First Install:** Install from `requirements.txt` with `scikit-learn` commented out.  
2. **Second Install:** Uncomment `scikit-learn` and rerun the install command.

---

## Professional Python Setup and Workflow
We follow professional Python practices. 
Full instructions are available at <https://github.com/denisecase/pro-analytics-01/>. 
A concise version is provided at [WORKFLOW_GUIDE.md](./docs/WORKFLOW_GUIDE.md)

**Important:** VS Code + Pylance may fail to recognize installed packages in Jupyter notebooks.  
See the above guides for troubleshooting and solutions.  

---