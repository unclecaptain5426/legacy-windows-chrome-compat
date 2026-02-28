Chrome 5.0.375.17 (Beta) and Chrome 4.1.249.1064 (Stable) are the latest Chrome versions observed to run on Windows Longhorn build 4093 through Windows Vista Beta 2 Build 5356, under experimental conditions.

Chrome 5.0.375.127 Stable - last unofficial version for Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296

Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - last unofficial version for Windows 2000 SP4 without Extended Kernel and Windows XP Beta 2 (builds 2410-2469) by using:
 
 advapixp.dll. kernelxp.dll, and userxp.dll by blackwingcat (Windows 2000 SP4 without Extended Kernel)

 kernelxp.dll by blackwingcat (Windows XP Beta 2 builds 2410-2469) only
 
wtsapi32.dll, winsta.dll, ws2_32.dll, imm32.dll, and iphlpapi.dll from Windows 2000 Extended Kernel. (Windows 2000 SP4 without Extended Kernel)

 wtsapi32.dll, winsta.dll, ws2_32.dll, and imm32.dll from Windows 2000 Extended Kernel. (Windows XP Beta 2 builds 2410-2469)

 Chrome 33-50 on Windows 2000 without Extended Kernel and Windows XP Beta 2 builds is not impossible but it can be unstable.

And Chromium 33.0.1709.0 (r234775) / Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - also the last unofficial version for Windows Whistler Late Beta 1 Build 2410 - Windows Whistler Pre-RC 1 Build 2469) by using:
 
 kernelxp.dll by blackwingcat (with API swaps to the wrapper)
 
 wtsapi32.dll, winsta.dll, imm32.dll from Windows 2000 Extended Kernel

 Since chrome_elf.dll was added on Chrome 33.0.1712.2 Dev, Chrome 33.0.1750.xxx-50.0.2661.xxx is unofficially possible with using bwc's wrappers, but it freezes within seconds.

Chrome 50.0.2661.102; but 50.0.2661.0 (r377898) / 49.0.2623.112 is recommended (and 34.0.1847.137 for no SSE2) is the last Chrome version observed by the community to run on Windows XP SP1 Build 2600.1050 (using compatibility wrappers), and on certain Windows Longhorn builds up to 4088 under experimental conditions. If on Windows XP Pre-RC 2 build 2517 (2517.main.010713-1717) through Windows XP RTM with Updates (xpclnt_qfe.021108-2107), it is recommended to use the files from XP SP1.

If on Windows 2000 with Extended Kernel, ensure you have InitOnce functions enabled to have Chrome 50 working properly.

 Chrome 49.0.2623.112 can run on Windows XP RC 1 builds 2474 through 2509 (using compatibility wrappers), but problems are found that the browser crashes after file downloading on some file extension is complete. IDM / downloading from Chromium 33.0.1709.0 (r234775) / Chrome 33.0.1707.0 Dev / Chrome 32.0.1700.107 Stable or earlier is recommended.

 Chrome 50.0.2661.102 can run on Windows XP RC 1 builds 2474 through 2509 (using compatibility wrappers), but it is unstable even if using just Browservice, rather than the core itself, as said above Chromium . On the other hand, Chrome 50.0.2661.102 can run on Windows XP Pre-RC 2 build 2517 (2517.main.010713-1717) through Windows Server 2003 SP2, but the browser itself will freeze if loading any most webpages or chrome://downloads is triggered, so using Browservice with it is recommended.

 Chromium 50.0.2661.0 (r378023) through early Chromium 51 builds on Windows XP/2003 without One-Core API is not impossible but it can be unstable.

Chrome 53.0.2785.143 - is the last Chrome version observed by the community to run on Windows Vista build 5360 (using kernel API swaps), and on certain Windows Vista builds and Windows 7 pre-Beta builds up to 68xx or 69xx builds under experimental conditions.
