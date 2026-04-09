# Generals/Code/Tools/Autorun/ViewHTML.cpp - Enhanced Analysis

## Architectural Role
This file is part of the Autorun tooling infrastructure, specifically handling external browser integration for documentation or help systems. It bridges the game's toolchain with the OS-level browser process, enabling runtime help or modding documentation access.

## Cross-References
### Incoming
- Likely called from Autorun tooling (e.g., help system triggers)
- Potential calls from modding tools (if Autorun is used for mod documentation)

### Outgoing
- Directly uses Win32 API (`CreateProcess`, `FindExecutable`, etc.)
- Depends on `wnd_file.h` for logging (`Msg` function)
- Uses `CallbackHook` for asynchronous wait handling

## Design Patterns
- **Facade Pattern**: Abstracts browser launching complexity behind a simple `ViewHTML` function
- **Temporary Resource Pattern**: Creates/destroys temp files for browser detection
- **Callback Pattern**: Uses `CallbackHook` for non-blocking wait loop control

*Not inferable*: No clear use of Observer or Strategy patterns in this snippet.
