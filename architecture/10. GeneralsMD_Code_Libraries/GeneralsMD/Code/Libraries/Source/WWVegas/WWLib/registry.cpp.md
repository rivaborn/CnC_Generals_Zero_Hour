# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/registry.cpp

## Purpose
Provides a C++ wrapper for Windows Registry operations, enabling read/write access to registry keys and values.

## Responsibilities
- Wraps Windows Registry API (RegOpenKeyEx, RegSetValueEx, etc.)
- Supports integer, float, boolean, string, and binary data types
- Handles registry key creation, deletion, and enumeration
- Provides INI file import/export for registry data
- Manages registry locking/unlocking

## Key Types
- RegistryClass (Class): Main wrapper for registry operations
- None (other types are Windows API structs/enums)

## Key Functions
### RegistryClass::RegistryClass
- Purpose: Constructor that opens or creates a registry key
- Calls: RegCreateKeyEx, RegOpenKeyEx

### RegistryClass::Get_Int / Set_Int
- Purpose: Read/write integer values from/to registry
- Calls: RegQueryValueEx, RegSetValueEx

### RegistryClass::Save_Registry_Tree
- Purpose: Recursively save registry keys/values to an INI file
- Calls: RegEnumKeyEx, RegQueryInfoKey, INIClass methods

### RegistryClass::Delete_Registry_Tree
- Purpose: Recursively delete registry keys and values
- Calls: RegEnumKeyEx, RegDeleteKey, RegDeleteValue

## Globals
- IsLocked (bool): Tracks if registry is in read-only mode

## Dependencies
- Windows.h (for registry API)
- registry.h (header)
- ini.h, inisup.h (INI file handling)
- rawfile.h (file I/O)
- assert.h (debug assertions)
