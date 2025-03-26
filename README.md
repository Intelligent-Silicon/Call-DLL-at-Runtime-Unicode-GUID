# Demo Clarion AppGen App show casing a variety of techniques.

## General Overview

![Screenshot](https://github.com/Intelligent-Silicon/Call-DLL-at-Runtime-Unicode-GUID/tree/main/ScreenShot.png)

Clarion 11 AppGen Example Application (.App) and Dictionary (.Dct) files.

Loads DLL's dynamically at Runtime.

Uses AppGen Source Procedure's to define dynamically loaded API's to show which procedures are calling dynamically loaded API's.

Uses Assembler to push parameter's onto the Stack.

The Assembler source (.a) file needs to be included in the AppGen Solution Explorer for the Clarion compiler to include.

Loads 16bit DLL at runtime (if running on a 32bit OS) to extract data from 16bit DLL's running in the NTVDM. Ignores if 64bit Windows.

Loads DLL's with the Security Attributes 'Load_Library_Search_System32' & 'Load_Library_Require_Signed_Target' to improve Windows OS security and not bypass Group Policy & AppLocker settings.

****************************** FYI ******************************

The LoadLibraryEx Security Attribute (SA) 'LOAD_IGNORE_CODE_AUTHZ_LEVEL' bypasses Group Policy and AppLocker security settings which is a major security risk, and most organisations dont check that their installed Windows apps are not using this SA for possibly malicious reasons. Its recommended use is only for installation software.

****************************** FYI ******************************

https://learn.microsoft.com/en-us/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa

### Registers, Displays and Unregisters the Power Setting Notification GUIDS.

https://learn.microsoft.com/en-us/windows/win32/power/registering-for-power-events

https://learn.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-registerpowersettingnotification

https://learn.microsoft.com/en-us/windows/win32/power/power-setting-guids

### Converts the Unicode GUIDS into Ansi strings detecting the local machine's Ansi Code Page (ACP).

https://learn.microsoft.com/en-us/windows/win32/api/stringapiset/nf-stringapiset-widechartomultibyte

https://learn.microsoft.com/en-us/windows/win32/api/winnls/nf-winnls-getacp

https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-lstrlenw


### Demo App

ApiUnicode.EXE compiled as a Standalone EXE so it doesnt need any Clarion Runtime DLL'S, just download and run.

ApiUnicode.Exe will generate a False Positive Windows Defender security alert - Behavior:Win32/DefenseEvasion.A!ml, because its not CodeSigned.

 
