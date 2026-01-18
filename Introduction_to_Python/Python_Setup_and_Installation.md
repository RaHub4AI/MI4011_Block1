# `Python` Setup and Installation

Before we start writing `Python` code, you need a working `Python` setup on your own computer. In Block 1, we will work in [`Jupyter notebooks`](https://jupyter.org/).

> #### <img alt="Jupyter logo" src="https://jupyter.org/assets/homepage/main-logo.svg" width="50" /> Why use Jupyter Notebooks?
> 
> Jupyter Notebooks are interactive documents that combine **code, text, equations, and visualizations** in a single file. We use notebooks in this course because:  
> - They provide an *interactive coding environment* ideal for learning and exploration.  
> - Code and results appear together, making workflows *transparent and reproducible*.  
> - Support for `Python` (and many other languages via kernels).  
> - Notebooks can be run in different environments. 
> - Widely used in science and data analysis, so learning them builds transferable skills.  

---

## Recommended ways to install `Python`

There are several ways to install `Python` locally.  
In this course, we **strongly recommend using Anaconda**.

$\color{#ff751f}{\textsf{Stop and check your operating system first!}}$
$\color{#ff751f}{\textsf{Before downloading Anaconda or Python, confirm whether you are on Windows, macOS, or Linux.}}$
$\color{#ff751f}{\textsf{Installing the wrong version is one of the most common causes of setup problems!}}$

### Option 1 (Recommended): Full Anaconda

- Download and install ([instructions](https://www.anaconda.com/docs/getting-started/anaconda/install)) **Anaconda** from https://www.anaconda.com/download 
- Includes **`Python`, `Conda`, and `Jupyter Notebook`** out of the box
- Comes with most scientific packages already installed
- Provides a graphical interface for managing environments and packages

The downside is size. A full Anaconda installation can take up to 3-5 GB of disk space, and additional space will be needed for packages, environments, and data files.  
For most students, this is not a problem and is worth the convenience.


### Option 2: Miniconda (lighter version)

- Download **Miniconda** from https://docs.conda.io/en/latest/miniconda.html
- Installs only **`Python` and `Conda`**
- Takes much less disk space than full Anaconda

You will need to install `Jupyter Notebook` manually:
```bash
conda install jupyter
```
or:  
```bash
pip install notebook
```  
This option is suitable if you want a minimal setup, but it requires more manual steps later.

### Option 3: System `Python` (not recommended for this course)
- Install `Python` directly from https://www.python.org/downloads/.  
- Install `Jupyter Notebook` separately:  
  ```bash
  pip install notebook
  ```
This option is not recommended for this course, because managing packages and environments is error-prone.

---

## Creating Environments
Environments (like `conda` environments or `virtualenvs`) are isolated spaces where you can install packages and libraries without affecting other projects or the system `Python` installation.

Key reasons to use environments:
- Avoid conflicts: Different projects often require different package versions. Environments prevent one project’s dependencies from breaking another.
- Reproducibility: An environment lets you recreate the same setup on another computer or at a later time. This is crucial for research, collaboration, and professional work.
- Course-specific isolation: During this course, we use specific versions of `Python` and various packages. Using a dedicated environment ensures your exercises and homework run exactly as intended.
- Best practice in professional workflows: In industry and academia, maintaining separate environments for each project is the standard. It makes software maintenance, debugging, and collaboration much easier.
- Easy cleanup and updates: When a project ends or requires upgrading packages, you can safely delete or rebuild the environment without breaking anything else on your system.

> Bottom line: Using environments is not just a course requirement, it’s how data scientists and developers manage dependencies and maintain reproducible workflows in real life.

#### Quick Guide
1. Open a `Terminal` (macOS, Linux) or `Anaconda Prompt` (Windows)
2. Create a new environment
   ```bash
   conda create -n modeling_py python=3.13
   ```
   > *Explanation:*\
   > `conda create` creates a new environment\
   > `-n modeling_py` sets the environment name to `modeling_py`\
   > `python=3.13` specifies the `Python` version used in this environment
   > 
   > When prompted, type `y` and press `Enter` to confirm.
3. Activate the environment
   ```bash
   conda activate modeling_py
   ```
   > You should now see `(modeling_py)` at the beginning of the command line.\
   > This indicates that the environment is active.
   >
   > If you do not see the environment name, stop and do not continue. **Ask for help.**
4. Install required packages
   ```bash
   conda install jupyter numpy pandas matplotlib seaborn
   ```
5. Verify the installation by starting Jupyter Notebook
   ```bash
   jupyter notebook
   ```
   > A browser window should open showing the Jupyter interface.\
   > If this happens, your environment is set up correctly.
6. Deactivate/close environment
   ```bash
   conda deactivate
   ``` 
Here is the full documentation on how to manage `conda` environments: https://docs.conda.io/projects/conda/en/4.6.0/user-guide/tasks/manage-environments.html

## Integrated Development Environments (IDEs)

So far, we have seen that we can work with `Jupyter Notebooks` using the Jupyter interface in a web browser.  
However, `Jupyter Notebooks` do not have to be run only this way.

Notebook files (`.ipynb`) can also be opened and executed inside **Integrated Development Environments (IDEs)**. An IDE is an application that helps you write, run, and manage code more efficiently than a basic text editor.

A widely used IDE for `Python` today is **Visual Studio Code (VS Code)**.

VS Code allows you to:
- Open and run `Jupyter Notebooks` directly inside the editor
- Use the same `Conda` environments you created earlier
- Navigate files and folders easily
- Benefit from features like code completion and an integrated terminal

VS Code is free, lightweight, and available on **Windows, macOS, and Linux**. It is widely used in both academia and industry.

You can download Visual Studio Code here: [https://code.visualstudio.com/](https://code.visualstudio.com/Download)

> Using VS Code is **recommended but not required**. You may use the Jupyter interface or another editor if you prefer.

--- 

### Useful materials
<img alt="YT" src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/09/YouTube_full-color_icon_%282017%29.svg/2560px-YouTube_full-color_icon_%282017%29.svg.png" width="15" /> [**Corey Schafer**: *Jupyter Notebook Tutorial: Introduction, Setup, and Walkthrough*](https://www.youtube.com/watch?v=HW29067qVWk&ab_channel=CoreySchafer)

[User-friendly Markdown syntax guide](https://markdownguide.offshoot.io/basic-syntax/)
