# Generals/Code/Tools/Autorun/GETCD.CPP - Enhanced Analysis

## Architectural Role
This file is part of the installation/autorun toolchain, responsible for CD-ROM drive detection and verification. It bridges the gap between the Windows API and the game's installation tools, ensuring the correct game CD is present before proceeding with installation or launch.

## Cross-References
### Incoming
- Likely called by installation tools (e.g., `SETUP.EXE`) and autorun logic to verify game CDs
- May be referenced by build tools for CD image verification

### Outgoing
- Uses Windows API (`GetVolumeInformation`, `GetDriveType`)
- Depends on `WinVersion` class for OS-specific behavior handling
- Uses `Msg` function from `wnd_file.h` for logging

## Design Patterns
- **Singleton Pattern**: Global `CDList` instance provides centralized CD drive management
- **Adapter Pattern**: Wraps Windows API calls to provide game-specific CD verification
- **Error Handling**: Uses Windows error codes and retry logic for CD changer support

*Not inferable*: Exact usage patterns in installation tools not visible from this file alone.
