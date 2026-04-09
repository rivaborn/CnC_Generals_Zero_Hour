# GeneralsMD/Code/GameEngine/Source/GameClient/Input/Mouse.cpp

## Purpose
Handles mouse input, cursor rendering, and tooltips in the SAGE engine.

## Responsibilities
- Processes mouse events (position, clicks, wheel)
- Manages cursor appearance and behavior
- Displays tooltips with configurable appearance
- Handles mouse dragging and click detection
- Parses mouse-related INI configurations

## Key Types
- `Mouse` (Class): Main mouse input handler
- `CursorInfo` (Struct): Stores cursor visual properties
- `MouseIO` (Struct): Raw mouse input data
- `MouseState` (Struct): Current mouse state
- `RedrawMode` (Enum): Cursor rendering modes

## Key Functions
### `moveMouse`
- Purpose: Updates mouse position (relative or absolute)
- Calls: None

### `updateMouseData`
- Purpose: Retrieves raw mouse events from DirectX
- Calls: `getMouseEvent`

### `processMouseEvent`
- Purpose: Converts raw events into game state
- Calls: `moveMouse`, `checkForDrag`

### `drawTooltip`
- Purpose: Renders mouse tooltip with animation
- Calls: `TheDisplay->drawFillRect`, `TheDisplay->drawOpenRect`

### `setCursorTooltip`
- Purpose: Configures tooltip text and appearance
- Calls: `m_tooltipDisplayString->setWordWrap`, `m_tooltipDisplayString->setText`

## Globals
- `TheMouse` (Mouse*): Singleton mouse instance
- `TheMouseCursorFieldParseTable` (FieldParse[]): INI parsing rules for cursors
- `TheMouseFieldParseTable` (FieldParse[]): INI parsing rules for mouse settings

## Dependencies
- `Display.h`, `GameClient.h`, `Keyboard.h`, `INI.h`
- `TheDisplay`, `TheGameClient`, `TheGameText`, `TheScriptEngine`
- DirectX mouse input functions (not shown in header)
