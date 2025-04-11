# Dowdle's Module 5 Lab Introduction
In this module, we will look at how we can combine an ensemble of models to achieve better performance. We will look at serial and parallel combinations of models, the problems with data sets that contain a high number of features, and techniques for reducing the dimensionality of the data. We will look at some prebuilt models that use decision trees as their basic components. Common types of ensemble models include:

- Boosted Decision Trees – Models train sequentially, with each new tree correcting the errors of the previous one.
- Random Forest – Multiple decision trees train in parallel, each on a random subset of the data, and their predictions are averaged.
- Voting Classifier (Heterogeneous Models) – Combines different types of models (e.g., Decision Tree, SVM, and Neural Network) by taking the majority vote or average prediction.
- Cross Validation – Divides data into multiple folds to improve the reliability of performance estimates.

[Clickable Link to Notebook](https://github.com/Bdowdle4/applied-ml-dowdle/blob/main/lab05/ensemble-dowdle.ipynb)

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

Analysis: What patterns or anomalies do you see? Do any features stand out?

### Section 3. Feature Selection and Justification

Analysis: Why did you choose these features? How might they impact predictions?

### Section 4. Split the Data into Train and Test Sets

Analysis: Did the sets split properly? Is there any data leakage?

### Section 5. Evaluate Model Performance (Choose 2)
- Random Forest (200, max depth=10)
- Gradient Boosting(100)

### Section 6. Compare Results

Analysis: How well did each model perform? Are there any surprising results? Why might one model outperform the others?

### Section 7. Conclusions and Insights

Analysis: Base all your reasoning on data. Feel free to tune parameters if you like. List the next steps you'd like to try if you were in a competition to build the best predictor.


| Model | Train Accuracy | Test Accuracy | Train F1 | Test F1 | Accuracy Gap | F1 Gap |
|-------|-----------|---------------|----------|-----------|--------|--------|
| Random Forest (200, max depth=10) | 0.972401 | 0.845588 | 0.971256 | 0.803440 | 0.126813 | 0.167816 |
| Gradient Boosting (100) | 0.959522 | 0.827206| 0.957773 | 0.804395| 0.132316 | 0.153379 |

---

## Repository Checklist

Verify your repository contains:

- [x] Useful .gitignore (that keeps .venv out of GitHub)
- [ ] Professional Jupyter Notebook with numbered sections   
- [x] Useful README.md
- [x] Useful requirements.txt

Include a professional README.md. Include:
- a personalized title
- an introduction to your project
- a clickable link to your notebook file.
- Instructions on how to set up your virtual environment and run your notebook locally.

---

## Dataset 
Wine Quality Dataset (Red wine samples from the north of Portugal. The goal is to model wine quality based on physicochemical tests)

Features included in this dataset: 
1. fixed acidity     mostly tartaric acid
2. volatile acidity  mostly acetic acid (vinegar)
3. citric acid       can add freshness and flavor
4. residual sugar    remaining sugar after fermentation
5. chlorides         salt content
6. free sulfur dioxide  protects wine from microbes
7. total sulfur dioxide sum of free and bound forms
8. density           related to sugar content
9. pH                acidity level (lower = more acidic)
10. sulphates        antioxidant and microbial stabilizer
11. alcohol          % alcohol by volume

The target variable is:   
quality (integer score from 0 to 10, rated by wine tasters)

- If you have a direct link to the CSV file, use:
  ```
  wget https://example.com/path/to/your.csv -P /path/to/your/project/folder
  ```
- If you already have the file downloaded copy the file, use:
  ```
  cp "C:\Example\Path\to\Your\File.csv" "C:\Path\to\Desitnation" 
  ```

- Additional dataset available on UCI Machine Learning Repository:
   [Wine Quality Dataset](https://archive.ics.uci.edu/dataset/186/wine+quality)

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