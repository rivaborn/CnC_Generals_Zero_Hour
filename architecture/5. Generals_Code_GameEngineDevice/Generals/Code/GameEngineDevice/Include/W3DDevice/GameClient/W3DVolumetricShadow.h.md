# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DVolumetricShadow.h

## Purpose
Header for volumetric shadow rendering in the W3D engine, managing shadow geometry and rendering tasks.

## Responsibilities
- Defines shadow manager and shadow classes
- Manages shadow volume generation and rendering
- Handles dynamic and static shadow casters
- Provides silhouette and volume construction tools

## Key Types
- **W3DVolumetricShadowManager (Class)**: Manages all volumetric shadows in the scene
- **W3DVolumetricShadow (Class)**: Represents a single shadow caster with volume data
- **W3DVolumetricShadowRenderTask (Struct)**: Render task for dynamic shadow volumes
- **SHADOW_DYNAMIC (Enum)**: Flag for dynamic shadow casters

## Key Functions
### W3DVolumetricShadowManager::addShadow
- Purpose: Adds a shadow caster to the rendering system
- Calls: Not visible in header

### W3DVolumetricShadow::Update
- Purpose: Updates shadow volumes when necessary
- Calls: updateVolumes, updateMeshVolume

### W3DVolumetricShadow::RenderVolume
- Purpose: Renders a specific shadow volume
- Calls: Not visible in header

## Globals
- **TheW3DVolumetricShadowManager (W3DVolumetricShadowManager*)**: Global shadow manager instance

## Dependencies
- matrix4.h
- W3DDevice/GameClient/W3DBufferManager.h
- GameClient/Shadow.h
- Forward references to W3DShadowGeometry, W3DShadowGeometryManager, Geometry, PolyNeighbor, Drawable
