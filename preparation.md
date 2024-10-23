# Preparation

This is the preparation guide if you are using Windows. If you are using MacOS, you can skip this guide.

## Requirements

Your need Windows 11 or Windows 10 newer than Build 19041. To see your build number, go to start menu -> `Settings` -> `System` -> `About`.

## VSCode

Go to the [VSCode website](https://code.visualstudio.com/) and download/install the latest version of the editor.

You need to install `WSL` extensions in VSCode. Open VSCode, click the `Extensions` icon on the left bar, search for `WSL` and install the extension.

## Windows terminal

* Go to the [Microsoft Store](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701) for the Windows Terminal.
* Click `View in Store`.
* Install the Windows Terminal in the Microsoft Store.

## Enable WSL

Open PowerShell as Administrator and run the following command:

```powershell
wsl --install --distribution Ubuntu-24.04
```

Allow adminsitrator access when you see pop-up window. After it finishes, restart the computer.

After restart, wait sometime, it automatically pops up a window for installing Ubuntu 24.04. It will take a few minutes. After it finishes, set username and password for the Ubuntu. Note: when you type the password you do not see anything. Just type and press enter.

After setting the username and password, close the pop-up window.

## Set-up Ubuntu

Open the Windows Terminal from start menu, and click the down arrow on the top bar. Select `Ubuntu-24.04` from the dropdown menu.

Run the following command to install the necessary packages. You need to enter the password you set up earlier.

```bash
sudo apt update
sudo apt upgrade -y
sudo apt install -y git python3.12 python3.12-venv python3.12-dev wslu
```

## Try with Python

Now we try to run the Python template project to see if it works.

### Clone and install project

Run the following command to clone and install the project.

```bash
git clone https://github.com/EES-TUe/ees-scientific-software-engineering.git
cd ees-scientific-software-engineering
python3.12 -m venv .venv
. .venv/bin/activate
pip install .[dev]
pytest
```

### Coverage report from browser

Run the following command to open the coverage report. You should see a coverage report in the browser. Try to play with it.

```bash
wslview python_cov_html/index.html
```

### Open VSCode

Run the following command to open the project in VSCode. You can do this for all the folders you want to open in VSCode. For the first time, it will pop up a window to allow the access. Check the `Permanetely allow host ...`, then click `Allow`.

When VSCode opens, you click `Trust Authors`. Also install recommended extensions.

```bash
code .
```

You might need to restart the VSCode to see the extensions. After that, go to test tab and run the tests.

### Deactivate and delete project

Now you can deactivate the virtual environment and delete the project.

```bash
deactivate
cd ..
rm -rf ees-scientific-software-engineering
```
