# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DInGameUI.cpp

## Purpose
Implements the in-game UI for the W3D (W3D) rendering system in Command & Conquer Generals/Zero Hour.

## Responsibilities
- Manages move/attack hints and building placement visuals
- Handles drag selection rendering
- Loads and displays text-based UI elements
- Integrates with the W3D scene and asset management

## Key Types
- `W3DInGameUI` (Class): Main in-game UI controller
- `DebugHintObject` (Class): Debug rendering helper (DEBUG only)
- `MoveHint` (Struct): Stores move hint position/frame data

## Key Functions
### `loadText`
- Purpose: Loads text from a file into a listbox UI element
- Calls: `fopen`, `fgets`, `GadgetListBoxReset`, `GadgetListBoxAddEntryText`, `fclose`

### `drawMoveHints`
- Purpose: Renders move hint markers in the 3D scene
- Calls: `TheTerrainLogic->alignOnTerrain`, `W3DDisplay::m_3DScene->Add_Render_Object`, `Set_Transform`

### `drawPlaceAngle`
- Purpose: Handles building placement angle visualization
- Calls: `W3DDisplay::m_assetManager->Create_Render_Obj`, `W3DDisplay::m_3DScene->Add_Render_Object`

## Globals
- `TheGlobalData` (External): Accesses game data (e.g., move hint names)
- `TheGameClient` (External): Frame timing and game state
- `TheTerrainLogic` (External): Terrain alignment and collision

## Dependencies
- W3D rendering system (`W3DDisplay`, `W3DScene`)
- Game logic (`GameLogic`, `TerrainLogic`)
- UI system (`GameWindowManager`, `GadgetListBox`)
- Asset management (`W3DAssetManager`)
- Core math/geometry types (`Coord3D`, `Matrix3D`)
