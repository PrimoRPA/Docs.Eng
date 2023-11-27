# Working with projects

A project within Primo Studio is a set of script files grouped into folders. The structure of a project is displayed on the Project palette. Within the file system, a project has the following appearance:

Project folder

* Folder 1
  * Script 1.ltw
  * Script 2.ltw
  * …
* Folder 2
  * …
* Main.ltw
* …
* project.ltp

In addition, projects have a _Dependencies_ folder. It contains additional libraries that are necessary for the project to work. More information on how to download additional libraries can be found in the [Managing dependencies](https://docs.primo-rpa.ru/primo-rpa/primo-studio/projects/manage-dependencies) section.

## Creating a project

In the **File ➝ Project** section of the menu, click the "Create a project" button ![](<../../.gitbook/assets/CreateProject.png>) 

After clicking the button, the project creation dialog box will appear on the screen.

![](<../../.gitbook/assets/CreateNewProject.png>)

In this dialog box, specify the project name, the path to the folder where the project will be stored and an optional comment. The structure of the new project will be displayed on the Project panel once you click the OK button.

![](<../../.gitbook/assets/PrjPanel-NewProject.png>)

## Project actions

_Project_ panel has the following action buttons:

* ![](<../../.gitbook/assets/RefreshPrj.png>) - **Refresh project** 
* ![](<../../.gitbook/assets/NewFolder.png>) - **New folder**
* ![](<../../.gitbook/assets/EditItem.png>) - **Edit item** 
* ![](<../../.gitbook/assets/AddFile.png>) - **Add file** 
* ![](<../../.gitbook/assets/DeleteItem.png>) - **Delete item** 
* ![](<../../.gitbook/assets/NewProcess.png>) - **New process** 
* ![](<../../.gitbook/assets/ExpandFolders.png>) - **Expand folders** 
* ![](<../../.gitbook/assets/CollapseFolders.png>) - **Collapse folders** 

To add a folder to the project, select the folder in which the new one will be created, and click the **New folder** button ![](<../../.gitbook/assets/NewFolder.png>). In the dialog, enter the folder name and click **ОК**:

![](<../../.gitbook/assets/NewFolder-Dialog.png>)

The folder will be created on disk and displayed in the project structure:

![](<../../.gitbook/assets/PrjPanel-NewFolder.png>)

To add a file, select the folder where it needs to be added, and click the **Add file** button ![](<../../.gitbook/assets/AddFile.png>). In the dialog, select the file and click the **Open** button. Files can also be drag-and-dropped onto the project panel.

When a file is added manually, it is necessary to reload the project structure - this is done by using the **Refresh project** button ![](<../../.gitbook/assets/RefreshPrj.png>). When it is clicked, the project structure will be reloaded from disk.

A process can be created using the **New process** button ![](<../../.gitbook/assets/NewProcess.png>) or by using **Ctrl+N** hot keys.
Processes and folders can be moved by dragging them to the desired project node.

To edit a folder or a process, click the **Edit item** button ![](<../../.gitbook/assets/EditItem.png>):

![](<../../.gitbook/assets/EditFolder-Dialog.png>)

Deleting an item is done by selecting the element in the project and clicking the **Delete item** button ![](<../../.gitbook/assets/DeleteItem.png>). Confirm the action by pressing the **OK** button.

![](<../../.gitbook/assets/DeleteFolder-Warning.png>)

## Saving changes

Changes can be saved by clicking the **Save project** button ![](<../../.gitbook/assets/SaveProject.png>) on the action panel of the _Home_ tab. An alternative method is to use **Ctrl+S** hot keys. This will save all changes in open sequences.
It is also possible to set up autosaving - this is done by selecting **File ➝ Settings ➝ General** and specifying the desired period for the **Process autosave** parameter. 

## Opening projects

To open an existing project, click on **Open project** button in the **File ➝ Project** section ![](<../../.gitbook/assets/OpenProject.png>). In the dialog box, specify the root file (project.ltp) of the project to be opened.

