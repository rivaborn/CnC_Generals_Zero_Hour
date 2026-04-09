# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DProjectedShadow.h

## Purpose
Manages real-time projected shadows and decals in the W3D rendering system.

## Responsibilities
- Manages shadow textures and render targets
- Handles shadow rendering and decal placement
- Maintains shadow camera and light environment
- Provides interface for adding/removing shadows and decals

## Key Types
- **W3DProjectedShadowManager (Class)**: Manages projected shadows and decals
- **W3DShadowTexture (Class)**: Forward reference to shadow texture class
- **W3DProjectedShadow (Class)**: Forward reference to individual shadow class
- **Drawable (Class)**: Forward reference to drawable objects

## Key Functions
### W3DProjectedShadowManager::renderShadows
- Purpose: Renders all shadows onto affected objects
- Calls: renderProjectedTerrainShadow

### W3DProjectedShadowManager::addShadow
- Purpose: Adds a new shadow with specified texture
- Calls: None visible

### W3DProjectedShadowManager::queueDecal
- Purpose: Adds shadow decal to render list (conforms to terrain)
- Calls: None visible

### W3DProjectedShadowManager::flushDecals
- Purpose: Renders all decals with given texture
- Calls: None visible

## Globals
- **TheW3DProjectedShadowManager (W3DProjectedShadowManager*)**: Global instance of the shadow manager

## Dependencies
- "GameClient/Shadow.h" (ProjectedShadowManager base class)
- TextureClass, CameraClass, LightEnvironmentClass, SpecialRenderInfoClass (forward references)
- RenderInfoClass, RenderObjClass, Shadow::ShadowTypeInfo (external types)
