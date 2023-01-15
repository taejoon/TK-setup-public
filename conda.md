# Set up conda and python 
By Taejoon Kwon (2023-Jan-15)


## Install miniconda. 

Either anaconda (more comprehensive package) or miniconda (a minimal package) should work, but I prefer miniconda to ignore unnecessary packages included in anaconda. 
See more details at [the official guide](https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html)

* Download the installation script from https://docs.conda.io/en/latest/miniconda.html#linux-installers
    * Current version: https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
* Download this file with wget (or curl).
    ```bash
    wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
    ```
    **Result:**

    ```bash
    $ wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    --2023-01-15 10:38:31--  https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    Resolving repo.anaconda.com (repo.anaconda.com)... 104.16.130.3, 104.16.131.3, 2606:4700::6810:8203, ...
    Connecting to repo.anaconda.com (repo.anaconda.com)|104.16.130.3|:443... connected.
    HTTP request sent, awaiting response... 200 OK
    Length: 72402405 (69M) [application/x-sh]
    Saving to: ‘Miniconda3-latest-Linux-x86_64.sh’

    Miniconda3-latest-Linux-x86_6 100%[=================================================>]  69.05M  11.1MB/s    in 6.3s

    2023-01-15 10:38:37 (10.9 MB/s) - ‘Miniconda3-latest-Linux-x86_64.sh’ saved [72402405/72402405]
    ```
* Run the downloaded script.
    ```bash
    bash Miniconda3-latest-Linux-x86_64.sh
    ``` 
    **Result:**
    ```bash
    $ bash Miniconda3-latest-Linux-x86_64.sh
    Welcome to Miniconda3 py310_22.11.1-1

    In order to continue the installation process, please review the license
    agreement.
    Please, press ENTER to continue
    ```
* Type ENTER; you can turn the page with spacebar.
    ```
    ... (full text of the license) ...
    
    Do you accept the license terms? [yes|no]
    [no] >>>
    ```
* Type 'yes' (if you accept the license terms).
    ```
    Miniconda3 will now be installed into this location:
    /home/taejoon/miniconda3

      - Press ENTER to confirm the location
      - Press CTRL-C to abort the installation
      - Or specify a different location below

    [/home/taejoon/miniconda3] >>>
    ```
* Type ENTER. You can use this default directory for the conda installation. Of course, 'taejoon' directory above would be replaced by your ID. 
    ```
    PREFIX=/home/taejoon/miniconda3
    Unpacking payload ...

    Installing base environment...

    Downloading and Extracting Packages

    Downloading and Extracting Packages

    Preparing transaction: done
    Executing transaction: done
    installation finished.
    Do you wish the installer to initialize Miniconda3
    by running conda init? [yes|no]
    [no] >>> 
    ```
* Type 'yes' for initialization. If you type ENTER (or 'no') here, you can initialize conda by 'conda init' on your terminal later. 

## Uninstall miniconda

You can remove miniconda installation by removing the directory. If you install it on '/home/YOUR_ID/miniconda3/' as above, you can remove it for removing the conda.
```bash
rm -rf /home/YOUR_ID/miniconda3/
```
or
```bash
rm -rf ~/miniconda3/
```

You may also have '.condarc' and '.conda' on your home directory for configuration. You can remove them also. 

## Basic usage

* Search the package.
```
conda search <package name>
```
* Install the package.
```
conda install <package name>
```
* Update the package.
```
conda update <package name>
```
* Update all packages.
```
conda update --all
```

## Change the python version

If you want to upgrade/downgrade your python version, use the following method (assume that you want to install python 3.10).
```bash
conda install python=3.10
```

## References
* https://conda.io/projects/conda/en/latest/user-guide/getting-started.html 
* Cheat Sheet: https://conda.io/projects/conda/en/latest/user-guide/cheatsheet.html
* https://towardsdatascience.com/managing-project-specific-environments-with-conda-b8b50aa8be0e

