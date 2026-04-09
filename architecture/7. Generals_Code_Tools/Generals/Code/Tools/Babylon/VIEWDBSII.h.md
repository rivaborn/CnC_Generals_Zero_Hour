# Generals/Code/Tools/Babylon/VIEWDBSII.h

## Purpose
Header file for the VIEWDBSII dialog class, part of the Babylon tool suite for viewing database changes.

## Responsibilities
- Defines the VIEWDBSII dialog class for database viewing
- Declares methods for creating change and full views
- Manages dialog initialization and data exchange
- Provides tree view functionality for database contents

## Key Types
- VIEWDBSII (Class): Dialog class for viewing database changes and full database contents
- (anonymous enum) (Enum): Contains IDD enum value
- IDD (Enum): Dialog resource identifier

## Key Functions
### VIEWDBSII()
- Purpose: Constructor for VIEWDBSII dialog class
- Calls: None

### OnClose()
- Purpose: Handles dialog close event
- Calls: None

### OnInitDialog()
- Purpose: Initializes the dialog
- Calls: None

### create_changes_view()
- Purpose: Creates a tree view showing database changes
- Calls: None

### create_full_view()
- Purpose: Creates a tree view showing the full database
- Calls: None

### DoDataExchange()
- Purpose: Handles data exchange between dialog controls and member variables
- Calls: None

## Globals
- ViewChanges (int): Flag indicating whether to show changes view

## Dependencies
- CDialog (MFC class)
- CWnd (MFC class)
- CDataExchange (MFC class)
- HTREEITEM (MFC tree control item type)
- IDD_VIEWDBS (resource ID)
