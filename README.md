This setting is what I have used for development in general (Taejoon Kwon, 2023-Jan-15). 

## (Windows only) Prepare the linux terminal on Windows 10/11.
1. Prepare Windows 10/11 & WSL2 (Windows Subsystems for Linux).
    * Installation ( [English](https://learn.microsoft.com/en-us/windows/wsl/install) ) ( [Korean](https://learn.microsoft.com/ko-kr/windows/wsl/install) )
    * Working with VScode ( [English](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode) ( [Korean](https://learn.microsoft.com/ko-kr/windows/wsl/tutorials/wsl-vscode) )
1. Install Ubuntu LTS version on WSL2. I started here when I work on Linux machine.
    * Current version is [20.04 Jammy Jalyfish](https://releases.ubuntu.com/jammy/) 
    * At Microsoft Store:  https://apps.microsoft.com/store/detail/ubuntu-22041-lts/9PN20MSR04DW?hl=ko-kr&gl=kr&rtc=1 

## Set up conda and python
You can set it up even if you use macOS or other linux. For Mac user, please check [another document](macOS.md). For a Windows user, you need to run the following steps on the WSL2 terminal.

See [conda document](conda.md).

## set up R

1. Install R on WSL2 (current version: 4.2.2)
    * [Ubuntu](https://cran.r-project.org/bin/linux/ubuntu/) - use the CRAN package repository.
1. Install Vsual Studio Code on WSL2. 
    * https://code.visualstudio.com/
    * https://learn.microsoft.com/ko-kr/windows/wsl/tutorials/wsl-vscode 
1. Install R packages for Jupyter notebook.
    * ```> install.packages("languageserver") ```
    * ```> install.packages("IRkernel") ```
