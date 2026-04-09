# Generals/Code/Tools/Babylon/RetranslateDlg.cpp

## Purpose
Implements a dialog for handling string retranslation decisions in the Babylon tool.

## Responsibilities
- Displays old and new text strings for comparison
- Handles user choices (retranslate, skip, no retranslate, skip all)
- Updates string objects based on user input

## Key Types
- RetranslateDlg (class): Dialog for retranslation decisions

## Key Functions
### RetranslateDlg::OnInitDialog
- Purpose: Initializes the dialog with old and new text strings
- Calls: CDialog::OnInitDialog, GetDlgItem, SetWindowText

### RetranslateDlg::OnRetranslate
- Purpose: Marks string for retranslation and closes dialog
- Calls: SetRetranslate, CDialog::OnOK

### RetranslateDlg::OnSkip
- Purpose: Skips current string and continues
- Calls: EndDialog

### RetranslateDlg::OnNoRetranslate
- Purpose: Marks string as not to be retranslated and closes dialog
- Calls: SetRetranslate, CDialog::OnOK

### RetranslateDlg::OnSkipAll
- Purpose: Skips all remaining strings and closes dialog
- Calls: CDialog::OnCancel

## Globals
- newtext (Not inferable): New string object
- oldtext (Not inferable): Old string object

## Dependencies
- stdafx.h, noxstring.h, RetranslateDlg.h
- MFC classes: CDialog, CStatic, CDataExchange
- Message map macros: BEGIN_MESSAGE_MAP, ON_WM_CANCELMODE, ON_BN_CLICKED
