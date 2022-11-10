# Robot

The robot is a standalone application with a minimal graphical interface. ![](<../../.gitbook/assets/0 (69).png>)

![](<../../.gitbook/assets/1 (108).png>) button is used to clear the robot console text.

There two editions of Robot:

* Enterprise: fully functional edition
* Standard: shortened edition

You can find version comparison here: [Robot editions](robot\_editions.md)

The robot must be launched from the command line, using the following arguments:

* projPath: Path to the folder of a performed project
* seqPath: Path to the main project sequence
* instantStart: Start the project as soon as the robot is loaded
* exitOnSuccess: Close the robot when the project is complete
* noOrchestrator: Operating mode with no orchestrator (mandatory if the robot is launched manually)
* StartupPosition: startap robot visualization mode. Choices: Normal (standard), Minimized, Maximized, Tray (send to system tray)
* CloseRdp: correctly close RDP session on startup
* logToFile: Sign of log entry (Log folder)
* logCustomToFile: Custom event logging feature
* logMsgTypes: Types of events to be reported (Error, Info, Debug, Network). The symbol | (Error|Info|Debug) is used to indicate several events
* logType: Log type (Text, Csv)
* noConsole: Disables the log displaying in the console
* RunConfig: startup configuration (WorkflowVar.RunConfig variable). Choices: None, Debug, Release
* RunConfigCustom: configuration startup (WorkflowVar.RunConfigCustom variable)

Example:

Primo.Robot.exe instantStart exitOnSuccess noOrchestrator logType=Csv "seqPath=C:\Work\Project\Sequence.ltw" "projPath=C:\Work\Project\\
