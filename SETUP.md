# Setup

## Prequisite Software Installations

Install the following software before starting the setup process.

- Unreal Engine 5.3
- Visual Studio Code

## Setup Unreal Project to Use Python

- Open Unreal project
- Choose ***Edit -> Plugins***
    - In the left panel:
        - scroll down to the ***Scripting*** section
    - In the right panel:
        - find ***Python Editor Script Plugin*** and check the enable box
        - find ***Editor Script Utilities*** and check the enable box  

![Image of Unreal Plugin Window](images/02_Unreal_Scripting_Plugins.png)  

- Close the plugin dialog window
- Choose ***Edit -> Project Settings***
    - In the left panel:
        - find ***Plugins*** main heading and select ***Python***
    - In the right panel:
        - check the ***Enable Remote Execution?*** checkbox  

![Image of Unreal Plugin Window](images/03_Unreal_Py_Enable_Remote.png)

- Close project settings dialog window
- Choose ***Edit -> Editor Preferences***
    - In the left panel:
        - Find ***Plugins*** category and select ***Python***
    - In the right panel:
        - Check ***Developer Mode*** checkbox  

![Image of Unreal Project Settings Window](images/04_Unreal_Enable_DevMode.png)  

- Close Editor Preferences dialog window
- Choose ***Edit -> Project Settings***
    - In the left panel:
        - Find and select ***Python***
    - In the right panel:
         - in the advanced area:
             - Check ***Developer Mode (all users)*** checkbox  

![Image of Unreal Plugin Window](images/05_Unreal_DevMode_AllUsers.png)  

- Close Project Settings dialog window
- Save all
- Check out any files not already checked out
- Submit changes to perforce
- Restart Unreal Editor *(Close Unreal project and open it again)*

## Python Version Required

Python Editor Script Plugin contains an embedded version of Python 3.9.7. Therefore, the user will not need to install Python on their workstation.

Please refer to the requirements file for the additional modules to install for Python.

### Embedded Python Module Installation Process:

- open a powershell terminal
- Naviate to the embedded Unreal Python installation location:
    - {Unreal Software Install Dir}\Engine\Binaries\ThirdParty\Python3\Win64\
    - **Example:** E:\01_EpicGames\UE_5.3\Engine\Binaries\ThirdParty\Python3\Win64\
- Run the following command and simply change the module for each item listed in the requirements:

```
 .\python.exe -m pip install PyYAML
```
This will install the required modules for the python version embedded within the Unreal Editor.

## Visual Studio Code Setup To Work With Unreal Engine

- Open ***Visual Studio Code***
- On left icon panel, click on the ***Extensions*** button
- At the top of the window, click inside the ***Search Extensions in Marketplace*** text field
     - Search for ***Unreal Engine Python*** extension
        - The author of this extension is Nils Soderman *(use to verify correct plugin extension)*
    - click ***Install***  

![Image of Unreal Plugin Window](images/06_VSC_UE_Extension_Install.png)

### Setup Unreal Engine Python Plugin
To setup the plugin functionality, run the following commands using the command palette: ***Ctrl + Shift + P***  
This will need to be done for each command to run.

### Setup keyboard shortcut to send Python script to Unreal:

```
Unreal Python: Execute
```

The shortcut will be ***Ctrl + Enter***

![Image of Unreal Plugin Window](images/07_VSC_Execute.png)

### Setup Unreal Python API Code Completion:

```
Unreal Python: Setup code completion
```
![Image of Unreal Plugin Window](images/08_VSC_Code.png)

### Setup Debugging:

```
Unreal Python: Attach
```
![Image of Unreal Plugin Window](images/09_VSC_Attach.png)

### Setup Python Interpreter:

- Select the interpreter button in the lower right bottom area
    - Once this has been click, look in the top center area within the ***Command Paletter*** for next steps  

![Image of Unreal Plugin Window](images/10_VSC_Button_Enterpreter.png)  

- Select ***Enter Interpreter Path...***  

![Image of Unreal Plugin Window](images/11_VSC_Enterpreter.png)  

- Then press the ***Find*** item to open the file browser dialog
- A windows path dialog box should open, navigate to the following location:
    - {Unreal Software Install Dir}\Engine\Binaries\ThirdParty\Python3\Win64\python.exe
- Here is an example for my workstation:
    - E:\01_EpicGames\UE_5.3\Engine\Binaries\ThirdParty\Python3\Win64\python.exe  

![Image of Unreal Plugin Window](images/12_VSC_Find.png) 

This completes the setup process. The user should now be able to write python code within Visual Studio Code using the embedded version of Python used by Unreal. Additionally, the user should have a functioning autocomplete for the Unreal API and use the shortcut keys: *Ctrl + Enter* to send the script to the Unreal editor for execution.

**NOTE:** The code needs to be saved before sending to Unreal, otherwise any edits will not be reflected when sending to Unreal.