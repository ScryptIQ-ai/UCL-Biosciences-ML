# Supervised Machine Learning with L2D

Welcome to this introductory teaching module in machine learning for bio-scientists from [Learn to Discover](https://learntodiscover.ai/) in partnership with UCL.

The code for this project is in three notebooks: 
1. [Data exploration](1_data_explore.ipynb)
2. [Classical ML](2_supervised_ml.ipynb)

## Setup

To use the code in this repository you'll need to perform the following steps:
- install `uv` (another environment and package manager, along with Python)
- clone the repository
- create a virtual environment and install the dependencies 
- open the notebook in the virtual environment

### Install uv

If you're using Mac or Linux, you should already have some version of Python installed. It's [important to keep this project separate](https://aibio.ac.uk/blog/why-do-we-use-python-environments/) from your main, system Python. There are various ways to do this, there are several related tasks: 
- installing and managing versions of the Python interpreter
- creating environments to insulate the system and projects from each other 
- installing and managing dependencies

`uv` does all of these. Note: If you're already familiar with all of these concepts and prefer to use other tools then you don't have to install `uv`. We're using it here as it's the simplest way we've found to perform all the above tasks. 

You can find installation instructions for all systems [here](https://docs.astral.sh/uv/getting-started/installation/#standalone-installer).

### Clone the repository

If you don't already have Git installed, follow [these instructions](https://github.com/git-guides/install-git). 

Once you have Git installed and working, navigate to the directory where you keep your projects and run:

```
git clone https://github.com/ScryptIQ-ai/UCL-Biosciences-ML.git
```

This should create a new directory called `UCL-Biosciences-ML` in the location you run the command from, and download the contents of the repository into it. You should now have the following files:

```
AIBio-demo
├── 1_data_explore.ipynb
├── 2_ml.ipynb
├── assets
│   └── fna_pic.png
├── data
│   └── breast_cancer.csv
├── pyproject.toml
├── README.md
└── uv.lock
```

Along with some hidden files. 

### Create an environment and install the dependencies 

Navigate into the repository directory (`UCL-Biosciences-ML`) and run:

```
uv sync
```

This small command does a bunch of useful things. The repository contains files, `pyproject.toml` and `uv.lock`, that specify the project's dependencies. `uv` reads these files, creates a virtual environment if necessary, and installs the dependencies into the environment. See the [`uv` docs](https://docs.astral.sh/uv/guides/projects/) for more information. 

### Open the notebook in the virtual environment

You can now open one of the notebooks in your IDE of choice or launch a jupyter notebook straight away using the terminal commands below:

```
uv run --with jupyter jupyter lab
```

This launches a Jupyter server and automatically opens a browser window at the right address. You should now be ready to start running code!