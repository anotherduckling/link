---
visibility: hidden
---
![](https://cdn.discordapp.com/attachments/1015131233824538624/1085458821037699092/DGHT1JA.png)
# Configure & Install Office

!!!info Brief
Our objective is to install Microsoft Office by making use of the Office Deployment Tool. For customization purposes, we will create a configuration for the Deployment Tool, allowing us to select the desired Architecture, Office Suite, Languages, and bundled apps (Word, Excel, Onenote etc.) to be installed.
!!!

## Step 1: Creating configuration

Go to [**this site**](https://config.office.com/deploymentsettings) and customize it.

1. In `Products and releases` 
	- Select your **PC Architecture**.
	- Choose your **Office suite** (Office version).
	- In **Apps** turn apps on or off to include or exclude them from being deployed.
	- Skip the rest.

2. In `Language`
	- You have to select **Primary Languages**
	- If you want, you can select additional language and proofing tools.

3. Skip `Installation` section
4. In `Updates and upgrades` section
	- **Turn off** Uninstall any MSI versions of Office, including Visio and Project.
	- Skip the rest.
5. Skip other sections and export (top right corner) the configuration file as **XML file**.

## Step 2: Download Office Deployment Tool

1. Download the [**Office Deployment Tool**](https://officecdn.microsoft.com/pr/wsus/setup.exe)
2. Run the executable file which will extract the **Setup.exe** file.

## Step 3: Installing Office

1. Create a folder and put the **Configuration.xml** and **Setup.exe** in that folder.
2. Open **Command Prompt** in that folder and run `setup /configure configuration.xml`

!!!light
It will now install the Office
!!!

## Step 4: Activating Office

1. Open **Powershell** and run `irm https://massgrave.dev/get | iex`. It will download and open `Microsoft Activation Scripts` in Command Prompt.
2. Press `3` and then `4` and let it do the process. After the successful process, press any key and go back.
3. Press `2`. It will start the activation process.
!!!warning
If it's not showing any progress redo **step 4.1** or download and run [**this**](https://github.com/massgravel/Microsoft-Activation-Scripts/releases).
!!!