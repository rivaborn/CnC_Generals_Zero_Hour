# Generals/Code/Tools/Autorun/ARGS.H - Enhanced Analysis

## Architectural Role
This file provides a lightweight command-line argument parser specifically for the Autorun tool, enabling configuration via command-line flags. It abstracts Windows-specific argument handling into a reusable class, supporting tool automation in the build pipeline.

## Cross-References
### Incoming
- Likely called by `Generals/Code/Tools/Autorun/ARGS.CPP` (implementation) and Autorun tool entry point (e.g., `WinMain`).

### Outgoing
- Uses Windows API types (`HINSTANCE`, `LPTSTR`) but no direct subsystem calls.

## Design Patterns
- **Singleton-like**: Global `Args` instance suggests intended single-use per process.
- **Facade**: Hides Windows command-line parsing complexity behind simple methods.
- **Fixed-size buffer**: Uses static arrays (`MAX_COMMAND_LINE_ARGUMENTS`, `MAX_ARGUMENT_LENGTH`), limiting flexibility but ensuring safety.

*Not inferable: No clear use of other patterns (e.g., no inheritance, factories, or observers).*
