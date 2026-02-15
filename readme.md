# COMPATIBILITY

Chrome 5.0.375.17 (Beta) and Chrome 4.1.249.1064 (Stable) are the latest Chrome versions observed to run on Windows Longhorn build 4093 through Windows Vista Beta 2 Build 5356, under experimental conditions.

Chrome 5.0.375.127 Stable - last unofficial version for Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296

Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - last unofficial version for Windows 2000 SP4 without Extended Kernel by using:
 
 advapixp.dll. kernelxp.dll, and userxp.dll by blackwingcat 
 
 wtsapi32.dll, winsta.dll, ws2_32.dll, imm32.dll, and iphlpapi.dll from Windows 2000 Extended Kernel. 

 Chrome 33-50 on Windows 2000 without Extended Kernel is not impossible but it can be unstable.

And Chromium 33.0.1709.0 (r234775) / Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - also the last unofficial version for Windows Whistler Late Beta 1 Build 2410 - Windows Whistler Pre-RC 1 Build 2469 (also Windows XP RC 1 Build 2474 & 2475 for some computers and virutalizers) by using:
 
 kernelxp.dll by blackwingcat (with API swaps to the wrapper)
 
 wtsapi32.dll, winsta.dll, imm32.dll from Windows 2000 Extended Kernel

or otherwise,

Chrome 12.0.729 Dev / Chrome 11.0.696.77 Stable - is the last unofficial version for Windows Whistler Late Beta 1 Build 2410 - Windows Whistler Pre-RC 1 Build 2475 (with API swaps or kernelxp.dll by roytam1) for some computers and virutalizers.

 Since chrome_elf.dll was added on Chrome 33.0.1712.2 Dev, Chrome 33.0.1750.xxx-50.0.2661.xxx is unofficially possible with using bwc's wrappers, but it freezes within seconds.

Chrome 50.0.2661.102; but 50.0.2661.0 (r377898) / 49.0.2623.112 is recommended (and 34.0.1847.137 for no SSE2) is the last Chrome version observed by the community to run on Windows XP SP1 Build 2600.1050 (using compatibility wrappers), and on certain Windows Longhorn builds up to 4088 under experimental conditions. If on Windows XP Pre-RC 2 build 2517 (2517.main.010713-1717) through Windows XP RTM with Updates (xpclnt_qfe.021108-2107), it is recommended to use the files from XP SP1.

If on Windows 2000 with Extended Kernel, ensure you have InitOnce functions enabled to have Chrome 50 working properly.

 Chrome 49.0.2623.112 can run on Windows XP RC 1 builds 2474 through 2509 (using compatibility wrappers), but problems are found that the browser crashes after file downloading on some file extension is complete. IDM / downloading from Chromium 33.0.1709.0 (r234775) / Chrome 33.0.1707.0 Dev / Chrome 32.0.1700.107 Stable or earlier is recommended.

 Chrome 50.0.2661.102 can run on Windows XP RC 1 builds 2474 through 2509 (using compatibility wrappers), but it is unstable even if using just Browservice, rather than the core itself, as said above Chromium . On the other hand, Chrome 50.0.2661.102 can run on Windows XP Pre-RC 2 build 2517 (2517.main.010713-1717) through Windows Server 2003 SP2, but the browser itself will freeze if loading any most webpages or chrome://downloads is triggered, so using Browservice with it is recommended.

 Chromium 50.0.2661.0 (r378023) through early Chromium 51 builds on Windows XP/2003 without One-Core API is not impossible but it can be unstable.

Chrome 53.0.2785.143 - is the last Chrome version observed by the community to run on Windows Vista build 5360 (using kernel API swaps), and on certain Windows Vista builds and Windows 7 pre-Beta builds up to 68xx or 69xx builds under experimental conditions.

# BUGS
Google Chrome 6 - 32 is not known to work on Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296, due to an hardcoded SystemFunction036 on ADVAPI32.DLL.

If Internet Explorer 7 or 8 is installed on Windows XP RTM, you must have imm32.dll from XP SP3 on C:\WINDOWS instead of C:\WINDOWS\SYSTEM32, and you also need to edit the registry to change the userinit value to C:\WINDOWS\explorer.exe.

Firstly, Google Chrome 33 - 49 is not known to work very well on Windows Whistler Beta 1 Build 2410 - Windows Whistler Beta 2 Build 2469 when using kernelxp.dll wrappers by BWC (because it starts but freezes within seconds). Secondly, on some computers and virtualizers, if you use roytam1's kernelxp.dll wrappers and attempted to replace GetNativeSystemInfo (since it was hardcoded on Chrome 12.0.730 Dev) with something else on kernelxp.dll on Windows Whistler Pre-RC 1 Build 2474 & Windows Whistler Pre-RC 1 Build 2475, it triggers an c0000094 exception, even though it is possible without trouble on Windows Whistler Pre-RC 1 Build 2474 & Windows Whistler Pre-RC 1 Build 2475. On the other hand, as said above, when using Chrome 33 - 49 on Windows Whistler Pre-RC 1 Build 2481 - Windows Whistler RC 1 Build 2509, downloading executable files leads to Chrome crashing (because the NTDLL.DLL from XP SP1 does not work on Windows XP builds prior to RC 2 build 2517).

Builds Windows Longhorn build 4093 through Windows Vista build 5356 has limited Chrome versions to 4.1.249.1064 Stable and 5.0.375.17 Beta. Chrome 5.0.375.23 Beta and up will not run on Longhorn build 4093 through Vista build 5356 due to the debug.log saying "A device attached to the system is not functioning".

# NOTES

Make sure you have 7-Zip & CFF Explorer installed.

If you are on a non-XP SP2 system... make sure you use --no-sandbox command line.

If you are looking for an modern version of Chromium, use the following:

https://github.com/e3kskoy7wqk/Chromium-for-windows-7-REWORK

It can only work at least Windows XP build 2481 unofficially

https://github.com/win32ss/supermium

It can only work at least Windows XP build 2517 unofficially

https://github.com/ttalvitie/browservice

If you want the modern web for older Chromium browsers

# DISCLAIMER

This guide is an unofficial, community-made compatibility guide. It is NOT affiliated with, endorsed, or supported by Google or Microsoft. All product names, trademarks, and copyrights belong to their respective owners. This repository does not contain any proprietary Google binaries. It only documents compatibility behavior on legacy Windows systems.

All binaries must be obtained by the user from official sources only. This guide does not provide or link to any downloads.

# WORD OF CAUTION

Please do not use an older version of Google Chrome (or Chromium) for reasons other than using Browservice.

# REFERENCES
* https://claraincorporated.blogspot.com/2025/12/windows-xp-rtm-in-2026-unofficial-guide.html

  Windows XP RTM in 2026: Unofficial Guide

# FUTURE UNOFFICIAL SUPPORT FOR

* Windows NT 4.0 with Extended Kernel

* Chrome 0.2 and newer for Windows 2000 Beta 3 Build 1946 and older

* Chrome 5 and newer for builds Windows Longhorn build 4093 through Windows Vista build 5356

* Chrome 0.3 and newer for Windows Whistler Beta 1 Build 2296 and older - but the exception is up to Chrome 5.0.375.127 Stable by using advapixp.dll and kernelxp.dll by blackwingcat (with API swaps to the wrapper)

* Chrome 12 and newer for Windows XP RC 1 Build 2475 and older (for some computers and virtualizers) - but the exception for some computers and virtualizers is up to Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable by using kernelxp.dll by blackwingcat (with API swaps to the wrapper) - However Chrome 33 through 49 see to work fine on Windows XP RC 1 Build 2474 & 2475, but not on some computers and virtualizers.

* Chrome 33 and newer for Windows 2000 without Extended Kernel (with newer wrappers instead of the BWC's wrappers from 2012)

# EXTRAS

* https://github.com/unclecaptain5426/legacy-windows-chrome-compat/blob/main/gallery.md

  Gallery

# OFF-TOPIC

* https://github.com/unclecaptain5426/legacy-windows-chrome-compat/blob/main/eastereggs.md

  Easter Eggs

* https://github.com/unclecaptain5426/legacy-windows-chrome-compat/blob/main/trivia.md

  Trivia
