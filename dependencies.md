| Chrome Version | Function/DLL file) | Windows Build | Notes |
| :--- | :---: | :---: | ---:
| 0.2.152.0 | SystemFunction036 (ADVAPI32.DLL) | Introduced in Windows XP build 2410 | Removed Windows 2000 compatibility without BWC's wrappers.
| 2.0.178.0 | GetNativeSystemInfo (KERNEL32.DLL) | Introduced in Windows XP build 2481 | Requires workarounds for Windows XP build 2475 and lower (like changing the function to GetSystemInfo, but on some computers and virtualizers, going past Chrome 12.0.729/11.0.696.77 leads to c0000094 (CPU division-by-zero) errors, but it can be managed by using BWC's wrappers (but up to Chrome 33.0.1707.0/32.0.1700.107 unfortunately))
| 4.0.249.xx | GetProcessId (KERNEL32.DLL) | Introduced in Windows XP build 2600.1078 | Removed Windows XP RTM compatibility, however it can be managed by changing the function to GetStdHandle.
| 5.0.317.0 | WTSQueryUserToken (WTSAPI32.DLL) | Introduced in Windows XP build 2481 | Requires workarounds for Windows XP build 2475 and lower (like drag+drop WTSAPI32.DLL and WINSTA.DLL from XP SP3 to the Chrome-bin folder)
| 5.0.366.0 | CancelIPChangeNotify (IPHLPAPI.DLL) | Introduced in Windows XP SP2 builds |
| 21.0.1145.0 | EncodePointer/DecodePointer (KERNEL32.DLL) | Introduced in Windows XP build 2600.2055 | Removed Windows XP SP1 compatibility without wrappers.
| 23.0.1255.0 | ImmDisableTextFrameService (IMM32.DLL) | Introduced in Windows Server 2003 build 3604 / Windows XP SP1 build 2600.1050 (but 3590 was incomplete) | Requires workarounds for Windows XP RTM/2000 SP4
| 50.0.2661.0 | InitOnce functions (KERNEL32.DLL) | Introduced in Windows Vista build 5360 | If InitOnceExecuteOnce is replaced with InterlockedChange, it would be unstable and can crash easily on XP/Server 2003.
