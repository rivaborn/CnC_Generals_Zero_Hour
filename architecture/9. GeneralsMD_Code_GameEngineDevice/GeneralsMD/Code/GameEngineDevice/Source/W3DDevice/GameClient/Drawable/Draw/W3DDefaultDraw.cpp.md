# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DDefaultDraw.cpp

## Purpose
Implements the default draw module for W3D (W3D2) renderable objects in the game engine.

## Responsibilities
- Manages creation and cleanup of W3D render objects and shadows
- Handles object transformation and scaling
- Implements serialization (Xfer) and CRC for network synchronization
- Provides shadow visibility control

## Key Types
- `W3DDefaultDraw` (Class): Default draw module for W3D objects
- `Shadow::ShadowTypeInfo` (Struct): Shadow configuration parameters

## Key Functions
### `W3DDefaultDraw::W3DDefaultDraw`
- Purpose: Constructor that initializes the render object and shadow
- Calls: `W3DDisplay::m_assetManager->Create_Render_Obj`, `TheW3DShadowManager->addShadow`, `W3DDisplay::m_3DScene->Add_Render_Object`

### `W3DDefaultDraw::reactToTransformChange`
- Purpose: Updates render object transform when parent object moves
- Calls: `m_renderObject->Set_Transform`

### `W3DDefaultDraw::doDrawModule`
- Purpose: Renders the object with proper scaling and transformation
- Calls: `m_renderObject->Set_ObjectScale`, `m_renderObject->Set_Transform`

### `W3DDefaultDraw::xfer`
- Purpose: Serializes object state for network synchronization
- Calls: `DrawModule::xfer`, `xfer->xferVersion`

## Globals
- `TheW3DShadowManager` (External): Global shadow manager instance

## Dependencies
- Common: `FileSystem`, `GlobalData`, `ThingTemplate`, `Xfer`
- GameClient: `Drawable`, `Shadow`, `FXList`
- GameLogic: `Object`, `TerrainLogic`
- WW3D2: `HAnim`, `HLod`, `RendObj`
- W3DDevice: `W3DDefaultDraw`, `W3DAssetManager`, `W3DDisplay`, `W3DScene`, `W3DShadow`
