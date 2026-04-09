# Generals/Code/Libraries/Source/WWVegas/WW3D2/renderobjectrecycler.cpp

## Purpose
Manages a pool of reusable render objects to optimize memory usage and performance.

## Responsibilities
- Recycles render objects by caching inactive ones
- Retrieves or creates render objects when needed
- Resets render objects before reuse
- Handles particle emitters and animations

## Key Types
- `RenderObjectRecyclerClass`: Manages render object recycling
- `RenderObjClass`: Base class for renderable objects
- `ParticleEmitterClass`: Specialized render object for particle effects

## Key Functions
### `Reset`
- Purpose: Clears the inactive render object cache
- Calls: `InactiveModels.Reset_List()`

### `Get_Render_Object`
- Purpose: Retrieves a render object from cache or creates a new one
- Calls: `stricmp`, `WW3DAssetManager::Get_Instance()->Create_Render_Obj`, `Reset_Model`

### `Return_Render_Object`
- Purpose: Returns a render object to the cache
- Calls: `Insert_Inactive_Model`

### `Insert_Inactive_Model`
- Purpose: Adds a render object to the inactive pool
- Calls: `InactiveModels.Add`

### `Reset_Model`
- Purpose: Resets a render object for reuse
- Calls: `Get_Num_Sub_Objects`, `Get_Sub_Object`, `Release_Ref`, `ParticleEmitterClass::Reset`, `Peek_Animation`, `Set_Animation`

## Globals
- `InactiveModels` (RefRenderObjList): Stores cached render objects

## Dependencies
- `renderobjectrecycler.h`
- `rendobj.h`
- `assetmgr.h`
- `part_emt.h`
- `matrix3d.h`
