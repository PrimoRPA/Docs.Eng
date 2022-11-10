# Studio settings

To open the Studio settings window, press the "File Menu Settings" button.

![](<../../.gitbook/assets/Studio settings.png>)

This window contains settings grouped by the following categories:

* General: Default studio setting
  * Debugger: Debugger setting
  * Personalization: Appearance of the studio, and interface langauage
* Network
  * Orchestrator
  * Reverse-Proxy: Traffic interception settings
* Tools
  * Extentions
* Smart devices
  * Android: Settings for integration with Android devices

## General&#x20;

In this panel you can set up:

* Log rows: Maximum number of rows displayed in the Console panel
* Auto Save Processes: Automatically save all open processes to temporary files
* Period: Autosaved file creation interval
* Log to file: Save debugger log to file
* Display Greeting Window: Responsible for displaying the greeting window at studio startup
* No code default - set No code mode for new elements
* Open last process - automatically open las opened project processes

### Debugger

In this panel the debugger functions are set up:

* Debugger type: Select debugger type - ROBOT (debugging start on real robot) and SEQUENCE (debugging start without robot)
* Close the robot: Close the robot automatically when the process is complete
* Display robot console: Enables log output in robot window
* Minimize Studio: Enables studio minimizing
* Show console window: shows console window
* Check syntax: Enables syntax checking
* Trace enable: Enables trace
* Waiting period for the robot: Deadline for waiting for the robot to start during debugging (ms)
* Robot type: x64 or x86&#x20;

### Personalization

* Theme: Selection of studio color palette
* Language: Selection of interface language. To apply the changes you will need to restart the Studio
* Show vertical titles: Display containers vertical titles

## Network

### Orchestrator

Setting up work with Orchestrator (not available in Community edition)

* Address: Orchestrator server address
* Login: Orchestrator login
* Password: Orchestrator password

### Revers-Proxy

Operation settings with traffic interceptor network:

* Port: Port used by the interceptor
* Auto-registration as a system proxy: When the intercept starts, the interceptor is automatically installed as a system Proxy server
* SSL interception: Sign of SSL/TLS packet capture and decryption
* Intercept incoming traffic: Sign of interception of responses to requests

## Tools

### Extensions

This menu controls the installation of browser extensions.

## Smart devices

### Android

Settings for integration with Android mobile devices

* Path to ADB: Path to the Android Device Bridge installation folder

