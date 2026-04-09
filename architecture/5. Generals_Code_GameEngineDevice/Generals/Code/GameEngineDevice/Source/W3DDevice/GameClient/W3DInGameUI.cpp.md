# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DInGameUI.cpp

## Purpose
Implements the in-game UI for the W3D (Warlord 3D) rendering system in Command & Conquer Generals.

## Responsibilities
- Manages move/attack hints and building placement visuals
- Handles drag selection rendering
- Loads and displays help text (commented out in release)
- Integrates with W3D scene rendering pipeline

## Key Types
- `W3DInGameUI` (Class): Main in-game UI controller
- `DebugHintObject` (Class): Debug rendering helper (DEBUG only)
- `MoveHint` (Struct): Stores move hint position/timing data

## Key Functions
### `loadText`
- Purpose: Loads text from file into a listbox gadget
- Calls: `fopen`, `fgets`, `GadgetListBoxReset`, `GadgetListBoxAddEntryText`, `fclose`

### `drawMoveHints`
- Purpose: Renders move hint markers in the 3D scene
- Calls: `TheTerrainLogic->alignOnTerrain`, `W3DDisplay::m_3DScene->Add_Render_Object`, `Set_Transform`

### `drawPlaceAngle`
- Purpose: Handles building placement angle visualization
- Calls: `W3DDisplay::m_assetManager->Create_Render_Obj`, `W3DDisplay::m_3DScene->Add_Render_Object`

## Globals
- `TheGlobalData` (External): Accesses game data (move hint names)
- `TheTerrainLogic` (External): Terrain alignment queries
- `TheGameClient` (External): Frame timing
- `TheDisplay` (External): View management

## Dependencies
- W3D rendering system (WW3D2, W3DDevice)
- Game logic (GameLogic, TerrainLogic)
- UI system (GameClient, WindowManager)
- Asset management (W3DAssetManager)
- Common utilities (GlobalData, ThingTemplate)
