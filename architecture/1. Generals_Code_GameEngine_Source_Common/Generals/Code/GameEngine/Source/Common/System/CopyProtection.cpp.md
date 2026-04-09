# Generals/Code/GameEngine/Source/Common/System/CopyProtection.cpp

## Purpose
This file implements copy protection mechanisms for the Command & Conquer Generals game, ensuring that only authorized launchers can run the game.

## Responsibilities
- Checks if the launcher is running.
- Notifies the launcher and waits for a response.
- Validates received data from the launcher.
- Handles shutdown procedures to clean up resources.

## Key Types
- CopyProtect (Class): Manages copy protection logic.

## Key Functions
### isLauncherRunning
- Purpose: Determines if the launcher process is running.
- Calls: CreateMutex, GetLastError, CloseHandle

### notifyLauncher
- Purpose: Notifies the launcher and waits for a response with protected data.
- Calls: PeekMessage, OpenEvent, SetEvent, CloseHandle, MapViewOfFileEx

### checkForMessage
- Purpose: Handles messages from the launcher.
- Calls: MapViewOfFileEx

### validate
- Purpose: Validates the received protected data.
- Calls: strcmp

### shutdown
- Purpose: Cleans up resources used in copy protection.
- Calls: UnmapViewOfFile

## Globals
- s_protectedData (LPVOID): Stores the mapped view of the file containing protected data.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/CopyProtection.h"
- External symbols:
  - CreateMutex, GetLastError, CloseHandle, PeekMessage, OpenEvent, SetEvent, MapViewOfFileEx, UnmapViewOfFile, timeGetTime, FindWindow
