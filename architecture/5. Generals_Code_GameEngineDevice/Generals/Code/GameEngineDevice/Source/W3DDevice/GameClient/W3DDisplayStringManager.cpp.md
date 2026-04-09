# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DDisplayStringManager.cpp

## Purpose
Manages display strings for the W3D rendering system, including creation, cleanup, and resource management.

## Responsibilities
- Creates and manages `DisplayString` objects
- Handles font assignment and text localization
- Implements resource cleanup for unused strings
- Provides group numeral and formation label strings

## Key Types
- `W3DDisplayStringManager` (Class): Manages display strings and their resources
- `W3DDisplayString` (Class): Individual display string implementation (external)
- `DisplayString` (Class): Base display string interface (external)

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
- Purpose: Retrieves pre-created numeral display strings
- Calls: None

## Globals
- `TheFontLibrary` (External): Font management system
- `TheDrawGroupInfo` (External): Drawing configuration
- `TheGameText` (External): Text localization
- `TheGlobalLanguageData` (External): Language settings
- `TheGameClient` (External): Game client interface

## Dependencies
- `Common/Debug.h`
- `GameClient/GameClient.h`
- `GameClient/GameText.h`
- `GameClient/DisplayString.h`
- `GameClient/DrawGroupInfo.h`
- `GameClient/GlobalLanguage.h`
- `W3DDevice/GameClient/W3DDisplayStringManager.h`
