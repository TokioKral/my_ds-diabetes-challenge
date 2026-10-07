# Diabetes Challenge

After learning several algorithms for classification problems, it is time to put them to work on new data and compare how they perform. In this challenge you pull the diabetes data from a database, explore it, and build models that predict whether a patient has diabetes. You decide which evaluation metric matters here, tune your models, and reason about how to handle imbalanced classes.

## Learning Objectives

By the end of this repository, you should be able to:

- Fetch and join the diabetes data from a SQL database to assemble a training set.
- Explore the data and explain what the tables represent and how they relate.
- Train and compare at least two classification algorithms on the same problem.
- Choose an evaluation metric that fits the problem, and justify the choice.
- Tune hyperparameters with grid search and randomized search.
- Reason about imbalanced classes and apply techniques to address them.

## Learning Path

> [!TIP]
> Start with the [**Machine Learning Workflow**](machine_learning_workflow.md) guide. It walks through every step of an ML project (define the goal, get the data, split, explore, model, evaluate) and gives you the map for what the challenge asks you to do.

| File / Folder | Description |
|---|---|
| [**The Machine Learning Workflow**](machine_learning_workflow.md) | Step-by-step overview of an end-to-end ML project. Read this first. |
| [**1 - Diabetes Challenge**](1_diabetes_challenge.ipynb) | The challenge: load the data from the database, explore it, and build and tune classifiers to predict diabetes. |

### Additional Folders and Files

| File / Folder | Description |
|---|---|
| [**Assets**](assets/) | Images used in the workflow guide. |
| [**Solutions**](solutions/) | Reference solutions. |
| [**Paper on the Diabetes Mellitus Data Set**](paper_on_diabetes_mellitus_data_set.pdf) | Background paper on the dataset. |
| [**.env.example**](.env.example) | Template for the database credentials. Copy to `.env` and fill in your values. |
| [**pyproject.toml**](pyproject.toml) | Project configuration and dependencies. |
| [**uv.lock**](uv.lock) | Dependency lock file. |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a **placeholder**. Replace it including the `< >` brackets with your own value. For example, `cd <repo-name>` becomes `cd ds-diabetes-challenge`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

This installs all dependencies and creates a virtual environment in (`.venv/`).

```bash
cd <repo-name>
uv sync
```

---

### 5. Set Up the Database Connection

The challenge reads its data from a Postgres database (the `diabetes` schema) via a connection string. Copy the example file and fill in your own values:

```bash
cp .env.example .env
```

Then open `.env` and replace the placeholders with the values from your coaches.

> [!CAUTION]
> The `.env` file holds credentials and must never be committed. It is already listed in `.gitignore`. Only `.env.example`, with placeholders, belongs in the repo.

---

### 6. Open the Notebook

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the environment created by `uv sync`.

Launch VS Code in the project root folder:

```bash
code .
```

Then open the notebook and select the Python environment created by `uv sync` as the kernel.

## References & Further Reading

- [**The Machine Learning Workflow**](machine_learning_workflow.md): The step-by-step guide in this repo, your starting point.
- [**Pima Indians Diabetes Database**](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database): The original dataset on Kaggle, with column descriptions.
- [**Scikit-learn: Tuning hyperparameters**](https://scikit-learn.org/stable/modules/grid_search.html): Grid search, randomized search, and successive halving.
- [**Scikit-learn: Cross-validation**](https://scikit-learn.org/stable/modules/cross_validation.html): Evaluating estimator performance and avoiding overfitting.
- [**Scikit-learn: Precision-Recall**](https://scikit-learn.org/stable/auto_examples/model_selection/plot_precision_recall.html): Choosing and reading classification metrics.
- [**8 Tactics to Combat Imbalanced Classes**](https://machinelearningmastery.com/tactics-to-combat-imbalanced-classes-in-your-machine-learning-dataset/): Practical strategies for imbalanced classification.
- [**Imbalanced-learn**](https://imbalanced-learn.org/stable/): Library of resampling tools for imbalanced datasets.
