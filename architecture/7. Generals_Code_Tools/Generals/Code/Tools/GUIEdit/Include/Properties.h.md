# Generals/Code/Tools/GUIEdit/Include/Properties.h

## Purpose
Header for property dialog management in the GUIEdit tool, defining types and functions for editing game window and control properties.

## Responsibilities
- Defines UI state identifiers and color/image info structures
- Declares property dialog initialization functions for various controls
- Provides utility functions for dialog message handling and property management

## Key Types
- ColorControl (struct): Associates control IDs with colors
- StateIdentifier (enum): Enumerates all UI control states (buttons, sliders, etc.)
- ImageAndColorInfo (struct): Stores image/color data for UI states

## Key Functions
### InitPropertiesDialog
- Purpose: Initialize main properties dialog
- Calls: Not inferable

### HandleCommonDialogMessages
- Purpose: Process common dialog messages
- Calls: Not inferable

### SaveCommonDialogProperties
- Purpose: Save dialog properties to a window
- Calls: Not inferable

### GetStateInfo
- Purpose: Retrieve state information by identifier
- Calls: Not inferable

## Globals
- None

## Dependencies
- "GameClient/GameWindow.h"
- "GUIEditColor.h"
- Uses Win32 API types (HWND, UINT, WPARAM, LPARAM)
- References Image, Color, GameFont, AsciiString types
