# Installing extensions and plugins

Extensions can be installed using one of the following methods:
* [automatically](https://docs.primo-rpa.ru/primo-rpa-eng/primo-studio/settings/autoinstall-browser-extension) - only for browsers;
* manually from Studio;
* from the command line.

## Installing from Studio

Installation instructions can be found in the following sections:

{% content-ref url="chrome.md" %}
[chrome.md](chrome.md)
{% endcontent-ref %}

{% content-ref url="firefox.md" %}
[firefox.md](firefox.md)
{% endcontent-ref %}

{% content-ref url="edge.md" %}
[edge.md](edge.md)
{% endcontent-ref %}

{% content-ref url="yandex.md" %}
[yandex.md](yandex.md)
{% endcontent-ref %}

{% content-ref url="rdp.md" %}
[rdp.md](rdp.md)
{% endcontent-ref %} 

{% content-ref url="java.md" %}
[java.md](java.md)
{% endcontent-ref %}


## Installing from the command line

Methods of installing extensions and plugins from the command line are outlined below.

## Browser extensions

```
LTools.WebBrowser.Native.exe install=[browser] lang=[language] mode=[mode]
```
Supported arguments:
* **browser** - browser types (CHROME, FIREFOX, EDGE, YANDEX);
* **language** - installation language (EN, RU);
* **mode** - installation mode (store, packed, unpacked, storelocal).

Example of installing without the internet connection:
```
LTools.WebBrowser.Native.exe install=CHROME lang=RU mode=packed
```

Example of installing with internet connection present:
```
LTools.WebBrowser.Native.exe install=CHROME lang=RU mode=storelocal
```

## Plugins

### RDP

```
Primo.RemoteAgent.exe InstallClient
```

### Java

```
Extensions\JavaBridge.ps1
```
