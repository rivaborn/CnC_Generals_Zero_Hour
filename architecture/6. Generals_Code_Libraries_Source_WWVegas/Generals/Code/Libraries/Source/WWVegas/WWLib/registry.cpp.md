# Generals/Code/Libraries/Source/WWVegas/WWLib/registry.cpp

## Purpose
Implements a wrapper class for Windows Registry operations, providing type-safe access to registry keys and values.

## Responsibilities
- Encapsulates Windows Registry API calls
- Provides methods for reading/writing various data types (int, float, bool, string, binary)
- Manages registry key lifecycle (creation/closure)
- Supports both ANSI and Unicode string operations

## Key Types
- RegistryClass (Class): Wrapper for Windows Registry operations
- None (other types are standard or from external headers)

## Key Functions
### RegistryClass::RegistryClass
- Purpose: Constructs and opens a registry key
- Calls: RegCreateKeyEx

### RegistryClass::Get_Int
- Purpose: Retrieves an integer value from the registry
- Calls: RegQueryValueEx

### RegistryClass::Set_Int
- Purpose: Writes an integer value to the registry
- Calls: RegSetValueEx

### RegistryClass::Get_String
- Purpose: Retrieves a string value from the registry (ANSI version)
- Calls: RegQueryValueEx

### RegistryClass::Set_String
- Purpose: Writes a string value to the registry (ANSI version)
- Calls: RegSetValueEx

### RegistryClass::Get_Value_List
- Purpose: Enumerates all value names under a registry key
- Calls: RegEnumValue

## Globals
- None

## Dependencies
- registry.h (header)
- windows.h (for Windows Registry API)
- assert.h (for assertions)
- StringClass, WideStringClass, DynamicVectorClass (from WWLib)
