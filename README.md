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
1. open your Winodws Terminal as administrator 
2. Download the latest Lando .deb package by input the following command on your terminal `wget https://github.com/lando/lando/releases/download/v3.8.1/lando-x64-v3.8.1.deb`
    1. Note that you can see all available lando releases [here](https://github.com/lando/lando/releases)  
    2. we will be using the ***lando-x64-v3.8.1.deb*** for this example. 
1. Once the prevoius process has completed you can __Install Lando__ by inputing the following command on your __Windows Terminal__ `sudo dpkg -I —ignore-depends=docker-ce lando-x64-v3.8.1.deb`
1. Confirm Lando was installed by running `lando —help`

### SYNC LANDO WITH Pantheon
1. With Lando installed on your __WSL 2__ system you can now sync your __Lando instance__ with Pantheon
    1. Note. Make sure to have __Docker Desktop__ active on your computer. 
    2. You will required to have a ***Machine token*** from Pantheon. See process [here](https://pantheon.io/docs/machine-tokens)
2. Create a folder on your system where you want to store the project ie. `mkdir lsc9`
3. Access the folder you just created `cd lsc9`
4. Start lando `lando init`
    1. Make sure to take note of the __URL__ to access your local server, that lando will provide once the this process is completed
5. Lando will start the initialization process apply the following options when prompted
    1.  source ***Phaeton***
    2.  Pantheon Auth ***paste machine token from pantheon****
    3.  Pantheon site name ***select from the list of available projects the one you wish to copy to your local machine***
6. Once the above process is completed successfully. Start lando `lando start`
7. Input assets from pantheon. `lando pull`
    1. In this process you can choose what will be downloaded from pantheon into your local machine and select which branch will be used
    2. Select branch to copy code files from ***development/testing/production***
    3. Choose if you like to download the Database
    4. Choose if you like to download the files (media files). Please note that downloading files from pantheon could take some time depending on the amount of files that exists on the branch selected. 
8. Process completed.  
    1. You can now open your browser and paste the lando local URL provided before
    2. You should be able to access the backend of your local installation using the same credentials of the branch you selected while installing the local project. 
