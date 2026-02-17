| Chrome Version | Function/DLL file) | Windows Build | Notes |
| :--- | :---: | :---: | ---:
| 0.2.152.0 | SystemFunction036 (ADVAPI32.DLL) | Introduced in Windows XP build 2410 | Removed Windows 2000 compatibility without wrappers.
| 5.0.317.0 | WTSQueryUserToken (WTSAPI32.DLL) | Introduced in Windows XP build 2481 | Requires workarounds for Windows XP build 2475 and lower (like drag+drop WTSAPI32.DLL and WINSTA.DLL from XP SP3 to the Chrome-bin folder)
| 5.0.366.0 | CancelIPChangeNotify (IPHLPAPI.DLL) | Introduced in Windows XP SP2 builds |
| 21.0.1145.0 | EncodePointer/DecodePointer (KERNEL32.DLL) | Introduced in Windows XP build 2600.2055 | Removed Windows XP SP1 compatibility without wrappers.
| 23.0.1255.0 | ImmDisableTextFrameService (IMM32.DLL) | Introduced in Windows Server 2003 build 3604 / Windows XP SP1 build 2600.1050 (but 3590 was incomplete) | Requires workarounds for Windows XP RTM/2000 SP4
| 50.0.2661.0 | InitOnce functions (KERNEL32.DLL) | Introduced in Windows Vista build 5360 |
