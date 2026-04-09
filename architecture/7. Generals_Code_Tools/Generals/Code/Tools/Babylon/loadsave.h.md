# Generals/Code/Tools/Babylon/loadsave.h

## Purpose
Header file for database loading and saving functionality in the Babylon tool.

## Responsibilities
- Declares functions for writing and loading translation databases
- Provides label count retrieval for database files
- Supports progress dialog during operations

## Key Types
- None

## Key Functions
### WriteMainDB
- Purpose: Writes a translation database to a file with optional progress dialog
- Calls: Not inferable

### LoadMainDB
- Purpose: Loads a translation database from a file with optional callback
- Calls: Not inferable

### GetLabelCountDB
- Purpose: Retrieves the number of labels in a database file
- Calls: Not inferable

## Globals
- None

## Dependencies
- TransDB (external type)
- CNoxstringDlg (external type)
- Uses char* for filename parameters
