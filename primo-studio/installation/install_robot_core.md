# Robot Core manual installation and execution

Robot Core is a cross-platform version of Primo Robot

**Ubuntu installation**

1. Open Ubuntu Store

![](<../../.gitbook/assets/image (213).png>)

&#x20; 2\. Install .NET Runtime 5.0

![](<../../.gitbook/assets/image (157).png>)

3\.  Execute

```
sudo apt install -y libgdiplus libc6 libc6-dev
sudo apt install -y fontconfig libharfbuzz0b libfreetype6
```

4\. Open robot folder and allow file Primo.Robot to be executable

![](<../../.gitbook/assets/image (282).png>)

&#x20; 5\. Open WebDriver folder and allow all files to be executable

![](<../../.gitbook/assets/image (187).png>)

&#x20; 6\.  Start robot using terminal. For example:

```
./Primo.Robot instantStart noOrchestrator "projPath=/home/primo/Downloads/Core" "seqPath=/home/primo/Downloads/Core/Main.ltw"

```
