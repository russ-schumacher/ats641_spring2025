# Lab assignment 1

### Due Friday, February 7

For lab assignment 1, we'll be using various python tools that are useful for analyzing and visualizing weather data, including [MetPy](https://unidata.github.io/MetPy/latest/index.html), developed by NSF Unidata. The first step, if you haven't done this before, will be to install python, and then ultimately install MetPy and related packages.

## Installing python via mambaforge
First, let's install the miniforge version of python.  (If you already have miniconda/anaconda/mamba installed on the computer you want to use, you can skip this step and go to the assignment.)  Following the instructions, which are based on those in the [Unidata python workshop](https://unidata.github.io/python-training/), but modified to use Miniforge/mamba instead, which is much faster:

#### Windows

- Download the [Miniforge installer](https://github.com/conda-forge/miniforge) for Windows.

- Follow the prompts, taking note of the options to "Create start menu shortcuts" and "Add Miniforge3 to my PATH environment variable". The latter is not selected by default due to potential conflicts with other software. Without Miniforge3 on the path, the most convenient way to use the installed software (such as commands conda and mamba) will be via the "Miniforge Prompt" installed to the start menu.
  
- You should now have a program called “Miniforge Prompt” installed. Open it (this will be your Python command prompt).

#### Mac/Linux

- Download the [Miniforge bash installer](https://github.com/conda-forge/miniforge) for your platform.

- After downloading the bash installer, open a command prompt (terminal app on the Mac).

- Change the directory at the terminal to wherever the installer was downloaded. On most systems, this will default to the downloads directory in your user account. If that’s the case, `cd ~/Downloads` will get you there, or replace the path with wherever you saved the file.

- Run the installer script by typing `bash Miniforge3-MacOSX-arm64.sh`. Note: Your file name may be different depending upon your operating system! replace `Miniforge3-MacOSX-arm64.sh` with whatever the name of the file you downloaded was.

- Accept the defaults.

- After the installer has completed completely close and restart your terminal program (this sources the newly modified path).

- If bash isn't your default shell, switch to it by running the command bash.

- Verify that your install is working by running `mamba --version`. You should see a response like `mamba 1.5.6, conda 23.11.0` or similar (though yours may be a different version number).

### Setting up your environment

Now we will set up an environment with the packages we need to have installed. Here is a link to an environment file that we'll use for the class (adapted from Unidata's workshop materials): [environment.yml file](environment_ats641_2025.yml)

To set up this environment, follow these steps:

- Open a terminal window (Miniforge Prompt if you're on Windows).

- Download the .yml file that tells your system what should be in the environment (see link above).

- In the terminal, navigate to wherever this file is saved, probably something like `cd ~/Downloads` will get you there.

- Run the command `conda env create -f environment_ats641_2025.yml` and wait for the installation to finish (it may take a while, especially if you're on a slow internet connection).

- Run the command `conda activate ats641_2025` to activate the environment you created and verify that everything is ready.  (It may ask you to do something like `conda init bash`, if so then do that first.)
