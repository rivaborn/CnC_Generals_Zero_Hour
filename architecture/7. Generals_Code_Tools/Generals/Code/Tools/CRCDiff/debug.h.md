# Generals/Code/Tools/CRCDiff/debug.h

## Purpose
Provides conditional debug logging functionality for the CRCDiff tool.

## Responsibilities
- Defines `DEBUG_LOG` macro for conditional debug output
- Declares `DebugLog` function for formatted logging
- Includes guard against multiple inclusions

## Key Types
- None

## Key Functions
### DebugLog
- Purpose: Outputs formatted debug messages to the log.
- Calls: `va_list` handling (via `cstdarg`)

## Globals
- None

## Dependencies
- `<cstdarg>` for variable argument handling
- `DEBUG` preprocessor symbol to control debug output
