# Generals/Code/Tools/WorldBuilder/src/TeamBehavior.cpp

## Purpose
Handles the UI and logic for team behavior configuration in WorldBuilder, including script assignments and behavioral flags.

## Responsibilities
- Manages team behavior property page UI
- Handles script assignments for team events
- Updates team behavior settings in the team dictionary
- Enforces mutual exclusivity for certain defense modes

## Key Types
- **TeamBehavior (class)**: MFC property page for team behavior configuration
- **NameKeyType (type)**: Key for dictionary entries (from WellKnownKeys.h)

## Key Functions
### `updateScript`
- Purpose: Updates the team dictionary with the selected script for a given key
- Calls: `m_teamDict->setAsciiString`

### `setupScript`
- Purpose: Populates a combo box with available scripts and selects the current one
- Calls: `EditParameter::loadScripts`, `m_teamDict->getAsciiString`

### `OnInitDialog`
- Purpose: Initializes the dialog controls with current team settings
- Calls: `setupScript`, `m_teamDict->getBool`, `m_teamDict->getReal`, `m_teamDict->getInt`

### `OnPerimeterDefense` / `OnBaseDefense`
- Purpose: Handles defense mode checkbox changes and enforces mutual exclusivity
- Calls: `m_teamDict->setBool`

### `OnChangePercentDestroyed`
- Purpose: Updates the destroyed threshold percentage in the team dictionary
- Calls: `m_teamDict->setReal`

## Globals
- **NONE_STRING (const)**: String constant for "None" option
- **AI_SLEEP (const)**: Base value for aggressiveness levels

## Dependencies
- `stdafx.h`, `worldbuilder.h`, `TeamBehavior.h`, `EditParameter.h`, `WellKnownKeys.h`, `GameLogic/AI.h`
- MFC classes: `CPropertyPage`, `CComboBox`, `CButton`, `CDataExchange`
- External symbols: `TheKey_*` constants, `AsciiString`, `NameKeyType`
