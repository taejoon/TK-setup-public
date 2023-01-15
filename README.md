This setting is what I have used for development in general (Taejoon Kwon, 2023-Jan-15). 

## (Windows only) Prepare the linux terminal on Windows 10/11.
1. Prepare Windows 10/11 & WSL2 (Windows Subsystems for Linux).
    * Installation ( [English](https://learn.microsoft.com/en-us/windows/wsl/install) ) ( [Korean](https://learn.microsoft.com/ko-kr/windows/wsl/install) )
    * Working with VScode ( [English](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode) ( [Korean](https://learn.microsoft.com/ko-kr/windows/wsl/tutorials/wsl-vscode) )
1. Install Ubuntu LTS version on WSL2. I started here when I work on Linux machine.
    * Current version is [20.04 Jammy Jalyfish](https://releases.ubuntu.com/jammy/) 
    * At Microsoft Store:  https://apps.microsoft.com/store/detail/ubuntu-22041-lts/9PN20MSR04DW?hl=ko-kr&gl=kr&rtc=1 

## Set up conda and python
You can set it up even if you use macOS or other linux. For Mac user, please check [a separate document](macOS.md). For a Windows user, you need to run the following steps on the WSL2 terminal.

1. Install miniconda. Either anaconda (more comprehensive package) or miniconda (a minimal package) should work, but I prefer miniconda to ignore unnecessary packages included in anaconda. 
    * Download the installation script from https://docs.conda.io/en/latest/miniconda.html#linux-installers
    * Current version: https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    * Download this file with wget (or curl).
    ```
    wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
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
    Type ENTER; you can turn the page with spacebar.
    ```
    ... (full text of the license) ...
    
    Do you accept the license terms? [yes|no]
    [no] >>>
    ```
    Type 'yes' (if you accept the license terms).
    ```
    Miniconda3 will now be installed into this location:
    /home/taejoon/miniconda3

      - Press ENTER to confirm the location
      - Press CTRL-C to abort the installation
      - Or specify a different location below

    [/home/taejoon/miniconda3] >>>
    ```
    Type ENTER. You can use this default directory for the conda installation. 
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
    Type yes for initialization. If you type ENTER (or 'no') here, you can initialize conda by 'conda init' on your terminal later. 
    
    * See more details at the official guide: https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html
1. (optional) Install python on WSL2. If you install the latest conda, you will have the latest stable python version. If you upgrade/downgrade your python version, use the following method (assume that you want to install python 3.10).
    ```
    conda install python=3.10
    ```
## set up R

1. Install R on WSL2 (current version: 4.2.2)
    * [Ubuntu](https://cran.r-project.org/bin/linux/ubuntu/) - use the CRAN package repository.
1. Install Vsual Studio Code on WSL2. 
    * https://code.visualstudio.com/
    * https://learn.microsoft.com/ko-kr/windows/wsl/tutorials/wsl-vscode 
1. Install R packages for Jupyter notebook.
    * ```> install.packages("languageserver") ```
    * ```> install.packages("IRkernel") ```
