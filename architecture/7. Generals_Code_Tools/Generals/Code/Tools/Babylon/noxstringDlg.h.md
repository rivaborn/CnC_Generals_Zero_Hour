# Generals/Code/Tools/Babylon/noxstringDlg.h

## Purpose
Header file for the CNoxstringDlg class, a dialog-based tool for managing string translations in the game.

## Responsibilities
- Manages string translation database operations
- Provides UI for translation verification and updates
- Handles progress tracking and status reporting
- Supports drag-and-drop file operations

## Key Types
- LogFormat (Enum): Defines logging output formats (same line/new line)
- UPDATEINFO (Struct): Tracks statistics about string/label updates
- CNoxstringDlg (Class): Main dialog class for the translation tool

## Key Functions
### ValidateStrFile
- Purpose: Validates a string file
- Calls: Not inferable

### UpdateLabel
- Purpose: Updates a label in the translation database
- Calls: Not inferable

### UpdateDB
- Purpose: Updates the entire translation database
- Calls: UpdateLabel

### Status
- Purpose: Displays status messages in the UI
- Calls: Not inferable

### Log
- Purpose: Logs messages with specified formatting
- Calls: Not inferable

## Globals
- MainDLG (CNoxstringDlg*): Global pointer to the main dialog instance

## Dependencies
- "resource.h", "transdb.h"
- CDialog, CProgressCtrl, CStatic, CComboBox (MFC classes)
- TransDB, LangID, NoxText, NoxLabel (translation database types)
