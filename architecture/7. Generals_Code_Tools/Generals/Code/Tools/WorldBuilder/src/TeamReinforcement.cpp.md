# Generals/Code/Tools/WorldBuilder/src/TeamReinforcement.cpp

## Purpose
Handles the UI and logic for team reinforcement settings in WorldBuilder.

## Responsibilities
- Manages team reinforcement dialog UI
- Handles user input for reinforcement parameters
- Updates team reinforcement data in the team dictionary
- Loads and displays available transports and waypoints

## Key Types
- TeamReinforcement (Class): Dialog for team reinforcement settings
- CPropertyPage (Class): Base MFC property page class
- CComboBox (Class): MFC combo box control
- CButton (Class): MFC button control

## Key Functions
### OnInitDialog
- Purpose: Initializes the dialog controls with current team reinforcement settings
- Calls: CPropertyPage::OnInitDialog, EditParameter::loadTransports, EditParameter::loadWaypoints

### OnDeployBy
- Purpose: Toggles transport deployment options
- Calls: GetDlgItem, CComboBox::SetCurSel, CComboBox::EnableWindow, CButton::EnableWindow

### OnTeamStartsFull
- Purpose: Updates team starts full setting
- Calls: GetDlgItem, CButton::GetCheck, m_teamDict->setBool

### OnSelchangeTransportCombo
- Purpose: Handles transport selection changes
- Calls: GetDlgItem, CComboBox::GetCurSel, CComboBox::GetLBText, m_teamDict->setAsciiString

### OnTransportsExit
- Purpose: Updates transports exit setting
- Calls: GetDlgItem, CButton::GetCheck, m_teamDict->setBool

### OnSelchangeVeterancy
- Purpose: Handles veterancy level selection changes
- Calls: GetDlgItem, CComboBox::GetCurSel, m_teamDict->setInt

### OnSelchangeWaypointCombo
- Purpose: Handles waypoint
