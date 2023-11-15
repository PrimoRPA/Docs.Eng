# Updating Selenium WebDriver 

Below you can find instructions on how to update Selenium WebDriver to work with browsers. The steps are the same for:
* Operating systems - Windows, Linux, MacOS;
* Browsers - Firefox, Chrome, Edge, Opera, Yandex.

**How to update the web driver:**

1. Check the version of the browser installed in your operating system.
2. Check compatibility of your browser and the webdriver. For example, for Firefox it can be done [here](https://firefox-source-docs.mozilla.org/testing/geckodriver/Support.html).
3. Download the compatible version of the webdriver for your operating system. For example:
   * [for Firefox](https://github.com/mozilla/geckodriver/releases);
   * [for Chrome](https://chromedriver.chromium.org/downloads);
   * [for Edge](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/);
   * [for Yandex](https://github.com/yandex/YandexDriver);
   * [for Opera](https://github.com/operasoftware/operachromiumdriver).

4. Replace geckodriver in the `<path to Studio>/WebDriver` folder.

   * Example for Linux:

   ![](<../../.gitbook/assets/Webdriver-Linux.png>)

   * Example for Windows:

   ![](<../../.gitbook/assets/Webdriver-Win.png>)
