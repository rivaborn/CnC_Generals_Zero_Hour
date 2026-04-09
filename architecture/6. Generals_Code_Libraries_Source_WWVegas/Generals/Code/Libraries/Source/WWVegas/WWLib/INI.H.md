# Generals/Code/Libraries/Source/WWVegas/WWLib/INI.H

## Purpose
Header file defining the `INIClass` for reading/writing Windows-style INI files.

## Responsibilities
- Parse and manage INI file data structures
- Provide typed get/put operations for INI entries
- Handle section and entry lookups
- Support various data types (bool, int, float, string, rect, point, etc.)

## Key Types
- **INIClass (Class)**: Main INI file handler
- **INISection (Struct)**: Not inferable
- **INIEntry (Struct)**: Not inferable

## Key Functions
### `Load`
- Purpose: Load INI data from file/straw
- Calls: Not inferable

### `Save`
- Purpose: Save INI data to file/pipe
- Calls: Not inferable

### `Get_*`
- Purpose: Retrieve typed values from INI entries
- Calls: Not inferable

### `Put_*`
- Purpose: Store typed values into INI entries
- Calls: Not inferable

### `Find_Section`
- Purpose: Locate a section by name
- Calls: Not inferable

### `Find_Entry`
- Purpose: Locate an entry within a section
- Calls: Not inferable

## Globals
- **SectionList (List<INISection *>)**: List of all sections
- **SectionIndex (IndexClass<int, INISection *>)**: Index for section lookup

## Dependencies
- `PKey`, `FileClass`, `Straw`, `Pipe`, `StringClass`, `FileFactoryClass`
- Template classes: `TPoint3D`, `TPoint2D`, `TRect`, `List`, `IndexClass`
