This setting is what I have used for development in general (Taejoon Kwon, 2023-Jan-15). 

## (Windows only) Prepare the linux terminal on Windows 10/11.
1. Prepare Windows 10/11 & WSL2 (Windows Subsystems for Linux).
    * Installation ( [English](https://learn.microsoft.com/en-us/windows/wsl/install) ) ( [Korean](https://learn.microsoft.com/ko-kr/windows/wsl/install) )
    * Working with VScode ( [English](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode) ( [Korean](https://learn.microsoft.com/ko-kr/windows/wsl/tutorials/wsl-vscode) )
1. Install Ubuntu LTS version on WSL2. I started here when I work on Linux machine.
    * Current version is [20.04 Jammy Jalyfish](https://releases.ubuntu.com/jammy/) 
    * At Microsoft Store:  https://apps.microsoft.com/store/detail/ubuntu-22041-lts/9PN20MSR04DW?hl=ko-kr&gl=kr&rtc=1 

## Set up conda and python
You can set it up even if you use macOS or other linux if you use a Terminal.

See [conda document](conda.md) for more information.

## Set up R

Either R packages on the Ubuntu repository or those on the conda are not good to use. They have a version issue (outdated), or dependency issue. I recommend to use the R from [the CRAN UBUNTU repository](https://cran.r-project.org/bin/linux/ubuntu/) directly. 

* Add the CRAN repository to your Ubuntu package manager.
```bash
# update indices
  sudo apt update -qq
# install two helper packages we need
  sudo apt install --no-install-recommends software-properties-common dirmngr
# add the signing key (by Michael Rutter) for these repos
# To verify key, run gpg --show-keys /etc/apt/trusted.gpg.d/cran_ubuntu_key.asc 
# Fingerprint: E298A3A825C0D65DFD57CBB651716619E084DAB9
  wget -qO- https://cloud.r-project.org/bin/linux/ubuntu/marutter_pubkey.asc | sudo tee -a /etc/apt/trusted.gpg.d/cran_ubuntu_key.asc
# add the R 4.0 repo from CRAN -- adjust 'focal' to 'groovy' or 'bionic' as needed
  sudo add-apt-repository "deb https://cloud.r-project.org/bin/linux/ubuntu $(lsb_release -cs)-cran40/"
```

* Install R
```bash
sudo apt-get update
sudo apt install --no-install-recommends r-base
```

See [R document](R.md) for more information.

## Set up Visual Studio Code on the terminal (WSL2)
1. Install Vsual Studio Code on WSL2. 
    * https://code.visualstudio.com/
    * https://learn.microsoft.com/ko-kr/windows/wsl/tutorials/wsl-vscode 
