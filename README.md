# Laptop-Forensic ([vid1](https://youtu.be/JedUl0bKfg0?si=sFYmQqTkz2UwbtM5) | [vid2](https://youtu.be/qUdU4xKOClA?si=DMM7sVWD03mTO6eS))

## Forensic Triage ([vid1](https://youtu.be/TzsqMTopNvs?si=ZE5d97LMXTpE1m7G))

## Memory Forensic ([vid1](https://youtu.be/G-ocTmsD5Tg?si=6VD_U-VHU_HKjbGO))
  - Physical Memory  (eg: Volatile & Non-Volatile Memory)
  - Virtual Memory  (eg: cloud storage)
## Browser Forensic

## Windows Artifact ([vid1](https://youtu.be/At8Dcc5k6eo?si=_wVHGBlFyA7EBTKn) | vid[2.1](https://youtu.be/qc6mEPUTclg?si=yl1w1M7XPzEyvykF),[2.2](https://youtu.be/icMH6C89URQ?si=qh3wvLinA7NN2New),2.3)
- Windows Registry is made up of several key sections called `Hives`, each containing specific types of information. Here are the main registry hives:
  > Location: `C:\Windows\System32\config`
  - `HKEY_CLASSES_ROOT(HKCR)`  : Stores info about which program is open or not
  - `HKEY_CURRENT_USER(HKCU)`  : Stores user-specific settings
  - `HKEY_LOCAL_MACHINE(HKLM)` : Stores info about hardware/software settings
    > eg: HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
  - `HKEY_USERS(HKU)`          : Stores all user profiles, each one represented by a security identifier(sid)
  - `HKEY_CURRENT_CONFIG(HKCC)`: Stores info about hardware profile
### List of Windows Artifacts  
| Artifact | Extension | Location | 
| --- | --- | --- |
|Hives|*.dat|C:\Windows\System32\config|
|Prefetch Files|*.pf|C:\Windows\Prefetch|
|Shellbags||`HKCU\Software\Microsoft\Windows\Shell\Bags`,`HKCU\Software\Microsoft\Windows\Shell\BagMRU`, `HKCU\Software\Microsoft\Windows\ShellNoRoam\Bags`,`HKCU\Software\Microsoft\Windows\ShellNoRoam\BagMRU`|
|LNK Files|*.lnk||
|Paging Files|pagefile.sys||
|Hibernateion Files|hiberfile.sys||

 like `Hives`(NTUSER.DAT), `Prefetch Files`(*.pf), `Shellbags`, `LNK Files`(*.lnk), `Paging Files`(pagefile.sys), `Hibernation Files`(hiberfile.sys), `Shimcache`, `Amacache`, `$UsnJrnl`, `Jumplist`, `USB Plugin & Play`
  - Open Source Tools like [Eric Zimmerman Tools](https://ericzimmerman.github.io/#requirements-and-troubleshooting),  [Nirsoft](https://launcher.nirsoft.net/downloads/index.html), [Reg ripper](https://github.com/keydet89/RegRipper3.0), [Autopsy](https://www.autopsy.com/download/)
  - Sample Registry Hive like [Windows](https://github.com/AndrewRathbun/VanillaWindowsRegistryHives/), Mac, Linux

