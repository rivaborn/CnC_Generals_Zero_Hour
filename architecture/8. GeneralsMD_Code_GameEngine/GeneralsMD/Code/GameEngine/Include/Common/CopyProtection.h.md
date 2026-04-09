# GeneralsMD/Code/GameEngine/Include/Common/CopyProtection.h

## Purpose
Header file declaring the CopyProtect class for anti-piracy checks in Generals Zero Hour.

## Responsibilities
- Declares static methods for copy protection validation
- Provides interface for launcher communication
- Handles message checking for copy protection
- Manages shutdown of copy protection systems

## Key Types
- CopyProtect (Class): Manages copy protection validation and launcher communication

## Key Functions
### isLauncherRunning
- Purpose: Checks if the copy protection launcher is running
- Calls: Not inferable

### notifyLauncher
- Purpose: Notifies the copy protection launcher
- Calls: Not inferable

### checkForMessage
- Purpose: Checks for copy protection messages
- Calls: Not inferable

### validate
- Purpose: Validates the copy protection status
- Calls: Not inferable

### shutdown
- Purpose: Shuts down copy protection systems
- Calls: Not inferable

## Globals
- s_protectedData (LPVOID): Static member for protected data storage

## Dependencies
- Windows API types (UINT, LPARAM, LPVOID)
- Bool type (likely from game engine)
- DO_COPY_PROTECTION macro control
