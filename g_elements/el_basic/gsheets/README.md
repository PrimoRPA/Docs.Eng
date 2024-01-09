# Google Sheets

&#x20;In order to connect to Google Sheets services you need to complete the following steps:

1. Navigate to the [developer console](https://console.developers.google.com/flows/enableapi?apiid=sheets.googleapis.com).

2. Create a new project or choose an existing one, then press **Continue**

![](<../../../.gitbook/assets/image (226).png>)

3. Press **Go to credentials**

![](<../../../.gitbook/assets/image (126).png>)

4. Press **Cancel**

![](<../../../.gitbook/assets/image (176).png>)

5. Proceed to **OAuth consent** screen menu

![](<../../../.gitbook/assets/image (225).png>)

6. Choose user type and press **Create**

![](<../../../.gitbook/assets/image (230).png>)

7. Enter application name (any), user support email address and developer email address, then press **Save and continue** on all subsequent forms

![](<../../../.gitbook/assets/image (262).png>)

8. Navigate to the **Credentials** menu, then click on **Create credentials**. Click on **OAuth client ID**

![](<../../../.gitbook/assets/image (200).png>)

9. In the **Application type** dropdown list, choose **Desktop app** and enter application name (any). Press **Create** button. Securely store the information from the pop up window (**Your client ID** and **Your client secret**). Press **OK**

![](<../../../.gitbook/assets/image (288).png>)

10. Download the json file by pressing the corresponding button. You will need to enter the full local path to this file in the **File path** property of the **Google Sheets document** element.

![](<../../../.gitbook/assets/image (264).png>)

11. To work with the table, you will need its ID. You can get the ID from the table URL - it is the alphanumerical string between d/ and /edit parts. Enter that ID into the **Spreadsheet ID** property of the **Google Sheets document** element.

![](<../../../.gitbook/assets/image (208).png>)

## Contents

There are the following element for working with Google Sheets:

1. [Google Sheets document](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/gsheets/el_gsheets_document).
2. [Write range](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/gsheets/el_gsheets_writerange).
3. [Read range](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/gsheets/el_gsheets_readrange).
