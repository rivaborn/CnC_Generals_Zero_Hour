# Generals/Code/Tools/Launcher/Protect.cpp

## Purpose
Implements copy protection for the game launcher by decrypting protected files and communicating with the game process.

## Responsibilities
- Initialize and manage protection mechanisms (mutex, memory mapping)
- Decrypt protected game files using Blowfish algorithm
- Generate passkey from system/registry data
- Communicate with game process via Windows messages
- Clean up protection resources

## Key Types
- `BlowfishEngine` (Class): Encryption/decryption engine
- `CDAPFN_DECLARE_GLOBAL` (Macro): Declares a global CDA function
- `SECURITY_ATTRIBUTES` (Struct): Windows security attributes

## Key Functions
### `InitializeProtect`
- Purpose: Sets up protection mutex and memory-mapped file
- Calls: `CreateMutex`, `CreateFileMapping`, `PrintWin32Error`

### `SendProtectMessage`
- Purpose: Decrypts protected file and sends handle to game process
- Calls: `MapViewOfFileEx`, `BlowfishEngine::Decrypt`, `PostThreadMessage`, `WaitForMultipleObjects`

### `ShutdownProtect`
- Purpose: Cleans up protection resources
- Calls: `CloseHandle`

## Globals
- `LAUNCHER_GUID` (const char*): Unique launcher identifier
- `protectGUID` (const char*): Unique protection identifier
- `mLauncherMutex` (HANDLE): Protection mutex handle
- `mMappedFile` (HANDLE): Memory-mapped file handle

## Dependencies
- `Protect.h`, `BFish.h`, `UString.h`, `RefPtr.h`, `File.h`
- Windows API: `windows.h`, `DebugPrint.h`
- SafeDisk: `CdaPfn.h`
