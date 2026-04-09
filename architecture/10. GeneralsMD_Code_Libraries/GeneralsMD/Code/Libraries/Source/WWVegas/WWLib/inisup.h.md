# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/inisup.h

## Purpose
Defines support structures for INI file parsing, including entry and section representations.

## Responsibilities
- Declares `INIEntry` and `INISection` classes for INI data storage
- Provides CRC-based indexing for entries and sections
- Manages linked lists of entries and sections
- Supports lookup of entries by name

## Key Types
- **INIEntry (Class)**: Represents a key-value pair in an INI file
- **INISection (Class)**: Represents a section in an INI file, containing a list of entries

## Key Functions
### INIEntry::Index_ID
- Purpose: Generates a CRC-based index for the entry
- Calls: `CRC::String`

### INISection::Find_Entry
- Purpose: Finds an entry by its name in the section
- Calls: Not inferable

### INISection::Index_ID
- Purpose: Generates a CRC-based index for the section
- Calls: `CRC::String`

## Globals
None

## Dependencies
- `listnode.h` (for `Node` and `List` templates)
- `index.h` (for `IndexClass`)
- `crc.h` (for `CRC::String`)
