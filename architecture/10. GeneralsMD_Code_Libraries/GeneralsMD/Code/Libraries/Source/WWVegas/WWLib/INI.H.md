# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/INI.H

## Purpose
Header file for the INIClass, which handles INI file data storage and retrieval.

## Responsibilities
- Define the INIClass and related structures for INI file operations
- Declare methods for loading/saving INI data in various formats
- Provide accessors for different data types stored in INI entries
- Manage section and entry indexing within INI files

## Key Types
- **INIClass (Class)**: Main class for INI file operations
- **INISection (Struct)**: Not inferable
- **INIEntry (Struct)**: Not inferable
- **PKey (Class)**: Used for key storage

## Key Functions
### Load
- Purpose: Load INI data from a file or stream
- Calls: Not inferable

### Save
- Purpose: Save INI data to a file or stream
- Calls: Not inferable

### Get_Entry
- Purpose: Retrieve an entry from a section by index
- Calls: Not inferable

### Put_String
- Purpose: Store a string value in a section/entry
- Calls: DuplicateCRCError

### DuplicateCRCError
- Purpose: Handle duplicate CRC errors during entry storage
- Calls: Not inferable

## Globals
- **KeepBlankEntries (bool)**: Controls whether blank entries are loaded
- **MAX_LINE_LENGTH (int)**: Maximum line length constant

## Dependencies
- Key includes: wchar.h
- External symbols: FileClass, Straw, Pipe, StringClass, WideStringClass, FileFactoryClass, PKey, TPoint3D, TPoint2D, TRect, List, IndexClass
