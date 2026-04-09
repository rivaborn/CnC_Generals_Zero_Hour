# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DGameClient.cpp

## Purpose
Implements the W3D-specific GameClient interface for the SAGE engine, handling rendering and client-side game logic.

## Responsibilities
- Manages W3D drawable creation and rendering
- Handles terrain effects (scorch marks, object movement)
- Controls time-of-day lighting and LOD settings
- Manages ray effects and team color visualization

## Key Types
- `W3DGameClient` (Class): Main W3D game client implementation
- `Drawable` (Class): Base class for renderable objects
- `ThingTemplate` (Class): Template for creating game objects

## Key Functions
### `friend_createDrawable`
- Purpose: Creates a new drawable from a thing template
- Calls: `newInstance(Drawable)`

### `createRayEffectByTemplate`
- Purpose: Creates a ray effect between two points using a template
- Calls: `TheThingFactory->newDrawable`, `TheRayEffects->addRayEffect`

### `setTimeOfDay`
- Purpose: Updates time-of-day lighting for all render objects
- Calls: `GameClient::setTimeOfDay`, `TheWaterRenderObj->setTimeOfDay`, `TheW3DShadowManager->setTimeOfDay`, `TheDisplay->setTimeOfDay`

### `adjustLOD`
- Purpose: Adjusts texture LOD for development testing
- Calls: `WW3D::Set_Texture_Reduction`, `TheGameLODManager->setCurrentTextureReduction`, `TheTerrainRenderObject->setTextureLOD`

### `notifyTerrainObjectMoved`
- Purpose: Notifies terrain when an object moves
- Calls: `TheTerrainRenderObject->unitMoved`

## Globals
- `TheTerrainRenderObject` (Pointer): Terrain rendering object
- `TheWaterRenderObj` (Pointer): Water rendering object
- `TheW3DShadowManager` (Pointer): Shadow manager
- `TheDisplay` (Pointer): Display system
- `TheGlobalData` (Pointer): Global game data
- `TheWritableGlobalData` (Pointer): Writable global game data
- `TheGameLODManager` (Pointer): LOD manager
- `TheThingFactory` (Pointer): Thing factory
- `TheRayEffects` (Pointer): Ray effects manager

## Dependencies
- `Common/ThingTemplate.h`, `Common/ThingFactory.h`, `Common/ModuleFactory.h`, `Common/RandomValue.h`, `Common/GlobalData.h`, `Common/GameLOD.h`
- `GameClient/Drawable.h`, `GameClient/GameClient.h`, `GameClient/ParticleSys.h`, `GameClient/RayEffect.h`
- `W3
