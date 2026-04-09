# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarResizer.cpp

## Purpose
Manages dynamic resizing of control bar windows based on screen resolution.

## Responsibilities
- Loads and parses control bar resizing configurations from INI files
- Maintains a list of resizable windows with default and alternative positions/sizes
- Applies appropriate sizing based on current display resolution
- Handles window creation and cleanup

## Key Types
- `ResizerWindow` (struct): Stores default and alternative positions/sizes for a window
- `ControlBarResizer` (class): Main class managing the resizing functionality
- `ResizerWindowList` (type): Container for tracking resizable windows

## Key Functions
### `ControlBarResizer::init`
- Purpose: Loads resizing configuration from INI file
- Calls: `INI::load`

### `ControlBarResizer::sizeWindowsDefault`
- Purpose: Restores windows to their default positions and sizes
- Calls: `GameWindow::winSetPosition`, `GameWindow::winSetSize`

### `ControlBarResizer::sizeWindowsAlt`
- Purpose: Applies alternative sizing based on current resolution
- Calls: `GameWindow::winSetPosition`, `GameWindow::winSetSize`, `TheDisplay::getWidth`, `TheDisplay::getHeight`

### `INI::parseControlBarResizerDefinition`
- Purpose: Parses INI definitions for control bar resizing
- Calls: `INI::initFromINI`

## Globals
- `ControlBarResizer::m_controlBarResizerParseTable` (FieldParse[]): INI parsing table for resizer configuration

## Dependencies
- `ControlBar.h`, `ControlBarResizer.h`, `GameWindow.h`, `GameWindowManager.h`, `Display.h`
- `INI` class for configuration parsing
- `GameWindow` for window manipulation
- `TheWindowManager`, `TheNameKeyGenerator`, `TheDisplay` global instances
