# Generals/Code/Tools/mangler/wlib/syslogd.cpp

## Purpose
Implements a cross-platform syslog wrapper for logging messages, with Windows-specific exclusion.

## Responsibilities
- Initializes syslog connection on non-Windows platforms
- Provides a print method to log messages
- Manages memory for temporary log strings

## Key Types
- SyslogD (Class): syslog wrapper with platform-specific behavior

## Key Functions
### SyslogD::SyslogD
- Purpose: Constructor initializes syslog with given parameters
- Calls: openlog (non-Windows)

### SyslogD::print
- Purpose: Logs a string via syslog with specified priority
- Calls: memset, strncpy, syslog (non-Windows), delete[]

## Globals
- None

## Dependencies
- "syslogd.h" (header)
- openlog, syslog (POSIX syslog functions)
- memset, strncpy, delete[] (C/C++ standard library)
