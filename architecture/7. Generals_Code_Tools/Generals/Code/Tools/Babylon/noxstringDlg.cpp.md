# Generals/Code/Tools/Babylon/noxstringDlg.cpp

## Purpose
Implements the main dialog for the Noxstring tool, which manages localization strings and dialogs in Command & Conquer Generals.

## Responsibilities
- Manages UI for localization operations
- Handles string verification and translation checks
- Provides progress reporting and error logging
- Coordinates with backend database operations

## Key Types
- INFO (Struct): Stores localization metadata (comment, context, speaker, listener, wave)
- CAboutDlg (Class): About dialog implementation
- CNoxstringDlg (Class): Main application dialog class

## Key Functions
### print_to_log
- Purpose: Logs error messages to the UI
- Calls: mainDlg->Log()

### print_to_log_and_update_progress
- Purpose: Logs messages and updates progress bar
- Calls: print_to_log(), mainDlg->SetProgress()

### readToEndOfQuote
- Purpose: Parses quoted strings from input
- Calls: Not inferable (truncated)

### getString
- Purpose: Extracts string content between quotes
- Calls: Not inferable (truncated)

### getToken
- Purpose: Tokenizes input based on delimiters
- Calls: Not inferable (truncated)

### parseComment
- Purpose: Processes comment blocks in localization files
- Calls: Not inferable (truncated)

## Globals
- buffer (char[100*1024]): Temporary string buffer
- buffer2 (char[100*1024]): Secondary string buffer
- buffer3 (char[100*1024]): Tertiary string buffer
- INCREMENTS (const int): Progress increment value
- MAX_INFO_LEN (const int): Maximum length for INFO fields
- found_error (int): Error flag
- cb_count (int): Callback counter
- mainDlg (CNoxstringDlg*): Pointer to main dialog instance
- global_info (INFO): Global localization metadata
- local_info (INFO): Local localization metadata

## Dependencies
- MFC framework classes (CDialog, CWnd, etc.)
- Localization database classes (TransDB, NoxLabel)
- File operations utilities
- Progress reporting mechanisms
- String parsing and validation routines
