# Generals/Code/Tools/Autorun/IGR.h - Enhanced Analysis

## Architectural Role
This file defines the interface for accessing Westwood Online (WOL) registry settings, serving as a bridge between the game's online features and Windows registry storage. It encapsulates platform-specific registry operations, abstracting them for use by higher-level online systems.

## Cross-References
### Incoming
- Likely called by online login systems (e.g., `Generals/Code/Game/Online/OnlineLogin.cpp`) to check auto-login permissions
- Used by nick management systems (e.g., `Generals/Code/Game/Online/NickManager.cpp`) for nick storage policies
- Referenced by registry app launchers (e.g., `Generals/Code/Game/Online/RegistryApp.cpp`) for execution control

### Outgoing
- Interacts with Windows Registry API (via `Init` and `Set_Options`)
- No other subsystem calls are inferable from this header alone

## Design Patterns
- **Singleton-like pattern**: Global `OnlineOptions` instance suggests a singleton-like usage, though not strictly enforced
- **Flag-based configuration**: Uses bitflags (`IGROptionsType`) for compact option storage and manipulation
- **Facade pattern**: Abstracts Windows Registry complexity behind a simple class interface
