# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarResizer.cpp

## Purpose
Manages dynamic resizing of control bar windows based on screen resolution.

## Responsibilities
- Loads and parses control bar resizing configurations from INI files
- Maintains a list of resizable windows with default and alternative positions/sizes
- Applies appropriate window dimensions based on current display resolution
- Handles window creation and cleanup

## Key Types
- `ResizerWindow` (struct): Stores default and alternative positions/sizes for a window
- `ControlBarResizer` (class): Main class managing window resizing functionality
- `ResizerWindowList` (type): Container for tracking resizable windows

## Key Functions
### `ControlBarResizer::init()`
- Purpose: Loads resizing configuration from INI file
- Calls: `INI::load()`

### `ControlBarResizer::sizeWindowsDefault()`
- Purpose: Restores windows to their default positions and sizes
- Calls: `GameWindow::winSetPosition()`, `GameWindow::winSetSize()`

### `ControlBarResizer::sizeWindowsAlt()`
- Purpose: Applies alternative positions/sizes scaled to current resolution
- Calls: `GameWindow::winSetPosition()`, `GameWindow::winSetSize()`

### `INI::parseControlBarResizerDefinition()`
- Purpose: Parses INI configuration for control bar resizing
- Calls: `ControlBarResizer::findResizerWindow()`, `ControlBarResizer::newResizerWindow()`

## Globals
- `ControlBarResizer::m_controlBarResizerParseTable` (FieldParse[]): INI parsing table for resizer configuration

## Dependencies
- `GameClient/ControlBar.h`
- `GameClient/ControlBarResizer.h`
- `GameClient/GameWindow.h`
- `GameClient/GameWindowManager.h`
- `GameClient/Display.h`
- `INI` class for configuration parsing
- `GameWindow` class for window manipulation
- `TheWindowManager`, `TheNameKeyGenerator`, `TheDisplay` global instances
