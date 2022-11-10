# Sandbox

![](<../../.gitbook/assets/image (234).png>)

**Windows Sandbox installation**

1. Ensure that your machine is using Windows 10 Pro or Enterprise, build version 18305 or later.
2. Enable virtualization on the machine.
   * If you're using a physical machine, make sure virtualization capabilities are enabled in the BIOS.
   * If you're using a virtual machine, run the following PowerShell command to enable nested virtualization:\
     **Set-VMProcessor -VMName \<VMName> -ExposeVirtualizationExtensions $true**
3. Use the search bar on the task bar and type **Turn Windows Features on and off** to access the Windows Optional Features tool. Select **Windows Sandbox** and then **OK**. Restart the computer if you're prompted.
   * If the **Windows Sandbox** option is unavailable, your computer doesn't meet the requirements to run Windows Sandbox. If you think this is incorrect, review the prerequisite list as well as steps 1 and 2.

**Sandbox usage**

Для запуска процесса в песочнице необходимо вызвать его из процесса робота при помощи элемента Ссылка на процесс. Для включения режима песочницы установите флаг Запуск в песочнице в свойствах элемента

To run a process in sandbox you need to use a Process link element. To execute in a sandbox mode check the property Run in SandBox

![](<../../.gitbook/assets/image (154).png>)

**IMPORTANT! Robots may interchange only simple data (String, Double, DateTime, Boolean etc) or simple data collections (List\<String>, List\<DateTime> etc)**

If you want to automatically close sandbox on finish check Close property

Start timeout property sets amount of milliseconds to wait until sandboxed robot starts

Finish timeout property sets amount of milliseconds to wait until sandboxed robot finishes (non-parallel mode) (0 - infinite)

You may execute sandboxed robot parallel to main (Parallel property) but you won't receive OUT arguments from it
