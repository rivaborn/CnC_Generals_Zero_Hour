# Generals/Code/GameEngine/Source/GameClient/Input/Mouse.cpp

## Purpose
Handles mouse input, cursor rendering, and tooltip display in the game client.

## Responsibilities
- Processes mouse events (position, clicks, wheel)
- Manages cursor appearance and behavior
- Displays tooltips and cursor text
- Handles mouse dragging and click detection
- Configures mouse limits and movement modes

## Key Types
- `Mouse` (Class): Main mouse input handler
- `CursorInfo` (Struct): Stores cursor appearance data
- `MouseIO` (Struct): Raw mouse input event data
- `MouseState` (Struct): Current mouse state snapshot

## Key Functions
### `moveMouse`
- Purpose: Updates mouse position in relative or absolute coordinates
- Calls: None

### `updateMouseData`
- Purpose: Retrieves latest mouse events from DirectX
- Calls: `getMouseEvent`

### `processMouseEvent`
- Purpose: Combines mouse events into main mouse variables
- Calls: `moveMouse`, `checkForDrag`

### `drawTooltip`
- Purpose: Renders mouse tooltip if one is set
- Calls: `TheDisplay->drawFillRect`, `TheDisplay->drawOpenRect`

### `setCursorTooltip`
- Purpose: Sets the text and appearance of the mouse tooltip
- Calls: `m_tooltipDisplayString->setWordWrap`, `m_tooltipDisplayString->setText`

## Globals
- `TheMouse` (Mouse*): Global mouse instance
- `TheMouseCursorFieldParseTable` (FieldParse[]): INI parsing table for cursor data
- `TheMouseFieldParseTable` (FieldParse[]): INI parsing table for mouse settings

## Dependencies
- `Common/Debug.h`, `Common/MessageStream.h`, `Common/GameEngine.h`
- `GameClient/Display.h`, `GameClient/GameClient.h`, `GameClient/Mouse.h`
- `INI::parseAsciiString`, `INI::parseRGBAColorInt`, `INI::parseReal`
- `TheDisplay`, `TheGameClient`, `TheGameText`, `TheScriptEngine`
