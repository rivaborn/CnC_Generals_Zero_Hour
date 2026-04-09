# Generals/Code/Tools/Babylon/Report.cpp

## Purpose
Implements a dialog for selecting languages and options for generating a report in the Babylon tool.

## Responsibilities
- Manages UI controls for language selection and report options
- Handles user input for report generation parameters
- Initializes and updates dialog state based on user selections
- Collects selected languages and options for report generation

## Key Types
- CReport (Class): Main dialog class for the report generation UI
- LANGINFO (Struct): Not inferable (used via GetLangInfo function)
- ReportOptions (Struct): Stores report generation settings (translations, dialog, limit)

## Key Functions
### CReport::OnInitDialog
- Purpose: Initializes the dialog controls and populates the language list
- Calls: GetDlgItem, GetLangInfo, CDialog::OnInitDialog

### CReport::OnOK
- Purpose: Handles the OK button click, collects user selections and prepares report generation
- Calls: GetSelItems, GetPathName, GetLangInfo, GetWindowText, atoi, CDialog::OnOK

### CReport::OnShowDetails
- Purpose: Toggles the visibility of advanced report options
- Calls: GetCheck, EnableWindow

### CReport::OnSelectall
- Purpose: Selects all languages in the list
- Calls: SelItemRange

### CReport::OnInvert
- Purpose: Inverts the selection state of all languages
- Calls: GetSel, SetSel

## Globals
- CurrentLanguage (int): The current language ID
- options (ReportOptions): Stores report generation settings
- langids (int[16]): Array to store selected language IDs
- filename (char[256]): Stores the output filename
- num_langs (int): Number of languages in the list

## Dependencies
- MFC classes: CDialog, CWnd, CButton, CListBox, CStatic, CEdit, CFileDialog
- External functions: GetLangInfo, AfxMessageBox
- Windows API: SelItemRange, SetSel, GetSel, EnableWindow, SetCheck, GetCheck
- Standard C: strcpy, atoi
