# GeneralsMD/Code/Libraries/Source/WWVegas/Wwutil/miscutil.h

## Purpose
Header file defining utility functions for string manipulation, file operations, and time formatting.

## Responsibilities
- Provides static utility methods for string comparison, character classification, and file operations.
- Includes time conversion utilities (seconds to hours/minutes/seconds).
- Offers basic file existence and read-only checks.
- Contains whitespace trimming and file removal functionality.

## Key Types
- cMiscUtil (Class): Container for static utility methods.

## Key Functions
### Get_Text_Time
- Purpose: Returns formatted text time.
- Calls: Not inferable.

### Seconds_To_Hms
- Purpose: Converts seconds to hours, minutes, and seconds.
- Calls: Not inferable.

### Is_String_Same / Is_String_Different
- Purpose: Case-sensitive string comparison utilities.
- Calls: Not inferable.

### Get_File_Id_String
- Purpose: Generates a file ID string from a filename.
- Calls: Not inferable.

### File_Exists / File_Is_Read_Only
- Purpose: Checks file existence and read-only status.
- Calls: Not inferable.

### Is_Alphabetic / Is_Numeric / Is_Alphanumeric / Is_Whitespace
- Purpose: Character classification functions.
- Calls: Not inferable.

### Trim_Trailing_Whitespace
- Purpose: Removes trailing whitespace from a string.
- Calls: Not inferable.

### Remove_File
- Purpose: Deletes a file from the filesystem.
- Calls: Not inferable.

## Globals
- MISCUTIL_EPSILON (float): Small epsilon value for floating-point comparisons.

## Dependencies
- "always.h", "bittype.h", "wwstring.h"
- LPCSTR,
