# Generals/Code/Tools/Launcher/Protect.cpp - Enhanced Analysis

## Architectural Role
This file implements the copy protection system for the game launcher, acting as a bridge between the launcher and the game process. It handles file decryption and inter-process communication to ensure protected game assets are accessible only when the launcher is active.

## Cross-References
### Incoming
- Not inferable (no callers visible in this file)

### Outgoing
- Calls into `BFish.h` (Blowfish encryption)
- Uses `File.h` for file operations
- Interacts with Windows API (`windows.h`) for mutexes, memory mapping, and messaging
- References `CdaPfn.h` for CDA function declarations

## Design Patterns
- **Singleton-like behavior**: The protection system maintains global state (`mLauncherMutex`, `mMappedFile`) with initialization/shutdown functions.
- **Inter-process communication (IPC)**: Uses Windows events and messages (`PostThreadMessage`) to coordinate with the game process.
- **Resource management**: Explicit cleanup in `ShutdownProtect` follows RAII-like principles for Windows handles.
