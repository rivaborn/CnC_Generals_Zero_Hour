# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DDisplayStringManager.cpp

## Purpose
Manages display strings for the W3D rendering system, including group numerals and formation labels.

## Responsibilities
- Creates and manages `DisplayString` objects
- Handles font assignment and text localization
- Implements resource cleanup for unused strings
- Provides group numeral strings for UI elements

## Key Types
- `W3DDisplayStringManager` (Class): Manages display strings and their lifecycle
- `W3DDisplayString` (Class): Individual text rendering object (defined elsewhere)
- `DisplayString` (Class): Base text display interface

## Key Functions
### `newDisplayString`
- Purpose: Creates a new display string with default font
- Calls: `newInstance`, `TheFontLibrary->getFont`, `link`

### `freeDisplayString`
- Purpose: Releases a display string and its resources
- Calls: `unLink`, `deleteInstance`

### `update`
- Purpose: Cleans up rendering resources for unused strings
- Calls: `DisplayStringManager::update`, `m_textRenderer.Reset`

### `getGroupNumeralString`
- Purpose: Retrieves a pre-configured group numeral string
- Calls: None

## Globals
- `m_groupNumeralStrings[MAX_GROUPS]` (DisplayString*): Pre-created group number displays
- `m_formationLetterDisplayString` (DisplayString*): Formation label display
- `m_currentCheckpoint` (DisplayString*): Optimization for update loop

## Dependencies
- `DisplayStringManager` (base class)
- `TheGameText`, `TheDrawGroupInfo`, `TheGlobalLanguageData`, `TheFontLibrary`, `TheGameClient` (globals)
- `GameFont`, `UnicodeString`, `AsciiString` (types)
