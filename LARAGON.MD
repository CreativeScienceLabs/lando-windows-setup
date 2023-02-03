# Laragon windows setup

### Requeriments 
1. [Git account]([url](https://github.com/)

### Installation
1. Download laragon from the official [webiste](https://laragon.org/download/index.html) - make sure to download the full version
2. After the download is complete, start the installation process by double-click on the Laragon installer.
3. On the **Select Destination Location** page, go with the default destination option which is `C:\laragon`
4. When the installation is done, click on Finish so as to restart your machine.
5. After your PC is done rebooting, launch the Laragon app from the desktop or from the Start menu. 
6. When Laragon opens, Click on the Start All button located at the bottom left corner of the laragon interface, to start Apache and MySQL
7.  In the event you get a firewall notice, click on checkbox for private networks and then the **Allow access** button for both Apache HTTP Server and mysqld so they can communicate on my private network.

### Download projects to Laragon.
1. Access the [project's page](https://dashboard.pantheon.io/sites/77d3f803-91a1-4ad9-a544-5a1a0b34a6ff#dev/code) on pantheon's dashboard
2. Make sure you are on the **DEV** tab. We will be setting up the development branch on your local pc.  
3. Locate the **Clone with Git** button. Make sure that the **Development Mode** is set to **Git**
4. Copy the provided git repository. Click on the **Copy button**
5. Open your **Laragon** interface
6. Locate the **Terminal** button at the bottom of the laragon widnow. This should open the laragon terminal window at the root folder `C:\laragon\www`
7. Paste the copied repository from pantheon `ctrl+v` them press `enter`
8. You will be promted to confirm that you want to connect to the provided host. Type the work `yes` and press `enter`
9. This will start downloading the code into your local pc. 
10. Once the download process has completed. type `cd lsc-d9` and hit `enter`. This is the root folder for the project. 

### Setting projects DB in laragon.
1. Access the [project's page](https://dashboard.pantheon.io/sites/77d3f803-91a1-4ad9-a544-5a1a0b34a6ff#dev/code) on pantheon's dashboard
2. Make sure you are on the **DEV** tab.
3. Locate the **Backups** option in the sidebar navigation and click it
4. Locate the **Create New Buckup** button and click it, that will create a new backup for code, database and files. 
5. Once the process is completed, you can download the **Database** file into your local PC by clicking the download icon on the Database of the file that was just created.
6. 
