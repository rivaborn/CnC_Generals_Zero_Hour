# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/ini.cpp

## Purpose
Handles INI file parsing, storage, and retrieval operations for the game engine.

## Responsibilities
- Load/save INI data from/to files or streams
- Store/retrieve various data types (strings, integers, floats, points, rectangles, etc.)
- Manage INI sections and entries with indexing
- Handle encoded data blocks and public key storage

## Key Types
- `INIClass`: Main INI file handler class
- `INISection`: Represents a section in an INI file
- `INIEntry`: Represents an entry within a section
- `INIEntryIndex`: Index for entries within a section
- `INISectionIndex`: Index for sections within the INI file

## Key Functions
### `Load(Straw & ffile)`
- Purpose: Load INI data from a data stream
- Calls: `Strip_Comments`, `Find_Section`, `Find_Entry`, `DuplicateCRCError`

### `Save(XPipe & ffile)`
- Purpose: Save INI data to a pipe stream
- Calls: `SectionList->Count`, `SectionList->Get_Head`, `SectionList->Get_Next`, `EntryList->Count`, `EntryList->Get_Head`, `EntryList->Get_Next`

### `Get_String(char const * section, char const * entry, char const * defvalue, char * buffer, int buflen) const`
- Purpose: Retrieve a string value from the INI database
- Calls: `Find_Section`, `Find_Entry`

### `Put_String(char const * section, char const * entry, char const * value)`
- Purpose: Store a string value into the INI database
- Calls: `Find_Section`, `Find_Entry`

### `Get_Point(char const * section, char const * entry, TPoint2D<int> const & defvalue) const`
- Purpose: Retrieve a 2D point value from the INI database
- Calls: `Get_String`

### `Put_Point(char const * section, char const * entry, TPoint2D<int> const & value)`
- Purpose: Store a 2D point value to the INI database
- Calls: `Put_String`

## Globals
- `KeepBlankEntries` (bool): Controls whether blank entries are kept
- `MAX_LINE_LENGTH` (const int): Maximum line length for INI files

## Dependencies
- `ini.h`, `b64pipe.h`, `b64straw.h`, `cstraw.h`, `readline.h`, `trim.h`, `win.h`, `xpipe.h`, `xstraw.h`, `stdio.h`, `malloc.h`, `rawfile.h`, `ffactory.h`, `inisup.h`, `trect.h`, `wwfile.h`, `pk.h`, `pipe.h`, `wwstring.h`, `widestring.h`, `nstrdup.h`
- `List`, `IndexClass`, `FileClass`, `Straw`, `XPipe`, `PKey`, `CRC`, `BigInt`
