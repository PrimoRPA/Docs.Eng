# Studio settings

To access Studio settings window, open **File -> Settings** menu. 

![](<../../.gitbook/assets/Studio-Settings-Main.png>)

Settings are grouped into the following categories:

* **General**:
  * Debugger: debugging tool setup.
  * Elements: management of elements. 
  * Personalization: Studio appearance.
* **Network**:
  * Nuget: setup of NuGet package sources.
  * Reverse-Proxy: traffic interception settings.
  * Orchestrator: settings for Orchestrator connection.
* **Integration**:
  * Management of integration with SAP and Java-based applications.
* **Tools**:
  * Extensions: browser extensions settings.
* **Smart Devices**:
  * Android: settings for integration with Android devices.

## General

This panel has the following general parameters:

1. **Max log lines** -maximum number of lines displayed in the [«Console»](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/debug#konsol) panel.
2. **Process autosave** - determines whether all open processes will be saved to temporary files. Autosaving interval is set up in minutes.
3. **Log to file** - determines whether the Studio log will be saved in a file. Example of a path to a saved file: `C:\Users\UserName\AppData\Local\Primo.Primo Studio\Log`. File name: `<day month year hour>_RobotStudio.log`.
4. **Show welcome page** – controls visibility of the Studio welcome screen.
5. **No code default** - determines whether the **No code** mode will be used by default for new elements.
6. **Open last processes** - determines whether the last open processes of a project will be opened automatically.
7. **Show magnifier** - controls visibility of the selector magnifier in the top corner of the screen. If this setting is on, then when an element is selected, the magnifier will be displayed. For example:

    ![](<../../.gitbook/assets/Studio-Settings-Magnifier1.png>)

8. **Grab pause** - here you can set up the hot keys for control element grab pause. By default, it uses the combination of `Alt` + `F12` keys, and its duration is 10 seconds. An example of a situation where a grab pause can be useful: let’s say you want to create a search template for a desktop application, where a click on a context menu item is required.   To avoid grabbing the menu name (instead of the menu item), you can set up a pause that you will use to open the list of menu items, and once the pause runs out - you can grab the necessary menu item. 
9. **Studio Mode** - select one of the two modes:
   * Pro - for users who have programming skills and would like to automate complex business processes that can be executed both on a server and on a desktop, test scenarios, etc.
   * Citizen - a simplified mode that is aimed at the business users who need to automate their own or their coworkers’ tasks; it is suitable for those who do not have programming background. 
10. **Do not show Studio mode choose** - when this setting is checked, the mode selection window will not be displayed upon launching Studio.
11. **Use fast component search** - this setting controls **Fast search** parameter in search templates for desktop applications. If this checkbox is marked, fast search will be enabled for desktop templates. This setting does not affect the templates that are already being used.

### Debugger

On this panel, [debugger](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/debug) functions can be set up:

1. **Debugger type** - by default it is set to `ROBOT` - this runs debugging on a real robot (debugger robot, which is a part of Studio distribution package). `SEQUENCE` value is meant for use by Studio technical personnel and runs debugging without a robot (experimental setting).
2. **Close robot** - determines whether the robot will be closed automatically when debugging is completed. By default the robot is closed. There are situations when this should not be done: for example, if upon completion it is necessary to view the robot console and identify Studio connection issues. Robot console stays accessible as long as the robot stays open.
3. **Show robot console** - if this option is checked, the robot console will be displayed during debugging. Robot console:

   ![](<../../.gitbook/assets/Studio-Settings-RobotConsole1.png>)
   
4. **Minimize Studio** - determines whether Studio will be minimized during debugging.
5. **Show console window** - whether the window with the Studio console will be displayed during debugging. It is a semi-transparent window in the corner of the screen, which allows viewing logs even if the Studio window is minimized. Example: 

   ![](<../../.gitbook/assets/Studio-Settings-StudioConsole.png>)

6. **Check syntax** - enables automatic [syntax check](https://docs.primo-rpa.ru/primo-rpa/primo-studio/projects/analyzer#dopolnitelno). Disabling this option helps speed up debugging on large projects.
7. **Trace enabled** - if this option is enabled, then when debugging is started Studio will be getting from the robot additional step-by-step information about the process. In particular, that is necessary for displaying the values in the “Current value” column in the “Variables” and “Arguments” panels. Disabling this option helps speed up debugging on large projects. 
8. **Realtime variables values** - determines whether current variable values will be displayed in the “Variables” and “Arguments” panels during debugging. This option works only when tracing is enabled. Enabling/disabling this parameter does not affect the ability to view variables in the “Output” panel. Disabling this option helps speed up debugging on large projects. 
9. **Show Output** - enabling this parameter will make the [«Output»](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/debug#panel-vyvod) panel available, which contains detailed information about variable values. This option works only when tracing is enabled. To display the “Output” panel, it is also necessary to set a  [breakpoint](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/debug#tochka-ostanova) on the element that follows after the value of the necessary variable(s) is obtained. Once the breakpoint is reached, “Output” tab will appear on the “Project” panel.
10. **Pause debugging on exception** - checking this option allows you to pause the process automatically if an exception comes up during debugging. That provides the ability for the user to analyze the error and repeat execution of the element manually, without having to restart the entire process from the beginning. If this option is unchecked, process debugging will start from the beginning.
11. **Log to file** - writing the robot log to file. Example of the file path: `C:\Users\UserName\AppData\Local\Primo.Primo Studio\Log`. Possible file names:
    * `<day month year hour>_Default_Robot.log` - robot log without debugging information.
    * `<day month year hour>_Default_Robot1.log`- contains debugging data.
12. **Log custom to file** - writing custom events to file. Custom events are those events that are formed when the robot executes the [«Add to log»](https://docs.primo-rpa.ru/primo-rpa/g_elements/el_basic/els_dialogs/el_dialogs_addlog) element. These files will have the word `custom` in their names, for example: `<day month year hour>_Default_Robot1_custom.log`.
13. **Robot await period** - the maximum time period of waiting for the robot to start during debugging (ms).
14. **Robot type** - x64 or x86.
15. **Engine version** - v1 или v2. The second version (v2) speeds up process loading for debugging and increases productivity on high-load processes. It is recommended to use v2 by default.


### Elements
1. **Hide Generation 1** - when this checkbox is marked, elements from “Generation 1” groups will be hidden on the  «[Elements](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements)» panel. Generation 1 is a set of deprecated elements for the browser and desktop. Hiding them will make the elements panel visually cleaner.
2. **Disable logging for new items** - controls automatic logging of new elements that are added to the project. This parameter provides a way to batch-change the value of the  [Disable logging](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements#svoistva-elementa) property for new elements:
   * if the checkbox is marked, the global property **Disable logging** will be active by default - so element execution logs will not be written;
   * if the checkbox is not marked, then the **Disable logging** property will be off by default.

   Toggling the checkbox on/off does not require Studio restart.


### Personalization

1. **Theme** - selection of the Studio color theme.
2. **Language** - selection of the interface language. You will need to restart Studio after changing the selected language.
3. **Show vertical titles** - displaying vertical titles of the sequence containers.
4. **Show numbering** - this parameter controls auto-numbering of elements in a process. Elements are numbered only in sequences. By default this checkbox is marked, which means that auto-numbering is enabled. To view the element number not only in the process but also in the “Console” panel, it is necessary to add the “Number” column to the console table. To do that, right-click on the header with column names and select the “Show columns” item in the context menu. In the dialog window, check-mark the “Number” column.
5. **Main menu style** - determines the display style of the main menu: as a ribbon or as a bar (deprecated).
6. **Sequence** - after changing the settings it is necessary to reopen the sequence tab:
   * Dropper height - by default, `40`;
   * Element margin - by default, `5`;
   * Container padding - by default, `20`.


## Network

### Nuget

In this section, you can specify the sources for NuGet packages. More details about this section can be found [here](https://docs.primo-rpa.ru/primo-rpa/primo-studio/settings/nuget).

In particular, [the local NuGet server](https://docs.primo-rpa.ru/primo-rpa/orchestrator/settings/nuget) can be specified as a source. This server is a part of the Orchestrator package.

### Reverse-Proxy

Settings for working with the traffic interceptor network:

1. **Port** - the port that is used by the interceptor.
2. **Autoregister as default proxy** - when interception is started, the interceptor will be automatically set as the system’s proxy server.
3. **Capture SSL** - the attribute for SSL/TLS packet capture and decryption.
4. **Capture incoming** - the attribute for interception of responses to requests.

### Orchestrator

Settings for connecting Studio with Orchestrator (not available in Community edition). Here you need to enter the information about the Orchestrator user that has a built-in Studio system role:

1. Orchestrator server address.
2. Tenant - user tenant.
3. User login.
4. User password.

After specifying the necessary information, you can press **Test** button to test the connection. 

Connection status indicator is located in the bottom right corner of the Studio window:

![](<../../.gitbook/assets/Studio-Settings-OrchConnection.png>)

Clicking on the indicator provides quick access to connection settings. 


## Tools

### Extensions
This section controls the setup of [browser extensions and plug-ins](https://docs.primo-rpa.ru/primo-rpa-eng/primo-studio/settings/extensions-and-plugins-install).

![](<../../.gitbook/assets/Studio-Settings-Tools.png>)

## Integration

### Java

Deep search - the option for control element search in Java applications. 

### SAP

SAP explorer:
* Time-out - maximum connection wait time, in milliseconds. By default it is set to `10000`.
* х64 - SAP application architecture.

## Smart devices

### Android

Settings for integration with Android-based mobile devices:

* **ADB path** - the path to the Android Device Bridge installation folder.
