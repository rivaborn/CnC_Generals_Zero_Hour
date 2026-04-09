# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DScene.h

## Purpose
Defines scene management classes for 3D/2D rendering in the SAGE engine, including custom rendering passes and lighting control.

## Responsibilities
- Manages 3D/2D/interface scenes with customizable rendering
- Handles dynamic lighting and global light environments
- Implements visibility checks and occlusion handling
- Provides ray casting for object picking
- Manages translucent and occluded object rendering

## Key Types
- **RTS3DScene (Class)**: Main 3D scene manager with lighting and rendering control
- **RTS2DScene (Class)**: 2D overlay scene manager
- **RTS3DInterfaceScene (Class)**: 3D interface overlay scene manager
- **CustomScenePassModes (Enum)**: Flags for non-standard rendering modes
- **W3DDynamicLight (Class)**: Dynamic light object (forward declared)
- **LightClass (Class)**: Light source (forward declared)
- **Drawable (Class)**: Renderable object (forward declared)
- **MaterialPassClass (Class)**: Base material pass (forward declared)
- **W3DShroudMaterialPassClass (Class)**: Shroud rendering pass
- **W3DMaskMaterialPassClass (Class)**: Mask rendering pass

## Key Functions
### RTS3DScene::castRay
- Purpose: Perform ray collision test against scene objects
- Calls: Not inferable

### RTS3DScene::Customized_Render
- Purpose: Custom rendering implementation for RTS3DScene
- Calls: Not inferable

### RTS3DScene::Visibility_Check
- Purpose: Check object visibility in the scene
- Calls: Not inferable

### RTS3DScene::Render
- Purpose: Main rendering function for the 3D scene
- Calls: Not
