# Generals/Code/Tools/WorldBuilder/include/MapSettings.h

## Purpose
Header file for the MapSettings dialog class in WorldBuilder, used to configure map properties.

## Responsibilities
- Defines the MapSettings dialog class
- Declares data exchange and message handlers for map settings
- Manages UI events for map properties (title, time of day, weather, compression)

## Key Types
- MapSettings (Class): Dialog for editing map settings
- (anonymous enum) (Enum): Contains IDD enum value
- IDD (Enum): Dialog resource identifier

## Key Functions
### MapSettings::DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: Not inferable

### MapSettings::OnChangeMapTimeofday
- Purpose: Handles changes to map time of day setting
- Calls: Not inferable

### MapSettings::OnChangeMapWeather
- Purpose: Handles changes to map weather setting
- Calls: Not inferable

### MapSettings::OnInitDialog
- Purpose: Initializes the dialog
- Calls: Not inferable

### MapSettings::OnOK
- Purpose: Handles dialog OK button click
- Calls: Not inferable

### MapSettings::OnChangeMapTitle
- Purpose: Handles changes to map title
- Calls: Not inferable

### MapSettings::OnChangeMapCompression
- Purpose: Handles changes to map compression setting
- Calls: Not inferable

## Globals
None

## Dependencies
- CDialog (MFC class)
- CDataExchange (MFC class)
- CWnd (MFC class)
- AFX data exchange macros (DDX/DDV)
- MFC message map macros (DECLARE_MESSAGE_MAP, afx_msg)
