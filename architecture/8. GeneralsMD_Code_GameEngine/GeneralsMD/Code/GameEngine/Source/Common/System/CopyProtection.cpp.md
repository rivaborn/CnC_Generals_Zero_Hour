# GeneralsMD/Code/GameEngine/Source/Common/System/CopyProtection.cpp

## Purpose
Implements copy protection mechanism for the game, communicating with a launcher process to validate the game's legitimacy.

## Responsibilities
- Checks if the launcher process is running
- Notifies the launcher and waits for validation data
- Validates received data against expected content
- Handles shutdown cleanup

## Key Types
- CopyProtect (Class): manages copy protection logic
- None

## Key Functions
### CopyProtect::isLauncherRunning
- Purpose: Checks if the launcher process is running by attempting to create a named mutex
- Calls: CreateMutex, CloseHandle

### CopyProtect::notifyLauncher
- Purpose: Notifies the launcher to send validation data via Windows messages
- Calls: PeekMessage, OpenEvent, SetEvent, CloseHandle, MapViewOfFileEx

### CopyProtect::checkForMessage
- Purpose: Processes validation messages from the launcher
- Calls: MapViewOfFileEx

### CopyProtect::validate
- Purpose: Validates the received data against expected content
- Calls: strcmp

### CopyProtect::shutdown
- Purpose: Cleans up resources used by the copy protection system
- Calls: UnmapViewOfFile

## Globals
- CopyProtect::s_protectedData (LPVOID): Stores the validation data received from the launcher
- LAUNCHER_GUID (const char*): GUID for the launcher process mutex
- protectGUID (const char*): GUID for the protection event

## Dependencies
- Common/CopyProtection.h
- Windows API (handles, events, messages)
- timeGetTime, Sleep from winmm.h
- DEBUG_LOG macro
