# lando-windows-setup
###Windows / WSL 2 / Docker / Lando

### Prerequisites
1. Getting started with Lando `https://docs.lando.dev/getting-started/what-it-do.html#cold-as-ice`
2. WSL 2 - installation `https://learn.microsoft.com/en-us/windows/wsl/install`
3. DOCKER 
    1. Installing docker on windows. `https://docs.docker.com/desktop/install/windows-install/`
    2. Support for WSL 2 `https://docs.docker.com/desktop/windows/wsl/`
5. Linux distro for windows `https://ubuntu.com/wsl`
6. Windows terminal https://learn.microsoft.com/en-us/windows/terminal/

### INSTALLING LANDO
1. Download the latest Lando .deb package 
    1. see available packages [here](https://github.com/lando/lando/releases)
    1. open your Winodws Terminal as administrator
    2. 
    3. wget https://github.com/lando/lando/releases/download/v3.8.1/lando-x64-v3.8.1.deb
2. Install Lando package
    1. sudo dpkg -I —ignore-depends=docker-ce lando-x64-v3.8.1.deb
3. Confirm Lando was installed 
    1. Lando —help

### SYNC LANDO WITH Pantheon
1. Create a folder on your system where you want to store the project ie. `mkdir`
