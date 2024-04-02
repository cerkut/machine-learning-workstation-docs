---
description: User-space python installation.
---

# Python/Conda

A lot of libraries for machine learning (scikit-learn), numerical computing (numpy, scipy), and data visualization (matplotlib, pandas, seaborn) are available in the form of python packages.&#x20;

We keep the default 'base' environment slim, created system-wide conda environments and installed the following frameworks, shown below with (env\_name):: packages format

* torch :: latest stable GPU-enabled torch, torchaudio, torchvision, and torchtext&#x20;
* tf-keras-jax :: latest stable GPU-enabled tensorflow 2, keras, and jax

You can activate these global environments with&#x20;

```sh
// conda activate torch # or tf-keras-jax
```

While `pip` let's you easily install new packages, it doesn't fully account for their dependencies which may result in malfunctionings or unreplicable results. Therefore, we use `conda;`a package and environment manager to create and maintain multiple development environments at the same time.&#x20;

Some packages may not exist in conda; as a last resort, you can then use pip from within the conda environment:

```bash
pip install --user <PACKAGE_NAME>
```

If absolutely needed, you can create a new environment called `<ENV_NAME>`at your user space, by&#x20;

```bash
conda create --name <ENV_NAME>
```

You can then activate the environment by running:

```bash
conda activate <ENV_NAME>
```

You will know that the environment is active because its name will appear between parentheses at the beginning of the command prompt. Once an environment is active, you can access all the python packages installed within. You can also use the command above to switch between existing environments.

By default, Conda environments are stored in the user’s home directory (`$HOME/.conda/envs/`).

In order to install the custom package `<PACKAGE_NAME>` within the environment, make sure the environment is active then type:

```bash
conda install <PACKAGE_NAME>
```

You can search for python packages on [this repository](https://anaconda.org/), which also contains detailed instruction on how to install most packages.

## Other commands

*   Update conda:

    ```bash
    conda update conda
    ```
*   Update a package in the environment:

    ```bash
    conda update <PACKAGE_NAME>
    ```
*   Remove a package from the environment:

    ```bash
    conda remove <PACKAGE_NAME>
    ```
*   List environments:

    ```bash
    conda info --envs
    ```
*   List packages inside current environment:

    ```bash
    conda list
    ```
*   Delete environment:

    ```bash
    conda env remove --name <ENV_NAME>
    ```

The following commands can be used to share environments.

*   Export environment into `.yml` file:

    ```bash
    conda env export > environment.yml
    ```
*   Create environment from `.yml` file:

    ```bash
    conda env create -f environment.yml
    ```

For more commands, refer to [this page](https://conda.io/projects/conda/en/latest/user-guide/tasks/index.html).
