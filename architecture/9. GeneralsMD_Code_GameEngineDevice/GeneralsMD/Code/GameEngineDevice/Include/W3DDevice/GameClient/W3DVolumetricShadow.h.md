# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DVolumetricShadow.h

## Purpose
Header for volumetric shadow rendering in the W3D engine, managing shadow geometry and rendering tasks.

## Responsibilities
- Manages shadow casters and their rendering
- Handles dynamic and static shadow volumes
- Provides silhouette and shadow volume construction tools
- Integrates with the W3D buffer manager for rendering tasks

## Key Types
- **W3DVolumetricShadowManager (Class)**: Manages all shadow casters and rendering tasks
- **W3DVolumetricShadow (Class)**: Represents a single shadow caster with geometry and rendering logic
- **W3DVolumetricShadowRenderTask (Struct)**: Rendering task for dynamic shadow volumes
- **SHADOW_DYNAMIC (Enum)**: Flag for dynamic shadow casters

## Key Functions
### W3DVolumetricShadowManager::addShadow
- Purpose: Adds a shadow caster to the rendering system
- Calls: Not inferable

### W3DVolumetricShadow::Update
- Purpose: Updates shadow volumes when necessary
- Calls: updateVolumes, updateMeshVolume

### W3DVolumetricShadow::RenderVolume
- Purpose: Renders a specific shadow volume from the model hierarchy
- Calls: Not inferable

## Globals
- **TheW3DVolumetricShadowManager (W3DVolumetricShadowManager*)**: Global instance of the shadow manager

## Dependencies
- matrix4.h
- W3DDevice/GameClient/W3DBufferManager.h
- GameClient/Shadow.h
- W3DShadowGeometry (forward reference)
- W3DShadowGeometryManager (forward reference)
- Geometry (forward reference)
- PolyNeighbor (forward reference)
- Drawable (forward reference)
