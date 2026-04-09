# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/registry.h

## Purpose
Header file defining the `RegistryClass` for Windows registry access and manipulation.

## Responsibilities
- Provides interface for reading/writing registry values (int, bool, float, string, binary).
- Supports registry key enumeration and bulk operations (load/save/delete).
- Manages registry key validity and read-only state.

## Key Types
- `RegistryClass` (Class): wraps Windows registry operations.
- `INIClass` (Class): referenced but not defined here (likely for INI file handling).

## Key Functions
### `RegistryClass::Exists`
- Purpose: Checks if a registry sub-key exists.
- Calls: Not inferable.

### `RegistryClass::Get_Int`
- Purpose: Retrieves an integer value from the registry.
- Calls: Not inferable.

### `RegistryClass::Set_Int`
- Purpose: Writes an integer value to the registry.
- Calls: Not inferable.

### `RegistryClass::Delete_Registry_Tree`
- Purpose: Deletes an entire registry subtree.
- Calls: `Delete_Registry_Values`.

### `RegistryClass::Load_Registry`
- Purpose: Loads registry data from an INI file.
- Calls: Not inferable.

### `RegistryClass::Save_Registry`
- Purpose: Saves registry data to an INI file.
- Calls: `Save_Registry_Tree`.

## Globals
- `RegistryClass::IsLocked` (bool): Controls read-only mode for the registry.

## Dependencies
- `always.h`, `vector.h`, `wwstring.h`, `widestring.h`
- Windows registry API (`HKEY` type).
