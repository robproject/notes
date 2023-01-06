---
id: mfvtanqce4myq3ym3675lbf
title: Windows
desc: ''
updated: 1672859247823
created: 1640371936505
---
### AppData
    C:\Users\*username*\AppData
Local: files are only on this pc

Roaming: files are synced through domain

LocalLow: files are only on this pc, and have a 'lower level of access'

### Win98
[Download](https://www.htasoft.com/u98sesp/)

## WSL
[Basic Commands](https://learn.microsoft.com/en-us/windows/wsl/basic-commands)

### List Installed Distros
    wsl --list --verbose

### Set version
    wsl --set-version <distribution name> <versionNumber>

### Set default Linux distribution
    wsl --set-default <Distribution Name>

### Unregister and Uninstall
"While Linux distributions can be installed through the Microsoft Store, they can't be uninstalled through the store."!  

    wsl --unregister <DistributionName>