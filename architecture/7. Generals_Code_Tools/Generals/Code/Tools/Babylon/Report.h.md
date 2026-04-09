# Generals/Code/Tools/Babylon/Report.h

## Purpose
Header file for the CReport dialog class, used in the Babylon tool for generating localization reports.

## Responsibilities
- Manages UI elements for report generation dialog
- Handles user input for report options and language selection
- Provides accessors for report filename, options, and language IDs
- Implements dialog initialization and message handlers

## Key Types
- CReport (Class): Dialog class for report generation UI
- (anonymous enum) (Enum): Contains IDD constant for dialog resource ID
- IDD (Enum): Dialog resource identifier

## Key Functions
### CReport::DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: Not inferable

### CReport::OnInitDialog
- Purpose: Initializes dialog controls and state
- Calls: Not inferable

### CReport::OnInvert
- Purpose: Handles invert selection command
- Calls: Not inferable

### CReport::OnSelectall
- Purpose: Handles select all command
- Calls: Not inferable

### CReport::OnShowDetails
- Purpose: Handles show details toggle
- Calls: Not inferable

### CReport::OnOK
- Purpose: Handles dialog OK button click
- Calls: Not inferable

### CReport::OnCancel
- Purpose: Handles dialog cancel button click
- Calls: Not inferable

## Globals
- None

## Dependencies
- "expimp.h" (include)
- CDialog, CWnd, CListBox, CEdit, CButton, CStatic (MFC classes)
- RPOPTIONS, LangID (external types)
- CDataExchange, afx_msg (MFC macros/functions)
