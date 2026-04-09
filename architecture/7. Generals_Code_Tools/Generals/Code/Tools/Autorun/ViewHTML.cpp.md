# Generals/Code/Tools/Autorun/ViewHTML.cpp

## Purpose
Launches the default web browser to display a specified URL.

## Responsibilities
- Validates input URL
- Creates temporary HTML file for browser detection
- Launches browser process with URL
- Optionally waits for browser to close with callback support

## Key Types
- CallbackHook (Class): Abstract callback interface for wait loop

## Key Functions
### ViewHTML
- Purpose: Launches default browser with specified URL
- Calls: GetWindowsDirectory, GetTempFileName, CreateFile, WriteFile, FindExecutable, DeleteFile, CreateProcess, WaitForInputIdle, GetExitCodeProcess, Sleep

## Globals
- None

## Dependencies
- windows.h (Win32 API)
- ViewHTML.h (header)
- wnd_file.h (Msg function)
- stdio.h (printf/sprintf)
