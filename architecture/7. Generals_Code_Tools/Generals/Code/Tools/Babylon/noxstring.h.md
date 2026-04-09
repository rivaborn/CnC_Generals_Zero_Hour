# Generals/Code/Tools/Babylon/noxstring.h

## Purpose
Header file for the NOXSTRING application, defining the main application class and global variables for localization string management.

## Responsibilities
- Declares the main application class `CNoxstringApp`.
- Defines global variables for localization databases and file paths.
- Provides a function to check if Excel is running.

## Key Types
- **CNoxstringApp (Class)**: Main application class inheriting from `CWinApp`.
- **TransDB (Type)**: External type for translation database (included from "transdb.h").

## Key Functions
### `ExcelRunning`
- Purpose: Checks if Excel is running.
- Calls: Not inferable.

### `CNoxstringApp::InitInstance`
- Purpose: Initializes the application instance.
- Calls: Not inferable.

## Globals
- **NoxstrDB (TransDB*)**: Pointer to the NOXSTRING translation database.
- **MainDB (TransDB*)**: Pointer to the main translation database.
- **NoxstrFilename (char[])**: Filename for the NOXSTRING database.
- **MainXLSFilename (char[])**: Filename for the main Excel database.
- **RootPath (char[])**: Root path for localization files.
- **DialogPath (char[])**: Path for dialog resources.
- **CurrentLanguage (LangID)**: Current language ID.

## Dependencies
- `"resource.h"`: Main symbols.
- `"transdb.h"`: Translation database definitions.
- `CWinApp`: Base class for MFC applications.
- `DECLARE_MESSAGE_MAP()`: MFC macro for message map declaration.
