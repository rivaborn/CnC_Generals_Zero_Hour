# GeneralsMD/Code/Libraries/Include/rts/profile.h

## Purpose
Proxy header file for the profile module in the SAGE engine.

## Responsibilities
- Provides a proxy include for the actual profile module header.
- Ensures the profile module is included correctly across the codebase.
- Manages include guards to prevent multiple inclusions.

## Key Types
- None

## Key Functions
- None

## Globals
- None

## Dependencies
- Includes `"../../source/profile/profile.h"` (the actual profile module header).
- Uses `#ifdef _MSC_VER` for Microsoft Visual C++ specific pragmas.
