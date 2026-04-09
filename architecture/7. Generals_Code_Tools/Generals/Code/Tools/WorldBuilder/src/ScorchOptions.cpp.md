# Generals/Code/Tools/WorldBuilder/src/ScorchOptions.cpp

## Purpose
Handles the UI and logic for configuring scorch mark properties in WorldBuilder.

## Responsibilities
- Manages scorch mark type and size selection
- Updates UI based on selected scorch marks
- Applies changes to selected scorch marks via undoable operations
- Handles slider and combo box interactions

## Key Types
- ScorchOptions (Class): Dialog for scorch mark configuration
- Scorches (Enum): Scorch mark types (SCORCH_1, etc.)
- MapObject: Game object with scorch properties

## Key Functions
### ScorchOptions::updateTheUI
- Purpose: Refreshes UI controls with current scorch properties
- Calls: getSingleSelectedScorch, getProperties, getInt, getReal

### ScorchOptions::changeScorch
- Purpose: Updates scorch type for selected marks
- Calls: getAllSelectedDicts, DictItemUndoable constructor, AddAndDoUndoable, Invalidate

### ScorchOptions::changeSize
- Purpose: Updates scorch size for selected marks
- Calls: getAllSelectedDicts, DictItemUndoable constructor, AddAndDoUndoable, Invalidate

### ScorchOptions::GetPopSliderInfo
- Purpose: Provides slider configuration for size control
- Calls: None

## Globals
- m_scorchtype (Scorches): Current scorch type selection
- m_scorchsize (Real): Current scorch size value
- m_staticThis (ScorchOptions*): Singleton reference to dialog instance

## Dependencies
- CUndoable.h, WbView3d.h, Common/WellKnownKeys.h, WorldBuilderDoc.h
- CDialog, CComboBox, CWnd (MFC)
- MapObject, Dict, DictItemUndoable, CWorldBuilderDoc, WbView3d
