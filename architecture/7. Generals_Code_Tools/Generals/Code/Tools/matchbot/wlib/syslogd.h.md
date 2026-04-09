# Generals/Code/Tools/matchbot/wlib/syslogd.h

## Purpose
Header for a cross-platform syslog wrapper class used in the matchbot tool.

## Responsibilities
- Provides a syslog interface for logging messages.
- Inherits from `OutputDevice` for output device functionality.
- Handles platform differences (Windows vs Unix-like systems).
- Manages log priority and facility settings.

## Key Types
- **SyslogD (Class)**: Cross-platform syslog wrapper for logging.

## Key Functions
### SyslogD::SyslogD
- Purpose: Constructor that initializes syslog with given parameters.
- Calls: Not inferable (constructor body not shown).

### SyslogD::print
- Purpose: Writes a string to syslog with specified length.
- Calls: Not inferable (implementation not shown).

## Globals
- None

## Dependencies
- `<stdlib.h>`, `<stdio.h>`, `<syslog.h>` (Unix), `<string.h>`
- `OutputDevice` (base class)
- `odevice.h` (header for `OutputDevice`)
