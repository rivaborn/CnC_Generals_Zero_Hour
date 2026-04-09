# Generals/Code/Tools/Babylon/TransDB.cpp

## Purpose
Manages translation databases for localization in Command & Conquer Generals.

## Responsibilities
- Stores and retrieves localized text strings
- Manages labels and text entries
- Validates translations and reports errors
- Handles duplicate text detection
- Tracks dialog audio file validity

## Key Types
- **TransDB (Class)**: Main translation database container
- **NoxLabel (Class)**: Label container for text entries
- **NoxText (Class)**: Individual text entry
- **LANGINFO (Struct)**: Language identifier information
- **Bin/BinID (Classes)**: Binary storage for text entries

## Key Functions
### TransDB::FindText
- Purpose: Retrieves text entry by ID or string
- Calls: text_bin->Get, text_id_bin->Get

### TransDB::Errors
- Purpose: Validates database and reports errors
- Calls: label_bin->Clear, tbin->Get, dlg->Log

### TransDB::ReportTranslations
- Purpose: Generates translation status report
- Calls: text->GetTranslation, trans->ValidateFormat

### GetLangInfo
- Purpose: Retrieves language info by index or ID
- Calls: None

## Globals
- **buffer (char[100*1024])**: Temporary string buffer
- **DataBases (List)**: Global list of translation databases
- **langinfo (LANGINFO[])**: Array of supported languages

## Dependencies
- "transdb.h", "noxstringdlg.h", "noxstring.h", "bin.h", "list.h"
- Uses List, Bin, NoxLabel, NoxText classes
- Depends on OLECHAR for string handling
