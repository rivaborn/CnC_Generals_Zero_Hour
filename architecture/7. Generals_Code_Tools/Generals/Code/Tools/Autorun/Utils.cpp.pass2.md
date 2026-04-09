# Generals/Code/Tools/Autorun/Utils.cpp - Enhanced Analysis

## Architectural Role
This file serves as a utility library for the Autorun tool, providing low-level string manipulation, file I/O, and path handling functions. It bridges the gap between the Autorun tool's specific needs and the underlying Windows API, offering both ANSI and Unicode versions of key functions for compatibility.

## Cross-References
### Incoming
- Autorun tool components likely call these utilities for string processing and file operations
- Other tooling in the Code/Tools directory may depend on path manipulation functions

### Outgoing
- Directly uses Windows API functions (e.g., `lstrcpy`, `wcscpy`)
- Depends on `StandardFileClass` for file operations
- Uses `Args` class for executable path resolution
- Relies on `Locale_GetString` for localization

## Design Patterns
- **Facade Pattern**: Wraps complex Windows API calls (e.g., path manipulation) behind simpler interfaces
- **Adapter Pattern**: Provides both ANSI and Unicode versions of functions to maintain compatibility
- **Utility Class**: Pure collection of static functions without state, following the utility pattern

Key insight: The file shows clear separation between ANSI and Unicode implementations, suggesting the engine was designed with Unicode support from early stages but maintained ANSI for legacy compatibility. The path manipulation functions reveal a focus on robust file system operations for the Autorun tool's installation/deployment workflow.
