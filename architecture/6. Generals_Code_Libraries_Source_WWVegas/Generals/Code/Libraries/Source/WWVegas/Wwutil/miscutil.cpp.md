# Generals/Code/Libraries/Source/WWVegas/Wwutil/miscutil.cpp

## Purpose
Provides utility functions for string manipulation, file operations, and time handling.

## Responsibilities
- String comparison and validation
- File existence and attribute checks
- Time formatting and conversion
- Character classification

## Key Types
- None

## Key Functions
### Get_Text_Time
- Purpose: Returns current time as a formatted string
- Calls: `::time`, `::ctime`, `::strlen`

### Seconds_To_Hms
- Purpose: Converts seconds to hours, minutes, seconds
- Calls: None

### Is_String_Same
- Purpose: Case-insensitive string comparison
- Calls: `::stricmp`

### File_Exists
- Purpose: Checks if a file exists
- Calls: `_TheFileFactory->Get_File`, `_TheFileFactory->Return_File`

### File_Is_Read_Only
- Purpose: Checks if a file is read-only
- Calls: `::GetFileAttributes`

### Get_File_Id_String
- Purpose: Generates a unique identifier string for a file
- Calls: `RawFileClass`, `Get_Image_File_Header`, `StringClass::Format`

## Globals
- None

## Dependencies
- `miscutil.h`, `time.h`, `rawfile.h`, `wwdebug.h`, `win.h`, `mmsys.h`, `ffactory.h`
- `WWASSERT`, `WWDEBUG_SAY`, `StringClass`, `RawFileClass`, `_TheFileFactory`
