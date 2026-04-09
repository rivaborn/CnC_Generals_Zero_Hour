# Generals/Code/Tools/Babylon/loadsave.cpp

## Purpose
Handles serialization and deserialization of localization data (text, translations, labels) using IFF file format.

## Responsibilities
- Write localization database to file (WriteMainDB)
- Load localization database from file (LoadMainDB)
- Count labels in database file (GetLabelCountDB)
- Serialize/deserialize text, translations, and labels with metadata

## Key Types
- DBINFO (struct): Database header info (label count, next ID)
- LBINFO (struct): Label metadata (max length)
- TXINFO (struct): Text entry info (ID, revision)
- TRINFO (struct): Translation info (language, revision)
- WVINFO (struct): Wave info (valid flag, lo/hi values)

## Key Functions
### writeString
- Purpose: Write a Unicode string to IFF chunk
- Calls: IFF_NEWCHUNK, IFF_WRITE, IFF_CloseChunk

### writeTransForm
- Purpose: Serialize a Translation object to IFF
- Calls: IFF_NewForm, IFF_NewChunk, IFF_Write, IFF_CloseChunk, IFF_CloseForm, writeString

### writeTextForm
- Purpose: Serialize a NoxText object to IFF
- Calls: IFF_NewForm, IFF_NewChunk, IFF_Write, IFF_CloseChunk, IFF_CloseForm, writeString

### WriteMainDB
- Purpose: Write entire TransDB to file with progress reporting
- Calls: IFF_New, IFF_NewForm, IFF_NewChunk, IFF_Write, IFF_CloseChunk, IFF_CloseForm, writeTextForm, writeTransForm

### LoadMainDB
- Purpose: Load TransDB from file with callback support
- Calls: IFF_Load, IFF_NextForm, IFF_NextChunk, IFF_READ, new NoxLabel/NoxText/Translation, IFF_Close, readString

### GetLabelCountDB
- Purpose: Count labels in database file without full load
- Calls: IFF_Open, IFF_NextForm, IFF_NextChunk, IFF_READ, IFF_Close

## Globals
- buffer (OLECHAR[MAX_BUFFER]): Temporary buffer for string operations

## Dependencies
- IFF file I/O functions (IFF_New, IFF_Load, etc.)
- TransDB class (localization database)
- NoxText, NoxLabel, Translation classes
- CNoxstringDlg (progress dialog)
- noxstringdlg.h, iff.h, TransDB.h headers
