# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DPropBuffer.cpp

## Purpose
Manages 3D prop rendering in the game world, including culling, drawing, and shroud handling.

## Responsibilities
- Loads and manages W3D prop models
- Handles prop visibility culling
- Renders props with lighting and shroud effects
- Updates prop positions and removes props

## Key Types
- `W3DPropBuffer` (Class): Main class managing prop rendering
- `Prop` (Struct): Represents a single prop with position, bounds, and render object
- `PropType` (Struct): Stores prop model type and bounds

## Key Functions
### `cull`
- Purpose: Marks props as visible/invisible based on camera frustum culling
- Calls: `CameraClass::Cull_Sphere`

### `drawProps`
- Purpose: Renders all visible props with proper lighting and shroud effects
- Calls: `RenderInfoClass` methods, `W3DShroudMaterialPassClass` methods

### `addProp`
- Purpose: Adds a new prop to the buffer
- Calls: `WW3DAssetManager::Get_Instance()->Create_Render_Obj`

### `updatePropPosition`
- Purpose: Updates a prop's position, rotation, and scale
- Calls: `RenderObjClass::Set_Transform`, `RenderObjClass::Set_ObjectScale`

## Globals
- `m_light` (LightClass*): Directional light for prop rendering
- `m_propShroudMaterialPass` (W3DShroudMaterialPassClass*): Shroud material pass
- `m_doCull` (Bool): Flag to enable/disable culling

## Dependencies
- `W3DPropBuffer.h`
- `WW3D2/Camera.h`, `WW3D2/Light.h`, `WW3D2/RInfo.h`
- `W3DDevice/GameClient/W3DShroud.h`
- `GameLogic/PartitionManager.h`
- `Common/Geometry.h`, `Common/PerfTimer.h`
