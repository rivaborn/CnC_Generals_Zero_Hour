# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/GUI/Gadget/W3DTabControl.cpp

## Purpose
Implements rendering logic for tab controls in the W3D UI system, supporting both colored and image-based tabs.

## Responsibilities
- Renders tab controls with either solid colors or images
- Handles tab positioning and layout based on configuration
- Manages visual states (active, disabled, enabled) for each tab
- Draws borders and backgrounds for the tab control container

## Key Types
- `TabControlData` (struct): Stores tab control configuration (tab count, positions, active tab, etc.)
- `GameWindow` (class): Base window class for UI elements
- `WinInstanceData` (struct): Window rendering context data

## Key Functions
### W3DGadgetTabControlDraw
- Purpose: Renders tab control using solid colors for each tab
- Calls: `W3DGameWinDefaultDraw`, `winGetScreenPosition`, `winGetSize`, `winDrawBorder`, `winOpenRect`, `winFillRect`

### W3DGadgetTabControlImageDraw
- Purpose: Renders tab control using images for each tab
- Calls: `W3DGameWinDefaultDraw`, `winGetScreenPosition`, `winGetSize`, `winDrawBorder`, `winDrawImage`

## Globals
- `TheWindowManager` (WindowManager*): Global window management system

## Dependencies
- `GameClient/GameWindowGlobal.h`
- `GameClient/GameWindowManager.h`
- `GameClient/GadgetTabControl.h`
- `W3DDevice/GameClient/W3DGameWindow.h`
- `W3DDevice/GameClient/W3DGadget.h`
- `W3DDevice/GameClient/W3DDisplay.h`
