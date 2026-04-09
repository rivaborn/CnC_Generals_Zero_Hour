# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DScene.h

## Purpose
Defines scene management classes for 3D/2D rendering in the SAGE engine, including custom rendering passes and lighting control.

## Responsibilities
- Manages 3D/2D scene rendering with customizable passes
- Handles dynamic lighting and visibility checks
- Controls object occlusion and translucency rendering
- Manages player-specific color passes and special effects (shroud, heat vision, frenzy)

## Key Types
- **RTS3DScene (Class)**: Main 3D scene manager with lighting and rendering control
- **RTS2DScene (Class)**: 2D overlay scene manager
- **RTS3DInterfaceScene (Class)**: 3D interface overlay scene manager
- **CustomScenePassModes (Enum)**: Flags for non-standard rendering modes
- **W3DDynamicLight (Class)**: Dynamic light object
- **LightClass (Class)**: Light source
- **Drawable (Class)**: Renderable object
- **MaterialPassClass (Class)**: Base material pass
- **W3DShroudMaterialPassClass (Class)**: Shroud rendering pass
- **W3DMaskMaterialPassClass (Class)**: Mask rendering pass

## Key Functions
### RTS3DScene::castRay
- Purpose: Perform ray picking against scene objects
- Calls: Not inferable

### RTS3DScene::Customized_Render
- Purpose: Customizable rendering pipeline for RTS3DScene
- Calls: Not inferable

### RTS3DScene::Visibility_Check
- Purpose: Check object visibility in the scene
- Calls: Not inferable

### RTS3DScene::Render
- Purpose: Main rendering function for the scene
- Calls: Not inferable

### RTS3DScene::addDynamicLight
- Purpose
