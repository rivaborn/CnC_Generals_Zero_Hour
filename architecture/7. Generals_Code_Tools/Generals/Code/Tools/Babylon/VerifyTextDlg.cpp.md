# Generals/Code/Tools/Babylon/VerifyTextDlg.cpp

## Purpose
Implements a dialog for comparing translated and original text strings in the Babylon tool.

## Responsibilities
- Displays two text strings (translated and original) for user verification.
- Handles user input for match/no-match decisions.
- Manages dialog initialization and control updates.

## Key Types
- CVerifyTextDlg (Class): Dialog class for text verification.

## Key Functions
### CVerifyTextDlg::CVerifyTextDlg
- Purpose: Constructor initializing dialog with translation and original strings.
- Calls: CDialog constructor.

### CVerifyTextDlg::OnNomatch
- Purpose: Handles "No Match" button click, ending dialog with IDNO.
- Calls: EndDialog.

### CVerifyTextDlg::OnMatch
- Purpose: Handles "Match" button click, ending dialog with IDYES.
- Calls: EndDialog.

### CVerifyTextDlg::OnInitDialog
- Purpose: Initializes dialog controls with provided text strings.
- Calls: CDialog::OnInitDialog, SetDlgItemText.

## Globals
- THIS_FILE (char[]): Debug file identifier.

## Dependencies
- stdafx.h, noxstring.h, VerifyTextDlg.h
- CDialog, CWnd, CDataExchange (MFC classes)
- IDD, IDC_TRANS, IDC_ORIG, IDC_NOMATCH, IDC_MATCH (resource IDs)
