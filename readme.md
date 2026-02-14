# COMPATIBILITY

Chrome 5.0.375.17 (Beta) and Chrome 4.1.249.1064 (Stable) are the latest Chrome versions observed to run on Windows Longhorn build 4093 through Windows Vista Beta 2 Build 5356, under experimental conditions.

Chrome 5.0.375.127 Stable - last unofficial version for Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296

Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - last unofficial version for Windows 2000 SP4 without Extended Kernel by using:
 
 advapixp.dll. kernelxp.dll, and userxp.dll by blackwingcat 
 
 wtsapi32.dll, winsta.dll, ws2_32.dll, imm32.dll, and iphlpapi.dll from Windows 2000 Extended Kernel. 

Chrome 33-50 on Windows 2000 without Extended Kernel is not impossible but it can be unstable.

And Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - also the last unofficial version for Windows Whistler Late Beta 1 Build 2410 - Windows Whistler Pre-RC 1 Build 2469 (also Windows XP RC 1 Build 2474 & 2475 for some computers and virutalizers) by using:
 
 kernelxp.dll by blackwingcat (with API swaps to the wrapper)
 
 wtsapi32.dll, winsta.dll, imm32.dll from Windows 2000 Extended Kernel

or otherwise,

Chrome 12.0.729 Dev / Chrome 11.0.696.77 Stable - is the last unofficial version for Windows Whistler Late Beta 1 Build 2410 - Windows Whistler Pre-RC 1 Build 2475 (with API swaps or kernelxp.dll by roytam1) for some computers and virutalizers.

Since chrome_elf.dll was added on Chrome 33.0.1712.2 Dev, Chrome 33.0.1750.xxx-50.0.2661.xxx is unofficially possible with using bwc's wrappers, but it freezes within seconds.

Chrome 50.0.2661.102; but 49.0.2623.112 is recommended (and 34.0.1847.137 for no SSE2) is the last Chrome version observed by the community to run on Windows 2000 with Extended Kernel and Windows XP build 2474 (using compatibility wrappers), and on certain Windows Longhorn builds up to 4088 under experimental conditions.

Chrome 50 on Windows XP/2003 without One-Core API is not impossible but it can be unstable.

Chrome 54.0.2??? Dev / Chrome 53.0.2785.143 - is the last Chrome version observed by the community to run on Windows Vista build 5360 (using kernel API swaps), and on certain Windows Vista builds and Windows 7 pre-Beta builds up to 68xx or 69xx builds under experimental conditions.

# FREQUENTLY ASKED QUESTIONS

1) Why Chrome 12.0.730+ Dev hardcoded GetNativeSystemInfo for some computers and virutalizers?

Because Chrome 12.0.729 Dev / Chrome 11.0.696.77 Stable is the last to use a fallback function like GetStdHandle or something for GetNativeSystemInfo (especially on Windows XP Pre-RC 1 build 2475 and below) for some computers and virutalizers. Because starting Chrome 12.0.730+ Dev, if GetNativeSystemInfo is replaced with something else, it will trigger an exception CPU divide-by-zero (0xc0000094) for some computers and virutalizers.

2) Why Chrome 23-32 require any additional DLLs for Windows 2000 without Extended Kernel / and Chrome 23-49 requires any additional files for Windows XP RTM? ===

Because starting at Chrome 23.0.1255.0 Dev, without any minor modifications like these files for Windows XP RTM/2000 SP4 without KernelEx, Chrome starts to lose functionally for the address bar due to imm32.dll and msftedit.dll changes, and by Chrome 24, Chrome will not start on Windows XP RTM/2000 SP4 without KernelEx without minor modifications. Therefore, on Windows XP RTM.

2.1) For Chrome 24-28...You must have the imm32.dll and msftedit.dll from Windows 2000 Extended Kernel, or the address bar will not work (for Windows 2000)

2.2) For Chrome versions 29-32... You must have the imm32.dll from Windows 2000 Extended Kernel, or Chrome will not launch.
   
3) Why chrome_elf.dll does not like Windows XP RTM/2000 SP4?

Because starting at Chrome 33.0.1712.2 Dev, Chrome starts to lose functionally for Windows 2000 SP4 without Extended Kernel, due to chrome_elf.dll being introduced, while it is  still unofficially possible to get it to work on Windows 2000 SP4 without Extended Kernel, but even with normal use after the timeout (up to 60 seconds), it will freeze. So, because later versions (like Chrome 33.0.1712.2 Dev - Chrome 49.0.2623.112) require at least Microsoft Windows XP build 2481 (but Microsoft Windows XP build 2517 or later is recommended especially to get it fully working is by swapping the ntdll.dll with the one from Microsoft Windows XP SP1, and with just using kernelxp.dll wrappers unofficially + additional XP SP3 DLLs (such as iphlpapi.dll, icmp.dll, imm32.dll (if on 2481-2509, then its from Windows 2000 Extended Kernel))).

3.1) 

4) Why chrome requires winhttp.dll?
Note: winhttp.dll must be inserted to system32 or the chrome folder for Windows versions before Windows 2000 SP3 and Windows XP SP1 in order for Chrome to work.
winhttp.dll must be from at least Windows Server 2003 RTM/Windows XP SP2/Windows 2000 SP4 UR1.

5) Why wrappers needed on Chrome versions after 0.2.149.30 for Windows 2000?
Because of the hardcoded SystemFunction036/RtlGenRandom functions on ADVAPI32.DLL, and if attempted to load Chrome 0.3 without wrappers on Windows 2000, the program will crash with "Whoa! Google Chrome has crashed. Restart now?"

# BUGS
Google Chrome 6 - 32 is not known to work on Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296, due to an hardcoded SystemFunction036 on ADVAPI32.DLL.

If Internet Explorer 7 or 8 is installed on Windows XP RTM, you must have imm32.dll from XP SP3 on C:\WINDOWS instead of C:\WINDOWS\SYSTEM32, and you also need to edit the registry to change the userinit value to C:\WINDOWS\explorer.exe.

Firstly, Google Chrome 33 - 49 is not known to work very well on Windows Whistler Beta 1 Build 2410 - Windows Whistler Pre-RC 1 Build 2475 when using kernelxp.dll wrappers by BWC (because it starts but freezes within seconds). Secondly, on some computers and virtualizers, if you use roytam1's kernelxp.dll wrappers and attempted to replace GetNativeSystemInfo (since it was hardcoded on Chrome 12.0.730 Dev) with something else on kernelxp.dll on Windows Whistler Pre-RC 1 Build 2474 & Windows Whistler Pre-RC 1 Build 2475, it triggers an c0000094 exception. However, Windows Whistler Pre-RC 1 Build 2474 & Windows Whistler Pre-RC 1 Build 2475 does seem to work on some computers and virutalizers, while some of them don't. On the other hand, when using Chrome 33 - 49 on Windows Whistler RC 1 Build 2474 - Windows Whistler RC 1 Build 2509, downloading executable files leads to Chrome crashing (because the NTDLL.DLL from XP SP1 does not work on Windows XP builds prior to RC 2 build 2517).

Builds Windows Longhorn build 4093 through Windows Vista build 5356 has limited Chrome versions to 4.1.249.1064 Stable and 5.0.375.17 Beta. Chrome 5.0.375.23 Beta and up will not run on Longhorn build 4093 through Vista build 5356 due to the debug.log saying "A device attached to the system is not functioning".

# SCREENSHOTS

<img width="640" height="400" alt="VirtualBox_vanilla Windows 2000_30_07_2025_18_59_23" src="https://github.com/user-attachments/assets/5daa8ba4-4780-4841-a451-44fc2489a062" />

Google Chrome 32 on Windows 2000 SP4 + without Extended Kernel!

<img width="640" height="400" alt="VirtualBox_Whistler 2410_27_01_2026_23_58_03" src="https://github.com/user-attachments/assets/5000de18-0335-4746-849c-d9c48734abaf" />

Google Chrome 32 on Windows XP build 2410!

<img width="640" height="400" alt="VirtualBox_vanilla Windows 2000_22_11_2025_00_09_06" src="https://github.com/user-attachments/assets/81b4decb-f1f1-4b58-aeb7-989a92922252" />

Google Chrome 49 on Windows 2000 SP4 + without Extended Kernel! (but it is extremely unstable there, same when using the UURollup v11 package from November 30, 2014)

<img width="640" height="400" alt="VirtualBox_Whistler 2481_26_10_2025_23_22_11" src="https://github.com/user-attachments/assets/bc171f62-19b4-4f26-85a0-9f47040e60a8" />

Google Chrome 49 on Windows XP build 2475!

<img width="640" height="400" alt="VirtualBox_Windows XP RC 1 Build 2475_13_02_2026_19_23_08" src="https://github.com/user-attachments/assets/2d554406-168d-4170-89db-29707b4ab57e" />

Google Chrome 49 on Windows XP build 2481!

<img width="640" height="400" alt="Google Chrome 53 on Windows Vista build 5360!" src="https://github.com/user-attachments/assets/85a4fe8f-95ac-4cda-9c68-bc14538ae039" />

Google Chrome 53 on Windows Vista build 5360!

# NOTES

Make sure you have 7-Zip & CFF Explorer installed.

If you are on a non-XP SP2 system... make sure you use --no-sandbox command line.

If you are looking for an modern version of Chromium, use the following:

https://github.com/e3kskoy7wqk/Chromium-for-windows-7-REWORK

It can only work at least Windows XP build 2481 unofficially

https://github.com/win32ss/supermium/

It can only work at least Windows XP build 2517 unofficially

# DISCLAIMER

This guide is an unofficial, community-made compatibility guide. It is NOT affiliated with, endorsed, or supported by Google or Microsoft. All product names, trademarks, and copyrights belong to their respective owners. This repository does not contain any proprietary Google binaries. It only documents compatibility behavior on legacy Windows systems.

All binaries must be obtained by the user from official sources only. This guide does not provide or link to any downloads.

# WORD OF CAUTION

Please do not use an older version of Google Chrome as a daily driver. It must be for testing purposes only.

# REFERENCES
* https://claraincorporated.blogspot.com/2025/12/windows-xp-rtm-in-2026-unofficial-guide.html

  Windows XP RTM in 2026: Unofficial Guide

# FUTURE UNOFFICIAL SUPPORT FOR

* Windows NT 4.0 with Extended Kernel

* Chrome 0.2 and newer for Windows 2000 Beta 3 Build 1946 and older

* Chrome 5 and newer for builds Windows Longhorn build 4093 through Windows Vista build 5356

* Chrome 6 and newer for Windows Whistler Beta 1 Build 2296 and older

* Chrome 12 and newer for Windows XP RC 1 Build 2475 and older (for some computers and virtualizers) - but the exception for some computers and virtualizers is up to Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable by using kernelxp.dll by blackwingcat (with API swaps to the wrapper)

* Chrome 33 and newer for Windows 2000 without Extended Kernel
