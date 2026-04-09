# Generals/Code/Tools/Launcher/patch.cpp

## Purpose
Handles patch application logic for the game launcher, including registry updates, file patches, and system restarts.

## Responsibilities
- Apply different patch types (.exe, .rtp, .exn, .web)
- Update registry with patch version info
- Display patch progress via dialog
- Handle system shutdown/restart for critical patches

## Key Types
- PATCHCALLBACK (Class): Callback interface for patching process
- PATCHFUNC (Class): Function pointer type for patch application

## Key Functions
### Update_Info_Proc
- Purpose: Dialog procedure for displaying patch information
- Calls: SendDlgItemMessage, EndDialog

### Shutdown_Computer_Now
- Purpose: Initiates system reboot for critical patches
- Calls: OpenProcessToken, LookupPrivilegeValue, AdjustTokenPrivileges, ExitWindowsEx

### PatchCallBack
- Purpose: Handles patching progress callbacks
- Calls: SendMessage, SetWindowText, MessageBox, fopen/fclose

### Apply_Patch
- Purpose: Main patch application function
- Calls: RegCreateKeyEx, RegSetValueEx, LoadLibrary, GetProcAddress, ShellExecute, Create_Process

## Globals
- None

## Dependencies
- patch.h
- shellapi.h
- direct.h
- Windows API (registry, process, dialog functions)
- External DLL: patchw32.dll (RTPatchApply32)
