# Generals/Code/Tools/PATCHGET/PROCESS.CPP - Enhanced Analysis

## Architectural Role
This file is part of the build/patching toolchain, providing low-level process management for launching external tools (e.g., patchers, updaters). It abstracts Windows process creation/synchronization, likely used during game installation or update workflows.

## Cross-References
### Incoming
- Not inferable (no callers visible in this file)

### Outgoing
- **Windows API**: `CreateProcess`, `WaitForSingleObject`, `GetExitCodeProcess`
- **Internal**: `ConfigFile` (for parsing), `Wstring` (string manipulation), `DBGMSG` (debug logging)

## Design Patterns
- **Facade Pattern**: Wraps Windows process APIs into simpler `Process` class methods.
- **Resource Management**: Uses RAII-like pattern for process handles (though manual cleanup is not shown).
- **Parser Pattern**: `Read_Process_Info` uses token-based parsing for config strings.

*Not inferable*: No clear use of Observer, Strategy, or other patterns.
