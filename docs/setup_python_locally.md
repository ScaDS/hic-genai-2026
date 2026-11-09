# Setting up your computer

One way of setting up reproducible coding environments, is by managing *Conda* environments ([read more](https://focalplane.biologists.com/2022/12/08/managing-scientific-python-environments-using-conda-mamba-and-friends/))

## Step 1: Install Mini-forge
Download and install Conda. We recommend the Conda distribution [mini-forge](https://conda-forge.org/download/).

For ease-of-use, it is recommended to install it for your use only and to add Conda to the PATH variable during installation.

![img.png](images/miniforge1.png)

![img.png](images/miniforge2.png)

## Step 2: Install Python and libraries

After Conda installation finished, use this command from the terminal:

```
conda create --name llm-da python=3.11 -c conda-forge
```

Afterwards, activate the environment:

```
conda activate llm-da
```

Install the libraries we plan to use during the training:
```
pip install bia-bob numpy scipy pandas scikit-learn scikit-image jupyterlab seaborn cellpose stackview
```

## Step 3: Testing the installation

Whenever you want to work on the same project, you should start a command line and enter this:

```
conda activate llm-da
```

Start [Jupyter lab](https://jupyter.org/) from the terminal like this

```
jupyter lab
```

A browser will open and show you the following web page. In the section `Notebook` click on "Python 3 (ipykernel)" to create a new notebook:

![img.png](images/start_jupyter_lab.png)



Start a new notebook.
Enter the following code. When asked, paste your Blablador API key and hit ENTER.

```
from bia_bob import config_blablador, bob

config_blablador()
```

![](images/jup4nfdi_7.png)

Afterwards, try to communicate with `%%bob` like this:

```
%%bob
Print hello world
```

If `%%bob` answers with a reasonable code-snippet, your installation was successful. 

![](images/jup4nfdi_8.png)



