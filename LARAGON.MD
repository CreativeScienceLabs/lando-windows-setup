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
7. In the event you get a firewall notice, click on checkbox for private networks and then the **Allow access** button for both Apache HTTP Server and mysqld so they can communicate on my private network.

### Download project's code to Laragon.
1. Access the [project's page](https://dashboard.pantheon.io/sites/77d3f803-91a1-4ad9-a544-5a1a0b34a6ff#dev/code) on pantheon's dashboard
2. Make sure you are on the **DEV** tab. We will be setting up the development branch on your local pc.  
3. Locate the **Clone with Git** button. Make sure that the **Development Mode** is set to **Git**
4. Copy the provided git repository. Click on the **Copy button**
5. Open your **Laragon** interface.
6. Make sure that all service are running (MySql + Apache / Nginx) at the bottom left corner of the screen you should have **Start ALL** buttom, click it. if instead you have a **Stop** buttom, all the necesary software should already be runing. 
7. Locate the **Terminal** button at the bottom of the laragon widnow. This should open the laragon terminal window at the root folder `C:\laragon\www`
8. Paste the copied repository from pantheon `ctrl+v` them press `enter`
9. You will be promted to confirm that you want to connect to the provided host. Type the work `yes` and press `enter`
10. This will start downloading the code into your local pc. 
11. Once the download process has completed. type `cd lsc-d9` and hit `enter`. This is the root folder for the project. 

### Setting project's DB in laragon.
1. Access the [project's page](https://dashboard.pantheon.io/sites/77d3f803-91a1-4ad9-a544-5a1a0b34a6ff#dev/code) on pantheon's dashboard
2. Make sure you are on the **DEV** tab.
3. Locate the **Backups** option in the sidebar navigation and click it
4. Locate the **Create New Buckup** button and click it, that will create a new backup for code, database and files. 
5. Once the process is completed, you can download the **Database** file into your local PC by clicking the download icon on the Database of the file that was just created. 
6. Once you have the file on your local pc, located and extract the file. A single file with extension 
7. Open your **Laragon** interface
8. Make sure that all service are running (MySql + Apache / Nginx) at the bottom left corner of the screen you should have **Start ALL** buttom, click it. if instead you have a **Stop** buttom, all the necesary software should already be runing. 
9. Locate the **Database** button at the bottom center of the window
10. HeidiSQL GUI should open.
11. locate the **Sessions list** options at the left side of the windonw.
12. You should have an existing session name "unnamed" dobble click it. That will open a new window with the MySql workbench listing all available **Databases** available on your system
13. Create a new database by `right click` on an empty space at the left sidebar where the **DB list** is shown.
14. select the **Create new** and then **Database** from the contextual Menu
15. Provide a DB name `lscd9` and click **OK**
16. You wil be able to see the `lscd9` DB in list. `double click` to set it as active.
17. Then go to **File** and select **Run SQL file** option.
18. Locate the downloaded DB backup on your local pc and selected it.
19. This will start the process of importing the backup into the `lscd9` DB. 
20. once the process is completed. you can press `f5` to refresh the DB and see all the imported data.

### Completing the setup by connection the project to the DB.
1. Create the local settings file.
2. download the `settings.local.php` from the [repository](https://github.com/CreativeScienceLabs/lando-windows-setup/blob/main/settings.local.php) into the `web\sites\default\`
3. Add the `settings.local.php` file into ***gitignore***.
4. Open the `.gitignore` file at the root of the project on your favorite editor, and add the follwing line at the end of the file `sites/*/settings.local.php`
5. Settup is complete now you can open the project.
  1. Open the ***Laragon*** interface and click for the **Menu** option at the top left corner
  2. Click on the `www` option and then look for the click on the `lcs-d9` to open the project on your browser
  3. Alternately you can navigate to `http://lsc-d9.test/` on your browser.

### Adding project's media and files (optional)
1. Please note that this step is optional, the project will be functional but it won't display any media.
2. For development the Media folder is often skipped due to it's large size. 
3. 

