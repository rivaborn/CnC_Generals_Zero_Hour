# Generals/Code/Tools/WorldBuilder/src/CFixTeamOwnerDialog.cpp

## Purpose
Handles a dialog for selecting a new team owner in the WorldBuilder tool.

## Responsibilities
- Displays a list of available sides/teams
- Allows user to select a new owner for a team
- Updates the selected owner when confirmed

## Key Types
- CFixTeamOwnerDialog (Class): Dialog for team owner selection
- TeamsInfo (Type): Not inferable
- SidesList (Type): Not inferable
- SidesInfo (Type): Not inferable

## Key Functions
### CFixTeamOwnerDialog::CFixTeamOwnerDialog
- Purpose: Constructor initializes dialog with team and sides info
- Calls: None

### CFixTeamOwnerDialog::getSelectedOwner
- Purpose: Returns the selected owner's name
- Calls: None

### CFixTeamOwnerDialog::OnInitDialog
- Purpose: Initializes the dialog with team name and populates the list of sides
- Calls: m_ti->getDict()->getAsciiString, m_sl->getNumSides, m_sl->getSideInfo, si->getDict()->getAsciiString

### CFixTeamOwnerDialog::OnOK
- Purpose: Handles OK button press, sets the selected owner
- Calls: CDialog::OnOK, GetDlgItem, pList->GetCurSel, m_sl->getSideInfo, si->getDict()->getAsciiString

## Globals
- NEUTRAL_NAME_STR (const char*): String literal for neutral team display

## Dependencies
- StdAfx.h, Resource.h, CFixTeamOwnerDialog.h, SidesList.h, WellknownKeys.h
- CDialog, CListBox, CWnd, CString, AsciiString, Bool, Int, TheKey_teamName, The
