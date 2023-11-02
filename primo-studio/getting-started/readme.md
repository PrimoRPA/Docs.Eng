# Launching Studio Enterprise

The application can be launched either via the desktop icon or visa the Start menu: **Start** > **Primo > Primo Studio**.

When Primo Studio Enterprise is launched for the first time, it will ask for the license. You can select one of the two license types: local or orchestrator. 

![](<../../.gitbook/assets/Ëèöåíçèè â Ñòóäèè.png>)

If neither license type is selected, the application will close once the registration window is closed. 

### Local license

This type of license is suitable for organizations with a small number of robots, or when a robot is set up on a machine that is not connected to Orchestrator. 

The license is tied to the user account and is updated locally.

**How to get this license**: 
* In the registration dialog, select **Local license** (1).
* Press **Request key** button (2).
* Request text will appear in the window (3):

![](<../../.gitbook/assets/local-license-for-studio.png>)
    
* Copy this text and send it to the vendor at [help@rondem.ru](mailto:help@rondem.ru). The reply will contain a license key file with \*.license extension.
* Load the license key into the system by pressing the **Upload the key** button (4). 
    
:white_check_mark: If this process is completed successfully, the registration window will close and Studio will be ready for work. 

### Orchestrator license

This type of license enables license management through Orchestrator. Select this license type if your organization has a large number of robots and it is easier to manage all license updates through a single source. 

**How to get this license**: 
* In the registration dialog, select **Orchestrator license** (1).
* The form for connecting Studio to Orchestrator will be displayed (2). Enter the data for the user account that Studio will use to connect to Orchestrator.

***What does it mean?*** Orchestrator Administrator first needs to [create a user](https://docs.primo-rpa.ru/primo-rpa/orchestrator/settings/users/orch-users) with the Studio role, and then communicate this user's data to you, along with the user tenant and Orchestrator address:*

![](<../../.gitbook/assets/orch-license-for-studio.png>)

* Press **Connect** (3).

:white_check_mark: If a connection is successfully established, Studio will request a free license from Orchestrator. If Studio gets it, the registration window will close and Studio will be ready for work. 

### Studio does not launch
Antivirus software can interfere in the Studio launch process. To avoid it, add the file `LTools.Selector.exe` (or the entire Studio folder) to your antivirus exceptions list. The file `LTools.Selector.exe` is located in the application installation folder. For example:

![](<../../.gitbook/assets/ltools.selector.exe-here.png>)

It is also recommended to read the instructons for [multisession work](https://docs.primo-rpa.ru/primo-rpa/primo-studio/settings/multisession).

