# Generals/Code/Tools/matchbot/global.h

## Purpose
Header file defining the global state and utilities for the matchbot tool.

## Responsibilities
- Declares the `GlobalClass` singleton for configuration and random number generation
- Provides log rotation functions
- Manages configuration file reading and string retrieval

## Key Types
- **GlobalClass (Class)**: Singleton managing configuration, random number generation, and file I/O
- **None** for other symbols

## Key Functions
### `rotateOutput`
- Purpose: Rotates output logs.
- Calls: Not inferable

### `rotateParanoid`
- Purpose: Rotates logs in a paranoid (safer) mode.
- Calls: Not inferable

## Globals
- **Global (GlobalClass)**: Singleton instance for global state access

## Dependencies
- `<wstypes.h>`, `<configfile.h>`, `<critsec.h>`, `<threadfac.h>`, `<tcp.h>`
- `matcher.h`, `rand.h`
- `ConfigFile`, `Wstring`, `RandClass` (external types)
