# Generals/Code/Tools/Babylon/ViewDBsDlg.cpp

## Purpose
Implements a dialog for viewing translation databases (TransDB) in the Babylon tool.

## Responsibilities
- Displays full or changes-only views of translation databases
- Manages tree control population with progress feedback
- Handles dialog initialization and cleanup
- Integrates with main dialog (MainDLG) for status/progress reporting

## Key Types
- VIEWDBSII (Class): Main dialog class for viewing databases
- TransDB (External): Translation database structure

## Key Functions
### VIEWDBSII::create_full_view
- Purpose: Creates a tree view showing all translation databases
- Calls: FirstTransDB, TransDB::NumLabels, TransDB::NumObsolete, MainDLG->InitProgress, TransDB::AddToTree

### VIEWDBSII::create_changes_view
- Purpose: Creates a tree view showing only changed translation databases
- Calls: FirstTransDB, TransDB::IsChanged, TransDB::NumLabels, TransDB::NumObsolete, MainDLG->InitProgress, TransDB::AddToTree, MainDLG->ProgressComplete

### progress_cb
- Purpose: Callback for progress reporting during tree population
- Calls: MainDLG->SetProgress

## Globals
- ViewChanges (int): Flag to determine whether to show all DBs or only changes
- label_count (int): Counter for progress tracking

## Dependencies
- "stdafx.h", "noxstring.h", "noxstringdlg.h", "VIEWDBSII.h", "transdb.h"
- CDialog, CTreeCtrl (MFC), TransDB, MainDLG (external)
