# Managing dependencies

Primo robots can use 3rd party libraries in their projects. Once the libraries are linked, they can be used in code inserts. The same method can be used to include additional elements into projects. 
The following methods of importing dependencies are available:  

1. Copying all required \*.dll files into the `Referenced` folder of Studio and robot (for regular libraries).
2. Copying all necessary \*.dll files into the root folder of Studio and robot (for elements).
3. Adding dependencies manually.
4. Using dependencies manager.

Loading dependencies into a project takes some time. The linked libraries will appear in the script editor only after the “Loading dependencies…” message disappears from the Studio status panel. 

![](<../../.gitbook/assets/LoadingDependencies.png>)

## Dependencies manager

Dependencies for Primo projects can be distributed as NuGet packages (\*.nupkg) either by direct copying or by using the [nuget.org](https://www.nuget.org/) portal. 

To start the Dependencies manager, use **Manage dependencies** button of the main menu <img src="../../.gitbook/assets/ManageDependenciesButton.png" alt="" data-size="line"> or right-click on the “Dependencies” item in the project panel. This will open a dialog window: 

![](<../../.gitbook/assets/ManageDependencies-dialog.png>)

Dependencies are divided into four main groups:

* **Project** - this group contains dependencies attached to the project itself. They are physically located in the `.Dependencies` folder of the project. Dependencies can be added either from the local Studio repository or from the nuget.org portal.
* **Studio** - these are dependencies that are located in the local Studio repository. New dependencies can be added either by visiting Nuget.org or manually, by copying into the  `.Dependencies` folder of the Studio root folder. When the manual method is used, it is necessary to create a subfolder in the `.Dependencies` folder, with the name of your nuget package (without the extension), then copy the nuget package file (\*.nupkg) into that subfolder. For example, for the package `Antlr.3.5.0.2.nupkg`, a subfolder with the name `Antlr.3.5.0.2` needs to be created. When installing from nuget.org, the dependency will be automatically imported into the current project. To import only into Studio it is necessary to close the current project before importing.  
* **Nuget.org** - the group contains packages from the nuget.org website. They require an Internet connection to work.\
  :small_blue_diamond: ***NOTE***. *To search for the official elements, use **Primo** or **Rondem** keywords*.
* 3rd party sources - information about handling additional sources can be found in the [Nuget section](https://docs.primo-rpa.ru/primo-rpa-eng/primo-studio/settings/nuget).

## Importing dependencies 
Dependencies are imported using the following algorithm:
1. Search is done in the Studio repository.
2. If the dependency is found, it will be installed from the Studio repository.
3. If it is not found, then installation will be done from nuget.org with subsequent copying into the local Studio repository.

Importing/deleting/updating of dependencies is done in batches, i.e. at the moment of pressing the control buttons (Add/Delete/Update), labels are set (shown as pictograms <img src="../../.gitbook/assets/ManageDependencies-Pictograms.png" alt="" data-size="line">), installation is performed after pressing the **Save** button.

Pressing the **Save** button displays a window with the list of proposed changes:

![](<../../.gitbook/assets/InstallDependencies.png>)

After **Install** button is pressed, all of these changes will be made, and the bottom part of the window will display the dependencies installer log.

Once the changes are completed the project will be reloaded. 

:bangbang: **IMPORTANT! Save all changes in the algorithms before starting the work with dependencies.**

## Restoring dependencies

If the `.Dependencies` folder of a project does not contain the necessary dependencies, Project palette will show errors (`htmlagilitypack` in the example below).

![](<../../.gitbook/assets/Dependencies-error.png>)

Dependencies can be restored manually by copying, or automatically: to do this, right-click on any dependency and select **Restore dependencies** item in the local menu.
