# Analyzing projects

Code of projects and processes can be analyzed - this is done by using **Analysis** button on the *Home* menu tab. 

Analysis functionality allows verifying that a project/process meets the standards of quality and reliability. Analysis uses a set of rules to check the code - these rules are unrelated to project execution. Rules are based on automation methods; they take into account variable names, empty sequences, package limitations, etc.  

**ATTENTION!** Static analyzer checks the code without actually executing the project. That means that the analyzer will not catch errors related to execution or compilation. For the latter, the [Debug](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/debug) tool can be used.

## Settings

To set up analyzer rules, click on **Analysis ➝ Settings** button on the *Home* menu tab:

![](<../../.gitbook/assets/AnalysisButton.png>)

A window with a set of rules will open:

![](<../../.gitbook/assets/AnalysisSettings.png>)
 
Each rule has its code, name, area of use and type of action that will be output in the analysis results. 

There is a checkbox next to each rule - it is used to toggle the rule on/off. Using these checkboxes analysis parameters can be set up individually. If a rule is disabled, it will be ignored when analysis is run. 

**Action** column contains the type of message that will be displayed in the **Analysis** panel when a specific rule is broken: 

* Error: displays an error in the **Analysis** panel.
* Warning: displays a warning.
* Information: displays information.

Actions for rules can be changed: press on an action in the column and select a different value in the dropdown list.

## Analysis results 

To start code analysis, select **Analysis ➝ Analyse project** or **Analysis ➝ Analyse process** option.
Analysis results will be displayed in the **Analysis** panel in the bottom part of the screen:

![](<../../.gitbook/assets/AnalysisResults.png>)

If a rule breach is identified, a message will be displayed, containing the name and code of the rule, name of the file where the breach was found, and recommendations on how to fix it. To expand recommendation text, click on the **Details** icon:

 ![](<../../.gitbook/assets/Analysis-Details.png>).

Analysis results can be exported as an \*.xlsx file. Export is available by clicking on **Export to file** icon at the top of the panel: 
![](<../../.gitbook/assets/Analysis-Export.png>) 

## Running the analyzer from console

The following parameters are used to run the analyzer from the command line:

1. rulepath - path to the rules file.
2. projfile - path to the project.
3. outputfile - path to the results file.
4. errlog - path to the log file.
5. noclose - do not close until analysis is completed.
6. console - output to console.
7. output=\<json,xml,xlsx\> - format of the results file.
8. lang=\<ru-RU\> - language.

Example:

```
Primo.ProjectAnalyzer.App.exe "rulepath=c:\Test\rules2.json" "projfile=C:\Users\Username\Documents\Primo\LibTest\project.ltp" noclose console "output=xlsx" "outputfile=c:\Test\aout.xlsx" "errlog=c:\Test\elog.txt" "lang=ru"
```

## Additional information

1\. In addition to the code analyzer, you can enable automatic syntax check that will work in the background. This setting works in conjunction with code analysis: if there is a syntax error, a warning icon will appear on the element where the error was found. Hovering the mouse over the icon will display detailed information about the error:

![](<../../.gitbook/assets/Analysis-Syntax.png>)
