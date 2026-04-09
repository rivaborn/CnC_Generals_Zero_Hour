# GeneralsMD/Code/Libraries/Source/profile/_pch.h

## Purpose
Precompiled header for the profile module, including common headers and definitions.

## Responsibilities
- Defines include guard `_PCH_H`
- Includes Windows API headers with lean-and-mean configuration
- Includes module-specific headers (`profile.h`, `internal.h`)

## Key Types
- None

## Key Functions
- None

## Globals
- None

## Dependencies
- `<windows.h>` (via `WIN32_LEAN_AND_MEAN` and `STRICT`)
- `profile.h`
- `internal.h`
