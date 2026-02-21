# HOME

* https://github.com/unclecaptain5426/legacy-windows-chrome-compat/blob/main/faq.md

  Frequently Asked Questions

* https://github.com/unclecaptain5426/legacy-windows-chrome-compat/blob/main/compatibility.md

  Compatibility Notes

* https://github.com/unclecaptain5426/legacy-windows-chrome-compat/blob/main/dependencies.md

  Dependencies

# BUGS, QUIRKS, AND KNOWN LIMITATIONS

## Version Limitations

### Chrome 5.0.375.17 Dev / Chrome 4.1.249.1064 Limitation
Chrome 5.0.375.23 Beta and up will not run on Windows Longhorn build 4093 through Windows Vista Beta 2 Build 5356 due to kernel constraints.

### Early Builds of Chrome 6 / Chrome 5.0.375.127 Limitation 
Google Chrome 6.0.41x and up will not run on Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296, due to an hardcoded SystemFunction036 on ADVAPI32.D.LL and a function that needs an unofficial for NTDLL.DLL.

### Chrome 33.0.1707.0 Dev / Chrome 32.0.1700.107 Limitation 
Chrome 33.0.1712.2 Dev or later can launch, but it is unstable on Windows 2000 SP4 + Update Rollup 1 + All Updates (without Extended Kernel) when using advapixp.dll, kernelxp.dll, and userxp.dll wrappers by BWC / Windows Whistler Beta 1 Build 2410 - Windows Whistler Beta 2 Build 2469 when using kernelxp.dll wrappers by BWC (because it starts but freezes within seconds) due to chrome_elf.dll being stricted.

### Chrome 51-58 blocked on NT 5.x
Because Chrome 51-58 doesn't work on NT 5.x, you must need to use NNN4NT5 to tweak it to Vista or higher, but it requires at least Microsoft Windows XP RTM with One-Core API or newer.

## IE7/8 quirk on XP RTM
### For Chrome 23.0.1255.0 Dev or later
If Internet Explorer 7 or 8 is installed on Windows XP RTM, and if you have an imm32.dll from another version, it must be on C:\WINDOWS instead of C:\WINDOWS\SYSTEM32, and you also need to edit the registry to change the userinit value to C:\WINDOWS\explorer.exe.

# NOTES

Make sure you have 7-Zip & CFF Explorer installed.

If you are on a non-XP SP2 system... make sure you use --no-sandbox command line.

If you are looking for an modern version of Chromium, use the following:

https://github.com/e3kskoy7wqk/Chromium-for-windows-7-REWORK

It can only work at least Windows XP build 2481 unofficially

https://github.com/win32ss/supermium

It can only work at least Windows XP build 2517 unofficially

https://github.com/ttalvitie/browservice

If you want the modern web for older Chromium browsers; ideal for Windows 2000 build 1964 and later with using older versions of Chromium.

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
