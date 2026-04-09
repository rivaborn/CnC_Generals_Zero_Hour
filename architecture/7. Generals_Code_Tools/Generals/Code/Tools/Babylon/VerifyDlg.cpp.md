# Generals/Code/Tools/Babylon/VerifyDlg.cpp

## Purpose
Dialog class for verifying audio translations in the Babylon tool.

## Responsibilities
- Displays text and corresponding audio file for verification
- Provides playback controls (play/pause/stop)
- Handles user input for match/nomatch decisions
- Manages audio stream and timer for playback progress

## Key Types
- VerifyDlg (Class): Dialog for audio translation verification
- NoxText (Type): Text data structure
- LangID (Type): Language identifier
- Translation (Type): Translation data structure

## Key Functions
### VerifyDlg::OnInitDialog
- Purpose: Initializes dialog controls and loads audio file
- Calls: CDialog::OnInitDialog, GetWindowRect, MoveWindow, AutoLoad, GetDlgItem, SetWindowText, GetTranslation, PostMessage

### VerifyDlg::OnNomatch
- Purpose: Handles "no match" user input
- Calls: CloseAudio, EndDialog

### VerifyDlg::OnMatch
- Purpose: Handles "match" user input
- Calls: CloseAudio, CDialog::OnOK

### VerifyDlg::OnCancel
- Purpose: Handles dialog cancellation
- Calls: CloseAudio, CDialog::OnCancel

### VerifyDlg::CloseAudio
- Purpose: Cleans up audio resources
- Calls: None (commented out AIL calls)

### VerifyDlg::OnTimer
- Purpose: Updates playback progress slider
- Calls: CDialog::OnTimer

## Globals
- TIMERID (const int): Timer identifier for playback updates

## Dependencies
- stdafx.h, noxstring.h, VerifyDlg.h
- CDialog, CWnd, CStatic, CSliderCtrl (MFC)
- NoxText, LangID, Translation (Babylon tool types)
- AIL audio library functions (commented out)
