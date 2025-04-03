# Dowdle's Module 4 Lab Introduction
In this module, we will look at how three basic kinds of classifiers (Decision Trees, Support Vector Machines, and Neural Nets) work and see how we can grade the performance of a classifier. One popular machine learning task is to predict a target that has category information. We learned how to compare and characterize the performance of a classifier to describe how model performance can be affected by internal parameter choice.

[Clickable Link to Notebook](https://github.com/Bdowdle4/applied-ml-dowdle/blob/main/lab03/ml03_dowdle.ipynb)

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
Businesses and organizations often need to categorize data to make informed decisions. For example, a company may want to predict whether a customer will purchase a product based on their browsing behavior or determine if an email is spam based on its content. Classification analysis helps identify patterns and assign labels to data points, enabling accurate predictions and informed decision-making.

This project demonstrates your ability to apply classification techniques to a real-world dataset. You will:
- Load and explore a dataset.
- Choose and justify features for predicting a target variable.
- Train a classification model and evaluate performance.
- Compare multiple classification approaches.
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

### Section 1. Import and Inspect the Data
What methods do you already know to inspect the data? Use these common methods every time you load a new dataset.

Analysis: What do you notice about the dataset? Are there any data issues?

### Section 2. Data Exploration and Preparation
- 2.1 Handle Missing Values and Clean Data
- 2.2 Feature Engineering

Analysis: What patterns or anomalies do you see? Do any features stand out?

### Section 3. Feature Selection and Justification
- 3.1 Choose features and target
- 3.2 Define X and y

Analysis: Why did you choose these features? How might they impact predictions?

### Section 4. Train a Classification Model (Decision Tree)
- 4.1 Split the Data
- 4.2 Create and Train Model (Decision Tree)
- 4.3 Predict and Evaluate Model Performance
- 4.4 Report Confusion Matrix (as a heatmap)
- 4.5 Report Decision Tree Plot
  
 Repeat for all three cases 

Analysis: How well did the different cases perform? Are there any surprising results? Which inputs worked better? 

### Section 5. Compare Alternative Models (SVC, NN)
- 5.1 Train and Evaluate Model (SVC)
- 5.2 Train and Evaluate Model (NN MLP)
  
Analysis: How well did each model perform? Are there any surprising results? Why might one model outperform the others?

### Section 6. Final Thoughts & Insights
- 6.1 Summarize Findings
- 6.2 Discuss Challenges Faced
- 6.3 Next Steps

| Model Type | Case | Features Used | Accuracy | Precision | Recall | F1-Score | Notes |
|------------|------|---------------|----------|-----------|--------|-----------|-------|
| **Decision Tree** | Case 1 | alone | 63% | 64% | 63% | 63% | - |
|                   | Case 2 | age | 61% | 58% | 61% | 55% | - |
|                   | Case 3 | age + family_size | 59% | 57% | 59% | 58% | - |
| **SVM (RBF Kernel)** | Case 1 | alone | 63% | 64% | 63% | 63% | - |
|                    | Case 2 | age | 63% | 66% | 63% | 52% | - |
|                    | Case 3 | age + family_size | 63% | 66% | 63% | 52% | - |
| **SVM (Linear Kernel)** | Case 1 | alone | 63% | 64% | 63% | 63% | - |
|                    | Case 2 | age | 63% | 66% | 63% | 52% | - |
|                    | Case 3 | age + family_size | 63% | 66% | 63% | 52% | - |
| **SVM (Poly Kernel)** | Case 1 | alone | 63% | 64% | 63% | 63% | - |
|                    | Case 2 | age | 63% | 66% | 63% | 52% | - |
|                    | Case 3 | age + family_size | 63% | 66% | 63% | 52% | - |
| **SVM (Sigmoid Kernel)** | Case 1 | alone | 63% | 64% | 63% | 63% | - |
|                    | Case 2 | age | 63% | 66% | 63% | 52% | - |
|                    | Case 3 | age + family_size | 63% | 66% | 63% | 52% | - |
| **Neural Network (MLP)** | Case 1 | alone | 63% | 64% | 63% | 63% | - |
|                    | Case 2 | age | 62% | 64% | 62% | 49% | - |
|                    | Case 3 | age + family_size | 69% | 68% | 69% | 67% | - |

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
Titanic Dataset (Predict survival based on passenger features like age, gender, and class)

- We use the built-in dataset from Seaborn:
   ```
   import seaborn as sns
   titanic = sns.load_dataset("titanic")
   ```
- Additional dataset available on Kaggle:
   [Kaggle Titanic](https://www.kaggle.com/datasets/akshaysehgal/titanic-data-for-data-preprocessing)

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