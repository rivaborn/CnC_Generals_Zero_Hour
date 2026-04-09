# Generals/Code/Tools/Babylon/GenerateDlg.cpp

## Purpose
Implements a dialog for configuring string generation options in the Babylon tool.

## Responsibilities
- Manages UI controls for string generation settings
- Handles user input for format, language selection, and output options
- Updates preview of output filename based on selections
- Collects selected options for string generation

## Key Types
- CGenerateDlg (Class): Main dialog class for string generation options
- GNOPTIONS (Struct): Contains format and untranslated options
- LANGINFO (Struct): Language information (external)

## Key Functions
### OnInitDialog
- Purpose: Initializes dialog controls and populates language list
- Calls: GetDlgItem, GetLangInfo

### OnChangePrefix
- Purpose: Updates filename preview based on current settings
- Calls: GetWindowText, SetWindowText

### OnOK
- Purpose: Validates selections and prepares data for string generation
- Calls: GetWindowText, GetSelItems, GetLangInfo

### OnUnicode/OnNoxstr/OnIds/OnOriginal
- Purpose: Updates generation options based on UI selections
- Calls: OnChangePrefix (for format changes)

## Globals
- options (GNOPTIONS): Stores current generation settings
- langids (int[16]): Array for selected language IDs
- filename (char[256]): Buffer for output filename
- CurrentLanguage (int): Current language ID (external)
- num_langs (int): Number of available languages

## Dependencies
- MFC classes (CDialog, CEdit, CButton, etc.)
- noxstring.h (GNOPTIONS, LANGINFO)
- direct.h (GetLangInfo)
- stdafx.h (precompiled headers)
