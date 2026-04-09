# Generals/Code/Tools/Autorun/autorun.h - Enhanced Analysis

## Architectural Role
This header defines the core classes and constants for the autorun tool, which is responsible for launching the game, demos, and other utilities from the installation directory. It serves as the bridge between the Windows shell and the game's executable, handling language selection, registry access, and process spawning.

## Cross-References
### Incoming
- Likely called by the autorun executable's main function (not shown in header)
- May be referenced by setup/installer tools for shared constants

### Outgoing
- Uses Windows API (HWND, HINSTANCE) for GUI and process creation
- References registry paths for installation management
- Depends on `ttfont.h` for text rendering (though not directly used in this header)

## Design Patterns
- **Singleton-like pattern**: `LaunchObject` is a global instance of `LaunchObjectClass`
- **Template Method**: `Window` is an abstract base class with pure virtual `Window_Proc`
- **Command pattern**: `LaunchObjectClass` encapsulates the command to launch a program

Rules followed. Output under 400 tokens.
