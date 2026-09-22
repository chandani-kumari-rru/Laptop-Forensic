# Laptop-Forensic ([vid1](https://youtu.be/JedUl0bKfg0?si=sFYmQqTkz2UwbtM5) | [vid2](https://youtu.be/qUdU4xKOClA?si=DMM7sVWD03mTO6eS))

## Forensic Triage ([vid1](https://youtu.be/TzsqMTopNvs?si=ZE5d97LMXTpE1m7G))

## Memory Forensic ([vid1](https://youtu.be/G-ocTmsD5Tg?si=6VD_U-VHU_HKjbGO))
  - Physical Memory  (eg: Volatile & Non-Volatile Memory)
  - Virtual Memory  (eg: cloud storage)
## Browser Forensic

## Windows Artifact ([vid1](https://youtu.be/At8Dcc5k6eo?si=_wVHGBlFyA7EBTKn) | vid[2.1](https://youtu.be/qc6mEPUTclg?si=yl1w1M7XPzEyvykF),[2.2](https://youtu.be/icMH6C89URQ?si=qh3wvLinA7NN2New),[2.3](https://youtu.be/6YVlQxcfRTA?si=NEm1qIxIK9A1TAWA),[2.4](https://youtu.be/qv12vRiC-YA?si=B2PXcncjXdYaYoyg),2.5)
- Windows Registry is made up of several key sections called `Hives`, each containing specific types of information. Here are the main registry hives:
  > Location: `C:\Windows\System32\config`
  - `HKEY_CLASSES_ROOT(HKCR)`  : Stores info about which program is open or not
  - `HKEY_CURRENT_USER(HKCU)`  : Stores user-specific settings
  - `HKEY_LOCAL_MACHINE(HKLM)` : Stores info about hardware/software settings
    > eg: HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
  - `HKEY_USERS(HKU)`          : Stores all user profiles, each one represented by a security identifier(sid)
  - `HKEY_CURRENT_CONFIG(HKCC)`: Stores info about hardware profile
### List of Windows Artifacts  
| Artifact | Extension | Location | Software |
| --- | --- | --- | --- | 
|Hives|*.dat|C:\Windows\System32\config|EricZimmerman,Nirsoft,RegRipper|
|Prefetch Files|*.pf|C:\Windows\Prefetch|EricZimmerman,Nirsoft|
|Shellbags||HKCU\Software\Classes\Local Settings\Software\Microsoft\Windows\Shell|EricZimmerman,Nirsoft|
|ShadowCopy|||Nirsoft|
|LNK Files|*.lnk||EricZimmerman,Nirsoft|
|Paging Files|pagefile.sys||EricZimmerman,Nirsoft|
|Hibernateion Files|hiberfile.sys||EricZimmerman,Nirsoft|
|Shimcache||C:\Windows\System32\config\SYSTEM|EricZimmerman,Nirsoft|
|Amacache||C:\Windows\appcompat\Programs|EricZimmerman,Nirsoft|
|$UsnJrnl|||EricZimmerman,Nirsoft|
|Jumplist|||EricZimmerman,Nirsoft|
|EventLog/MFT_Files|||[Chainsaw](https://github.com/WithSecureOpenSource/chainsaw/)|
|USB||HKLM\SYSTEM\CurrentControlSet\Enum\USB|Nirsoft, [USB Detective](https://usbdetective.com/community-download/)|
  - Open Source Tools like [Eric Zimmerman Tools](https://ericzimmerman.github.io/#requirements-and-troubleshooting),  [Nirsoft](https://launcher.nirsoft.net/downloads/index.html), [Reg ripper](https://github.com/keydet89/RegRipper3.0), [Autopsy](https://www.autopsy.com/download/)
  - Sample Registry Hive like [Windows](https://github.com/AndrewRathbun/VanillaWindowsRegistryHives/), Mac, Linux

