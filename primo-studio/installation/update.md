# Updates 

Updating Studio to the latest version provides access to new functionality and improves data security. 

Updating requires complete reinstallation of the application: first uninstall the old version of Studio, then install the new one. 
The application has to be removed along with all files and folders in the previous installation folder (see exceptions below).

**The following files and folders can be preserved**: 
1. `.Dependencies` folder with earlier set up dependencies - that way they can be kept for later use.
2. If any extensions had been set up - make a backup copy of the file `Primo\Primo Studio\Extensions\manifest_ch.json`, to avoid potential problems with search templates (selectors). Once Studio is reinstalled, use this backup copy to replace the newly installed file with the same name. This recommendation applies to the situations when extensions were installed using the standard method: manually, without using [automation](https://docs.primo-rpa.ru/primo-rpa-eng/primo-studio/settings/autoinstall-browser-extension).

## Uninstallation

Open **Control Panel > Programs > Programs and Features**. Select Studio from the list and click **Uninstall**.
