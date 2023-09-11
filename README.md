# Introduction to Jupyter Notebooks in VS Code

- [GitHub Repository](https://github.com/denisecase/datafun-04-notebooks/)

Jupyter Notebooks are a popular way to create and share documents for data analytics. They are interactive, easy to share, and support a wide variety of data science tools.

## Step 1: Open The Project Folder

Open VS Code and clone your `datafun-04-notebooks` repository to your machine.

## Step 2: Update Default Python

Open a terminal in VS Code. Use the menu View / Terminal. 
In Windows, use PowerShell, in Mac, use bash.
Verify you've added some essential packages to your default Python environment.

```shell
python -m pip install --upgrade pip ipykernel jupyterlab
python -m pip install --upgrade black ruff
```

Note: If `py` or `python3` works on your machine, use that instead of `python` in the commands.

-----

## Step 3: Add Common Files

When starting a new project, there are some common files you should add to the project folder.

### Add .gitignore

- The .gitignore file tells Git files to ignore when committing changes.
- Review the [gitignore](gitignore) file, you can use it without modification.

### Modify README.md

- Learn to edit and customize README.md files, which provide a quick overview of the project and instructions for running it. 

### Scan requirements.txt

- The requirements.txt file lists the packages used in the project.
- You may not use all them and may want to add others. Modify this list as you like. 

🚀 Rocket Tip: When employers ask for years of experience with a language, it's not the syntax - that's learned in a few days. It's the experience with the tools, libraries, and frameworks that takes time.

-----

## Step 4: Set up a Virtual Environment

Next, we'll create and activate a virtual environment specifically for this project. We'll also install additional packages required for this project.

### Create a Virtual Environment

1. Open the terminal in VS Code. (View / Terminal)
2. Run the following command to **create** a virtual environment for this project.

```shell
python -m venv .venv
```

Verify that a new `.venv` folder was created. It may take a while for the command to complete.

🚀 Rocket Tip: When VS Code Python Extension offers to select the Environment, say Yes.

### Activate the Virtual Environment

Wait for the creation to finish, then **activate** the virtual environment:

- For PowerShell: `.venv\Scripts\Activate`
- For macOS/Linux:  `source .venv/bin/`

🚀 Rocket Tip: Notice the terminal changes to reflect the active virtual environment.

### Install Dependencies to the Active Virtual Environment

Install additional project dependencies into the active virtual environment.
The packages ipykernel and jupyterlab are required to run a notebook.
The packages pandas, matplotlib, and seaborn are used to work with data and charts.

```shell
python -m pip install --upgrade pip ipykernel jupyterlab
python -m pip install --upgrade pandas matplotlib seaborn
python -m pip install --upgrade voila
```

Alternatively, you can install all the packages listed in the requirements.txt file.

```shell
python -m pip install --upgrade -r requirements.txt
```

Note: The `--upgrade` parameter gets the latest version of each package.

-----

## Step 5: Working with Notebooks

In the active virtual environment, create a Python kernel to run our notebooks. 

```shell
python -m ipykernel install --user --name .venv --display-name "Python (.venv)"
```

### Create a new notebook

In VS Code, from the menu, select View / Command Palette.
Type `notebook` and select `Jupyter: Create New Blank Notebook`.
This will create a new notebook in the project folder.
Save the notebook with a name like `yourname-notebook.ipynb`.


-----
If you've created the .venv virtual environment,  installed the necessary packages, 
and selected a Kernel for your Jupyter Notebook, it should run - 
even if the code shows a missing package error. See the image below.

![Check Kernel and .venv. VS Code may show an issue, but may still work](images/VSCode-SelectKernel-AndInstallPkgs-Then-It-Should-Run-Even-With-NotFound-Issue.PNG)

Focus of this module is to learn about:
array-oriented programming with NumPy and diving into the depths of strings

Explore Chapter 7 - Array-Oriented Programming with NumPy
Explore Chapter 8 - Strings: A Deeper Look

Contrary to the names of the chapters, the most generally useful things here are:

Jupyter - a browser-based environment for processing and presenting analytics. 
We use Jupyter (and the integrated Python and Markup languages) to "tell a story with data"
Jupyter notebooks (.ipynb) are great for all steps in a data analytics project:
Defining the question.
Collecting the data.
Exploring and cleaning the data.
Processing and analyzing the data.
Visualizing, reporting, and sharing your results.
The pandas library is widely used. 
The pandas library gives us a Series (for one dimensional data)
It also provides the pandas DataFrame for two-dimensional data (like a spreadsheet). 
It makes it easy to read from files, explore data, and provides a foundation for visualization (e.g., with matplotlib and seaborn).
To get access to these tools, we'll go beyond the Python Standard Library and install additional, external libraries. 
Before we can import them, we must first download and install them into our active Python environment (if using conda, this is typically the 'base' or default environment).
It's possible to have many different Python virtual environments, each with a specific Python version and set of libraries installed. In this course we just use base - do a web search to learn more. 