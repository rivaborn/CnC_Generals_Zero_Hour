# Generals/Code/Tools/PATCHGET/registry.cpp

## Purpose
Provides a simple interface for reading and writing values to the Windows Registry.

## Responsibilities
- Read string and unsigned integer values from the registry
- Write string and unsigned integer values to the registry
- Handle both HKEY_LOCAL_MACHINE and HKEY_CURRENT_USER registry hives
- Construct full registry paths for Generals game settings

## Key Types
None

## Key Functions
### getStringFromRegistry
- Purpose: Retrieves a string value from the registry.
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### getUnsignedIntFromRegistry
- Purpose: Retrieves an unsigned integer value from the registry.
- Calls: RegOpenKeyEx, RegQueryValueEx, RegCloseKey

### setStringInRegistry
- Purpose: Writes a string value to the registry.
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### setUnsignedIntInRegistry
- Purpose: Writes an unsigned integer value to the registry.
- Calls: RegCreateKeyEx, RegSetValueEx, RegCloseKey

### GetStringFromRegistry
- Purpose: Retrieves a string value from the Generals registry path.
- Calls: getStringFromRegistry

### GetUnsignedIntFromRegistry
- Purpose: Retrieves an unsigned integer value from the Generals registry path.
- Calls: getUnsignedIntFromRegistry

## Globals
None

## Dependencies
- `<string>`
- `<windows.h>`
- `Registry.h`
