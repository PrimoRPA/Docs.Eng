# Multi-session work

Multi-session environments where multiple users work with multiple instances of Studio may require differentiating between ports used by those instances of Studio. To reconfigure the ports it is necessary to edit configuration files of the applications that are included in the distribution package:

<table><thead><tr><th>Primo.Studio.exe.config</th><th>Primo.Robot.x64.exe.config</th><th>Primo.Robot.exe.config</th><th width="200">LTools.WebBrowser.Native.exe.config</th><th>LTools.Selector.exe.config</th></tr></thead><tbody><tr><td>debugPort</td><td>debugPortStudio</td><td>debugPortStudio</td><td>-</td><td>-</td></tr><tr><td>debugPortRobot</td><td>debugPort</td><td>debugPort</td><td>-</td><td>-</td></tr><tr><td>selectorPort</td><td>-</td><td>-</td><td>-</td><td>selectorPort</td></tr><tr><td>selectorPortStudio</td><td>-</td><td>-</td><td>-</td><td>selectorPortStudio</td></tr><tr><td>webExtPort</td><td>webExtPort</td><td>webExtPort</td><td>webExtPort</td><td>webExtPort</td></tr><tr><td>webExtPortDebug</td><td>webExtPortDebug</td><td>webExtPortDebug</td><td>webExtPortDebug</td><td>webExtPortDebug</td></tr></tbody></table>

**Please note when configuring parameters of the Studio=Robot pair: debugPort=debugPortStudio, debugPortRobot=debugPort**
