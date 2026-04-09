# Generals/Code/Tools/wolSetup/wolSetup.h - Enhanced Analysis

## Architectural Role
This header defines the interface for the Windows Online (WOL) setup subsystem, which handles installation verification and configuration for the online multiplayer component of Generals. It bridges the game's installation process with the WOL API, ensuring compatibility before online features are enabled.

## Cross-References
### Incoming
- Likely called by the game's installer or launcher executable (e.g., `Generals.exe` or `setup.exe`) during initialization.
- May be referenced by the WOL client or matchmaking components for version validation.

### Outgoing
- Interacts with Windows Registry APIs (via `windows.h`) to read WOL API version.
- Uses file I/O operations (implied by `MAX_PATH` paths) to verify WOL API installation.

## Design Patterns
- **Facade Pattern**: Abstracts the complexity of WOL API version checking and setup into simple functions (`checkInstalledWolapiVersion`, `setupGenerals`).
- **Global State**: Uses module-level globals to track WOL API state, avoiding repeated registry/file checks.
- **Utility Functions**: `MAJOR`/`MINOR` macros encapsulate version number parsing logic, promoting reusability.
