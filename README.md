# Call-DLL-at-Runtime-Unicode-GUID

Loads DLL's dynamically at Runtime.

Uses Assembler to push data onto the Stack.

Loads 16bit DLL at runtime, if running on a 32bit OS to extract data from 16bit DLL's.

Loads DLL with the Security Attributes Load_Library_Search_System32 & Load_Library_Require_Signed_Target to improve system security.

https://learn.microsoft.com/en-us/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa

Registers, Display and Unregisters the Power Setting Events.

https://learn.microsoft.com/en-us/windows/win32/power/registering-for-power-events

https://learn.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-registerpowersettingnotification

https://learn.microsoft.com/en-us/windows/win32/power/power-setting-guids

Converts Unicode GUIDS into Ansi Strings detecting the local machine's Ansi Code Page (ACP).

https://learn.microsoft.com/en-us/windows/win32/api/stringapiset/nf-stringapiset-widechartomultibyte

https://learn.microsoft.com/en-us/windows/win32/api/winnls/nf-winnls-getacp

https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-lstrlenw

Exe will trigger a Windows Defender security alert - Behavior:Win32/DefenseEvasion.A!ml because its not currently code signed.


 
