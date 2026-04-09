# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DDefaultDraw.cpp

## Purpose
Implements the default W3D drawing module for game objects, handling rendering and shadow management.

## Responsibilities
- Manages W3D render objects and shadows for drawable game entities
- Handles transform updates and scaling for rendered objects
- Provides shadow visibility control based on shroud state
- Implements serialization (Xfer) and CRC functionality
- Manages asset loading and cleanup (conditionally compiled)

## Key Types
- `W3DDefaultDraw` (Class): Default W3D drawing module implementation
- `Shadow::ShadowTypeInfo` (Struct): Shadow configuration parameters

## Key Functions
### `W3DDefaultDraw::W3DDefaultDraw`
- Purpose: Constructor that initializes render object and shadow
- Calls: `W3DDisplay::m_assetManager->Create_Render_Obj`, `TheW3DShadowManager->addShadow`, `W3DDisplay::m_3DScene->Add_Render_Object`

### `W3DDefaultDraw::reactToTransformChange`
- Purpose: Updates render object transform when parent object moves
- Calls: `m_renderObject->Set_Transform`

### `W3DDefaultDraw::doDrawModule`
- Purpose: Renders the object with proper scaling and transformation
- Calls: `m_renderObject->Set_ObjectScale`, `m_renderObject->Set_Transform`

### `W3DDefaultDraw::xfer`
- Purpose: Serialization method for network synchronization
- Calls: `DrawModule::xfer`, `xfer->xferVersion`

## Globals
- `TheW3DShadowManager` (External): Global shadow manager instance

## Dependencies
- Common: `FileSystem`, `GlobalData`, `ThingTemplate`, `Xfer`
- GameClient: `Drawable`, `Shadow`, `FXList`
- GameLogic: `Object`, `TerrainLogic`
- WW3D2: `HAnim`, `HLod`, `RendObj`
- W3DDevice: `W3DDefaultDraw.h`, `W3DAssetManager`, `W3DDisplay`, `W3DScene`, `W3DShadow`
