# Generals/Code/Tools/Launcher/main.cpp - Enhanced Analysis

## Architectural Role
This file is the entry point for the game launcher, bridging the installation/patching system with the main game executable. It handles patch application, process management, and conditional execution of secondary launchers (e.g., for copy protection).

## Cross-References
### Incoming
- **matchbot/main.cpp**: Calls `Signal_Quit` (likely for shutdown coordination).
- **WW3D/max2w3d/dllmain.cpp**: References `LibClassDesc`, `LibDescription`, etc. (unclear direct link; possibly shared utility functions).

### Outgoing
- **patch.h/findpatch.h**: Patch discovery/application logic.
- **process.h**: Process creation/waiting (Windows API wrappers).
- **configfile.h**: Configuration parsing (`launcher.cfg`).
- **Protect.h** (COPY_PROTECT): Copy protection integration.

## Design Patterns
- **Command Pattern**: Encapsulates process execution (`Process` struct + `Create_Process`).
- **Strategy Pattern**: Conditional execution paths for primary/secondary launchers.
- **Singleton-like**: Global `Global_instance` for Windows app instance (implicit).

*Not inferable*: No clear use of Observer or Factory patterns.
