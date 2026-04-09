# Generals/Code/Tools/Babylon/expimp.cpp

## Purpose
Handles export/import of game translations and localization data for Command & Conquer Generals.

## Responsibilities
- Export translations to spreadsheet format
- Import translations from spreadsheet format
- Generate game string files (.str, .csf)
- Process wave files for localization
- Generate translation reports

## Key Types
- **NoxLabel**: Label metadata for localization strings
- **NoxText**: Localization string text data
- **Translation**: Translated string data
- **TransDB**: Translation database
- **TROPTIONS**: Translation export/import options
- **RPOPTIONS**: Report generation options

## Key Functions
### export_trans
- Purpose: Exports translations to spreadsheet format
- Calls: writeLabel, writeText, EncodeFormat, PutCell

### import_trans
- Purpose: Imports translations from spreadsheet format
- Calls: GetString, PutCell, EncodeFormat

### generate_noxstr
- Purpose: Generates .str format game string files
- Calls: writeCSFLabel, writeCSFString

### generate_csf
- Purpose: Generates .csf format game string files
- Calls: writeCSFLabel, writeCSFString

### ProcessWaves
- Purpose: Processes wave files for localization
- Calls: OpenWorkBook, GetString, fclose

### GenerateReport
- Purpose: Generates translation status reports
- Calls: fopen, fprintf, db->ReportTranslations, db->ReportDialog

### UpdateSentTranslations
- Purpose: Updates sent translation status
- Calls: OpenWorkBook, GetString, update_sent_trans

## Globals
- **buffer** (char[100*1024]): Temporary buffer for string operations
- **olebuf** (OLECHAR[100*1024]): Unicode buffer for string operations
- **progress_dlg** (CNoxstringDlg*): Progress dialog pointer
- **progress_count** (int): Progress counter
- **cb_file** (FILE*): File handle for report generation

## Dependencies
- "transDB.h", "XLStuff.h", "Noxstringdlg.h", "VerifyTextDlg.h", "Noxstring.h", "expimp.h", "direct.h", "fileops.h", "olestring.h"
- CNoxstringDlg, NoxLabel, NoxText, Translation, TransDB classes
- GetLangInfo, GetLangName, EncodeFormat, PutCell, OpenWorkBook, GetString functions
