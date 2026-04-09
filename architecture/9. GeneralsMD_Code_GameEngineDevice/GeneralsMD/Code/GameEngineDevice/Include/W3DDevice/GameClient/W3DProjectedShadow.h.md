# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DProjectedShadow.h

## Purpose
Manages projected shadows and decals in the W3D rendering system.

## Responsibilities
- Manages shadow textures and rendering
- Handles shadow projection updates
- Maintains shadow and decal lists
- Provides shadow rendering functionality

## Key Types
- **W3DProjectedShadowManager (Class)**: Manages all projected shadows and decals
- **W3DProjectedShadow (Class)**: Represents an individual projected shadow
- **TexProjectClass (Class)**: Handles shadow projection calculations
- **W3DShadowTexture (Class)**: Shadow texture management (forward reference)
- **W3DShadowTextureManager (Class)**: Shadow texture manager (forward reference)

## Key Functions
### W3DProjectedShadowManager::renderShadows
- Purpose: Renders all shadows onto affected objects
- Calls: renderProjectedTerrainShadow

### W3DProjectedShadow::update
- Purpose: Updates shadow texture and projection when object/light moves
- Calls: updateTexture, updateProjectionParameters

### W3DProjectedShadowManager::addShadow
- Purpose: Creates a new shadow for a render object
- Calls: Not inferable

## Globals
- **TheW3DProjectedShadowManager (W3DProjectedShadowManager*)**: Global instance of the shadow manager

## Dependencies
- "GameClient/Shadow.h"
- RenderInfoClass, TextureClass, CameraClass, LightEnvironmentClass, SpecialRenderInfoClass, AABoxClass, Vector3, Matrix3D, RenderObjClass, RenderCost
- MAX_SHADOW_LIGHTS constant
