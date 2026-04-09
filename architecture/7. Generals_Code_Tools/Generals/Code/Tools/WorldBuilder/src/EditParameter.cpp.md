# Generals/Code/Tools/WorldBuilder/src/EditParameter.cpp

## Purpose
Handles editing of game parameters in the WorldBuilder tool, providing UI for various parameter types.

## Responsibilities
- Manages parameter editing dialogs for different data types
- Validates parameter values and provides warnings
- Handles preview functionality for audio parameters
- Loads and displays available options for combo boxes/lists

## Key Types
- **EditParameter (Class)**: Main dialog class for parameter editing
- **Parameter (Class)**: Represents game parameters being edited
- **AsciiString (Type)**: String type used throughout

## Key Functions
### `edit`
- Purpose: Dispatches parameter editing to appropriate dialog based on type
- Calls: `EditCoordParameter::DoModal`, `EditObjectParameter::DoModal`, `CColorDialog::DoModal`

### `getWarningText`
- Purpose: Validates parameter values and generates warning messages
- Calls: `loadScripts`, `loadAttackPrioritySets`, `loadWaypoints`, etc.

### `getInfoText`
- Purpose: Populates UI controls with appropriate options for the parameter type
- Calls: `loadMovies`, `loadSpecialPowers`, `loadSciences`, etc.

### `OnPreviewSound`
- Purpose: Plays preview of audio parameters
- Calls: `PlaySound` (Windows API)

## Globals
- **m_selectedLocalizedString (AsciiString)**: Stores currently selected localized string
- **m_unitName (AsciiString)**: Stores name of unit being edited
- **m_sidesListP (SidesList*)**: Pointer to sides list

## Dependencies
- Key includes: `EditParameter.h`, `EditCoordParameter.h`, `EditObjectParameter.h`, various game logic headers
- External symbols: `TheGameText`, `TheAudio`, `TheTerrainRenderObject`, `ThePlayerTemplateStore`
