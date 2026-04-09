# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/renderobjectrecycler.cpp

## Purpose
Manages a pool of reusable render objects to optimize memory usage in the SAGE engine.

## Responsibilities
- Recycles render objects by caching inactive ones
- Provides methods to retrieve and return render objects
- Resets render objects for reuse (clearing state, animations, etc.)

## Key Types
- **RenderObjectRecyclerClass**: Manages the render object pool
- **RenderObjClass**: Base class for renderable objects
- **ParticleEmitterClass**: Specialized render object for particle effects

## Key Functions
### `Reset`
- Purpose: Clears the inactive render object cache
- Calls: `InactiveModels.Reset_List()`

### `Get_Render_Object`
- Purpose: Retrieves a render object from the pool or creates a new one
- Calls: `InactiveModels` iteration, `WW3DAssetManager::Get_Instance()->Create_Render_Obj()`, `Reset_Model()`

### `Return_Render_Object`
- Purpose: Returns a render object to the pool for reuse
- Calls: `Insert_Inactive_Model()`

### `Insert_Inactive_Model`
- Purpose: Adds a render object to the inactive pool
- Calls: `InactiveModels.Add()`

### `Reset_Model`
- Purpose: Resets a render object's state for reuse
- Calls: Recursively calls itself for sub-objects, `ParticleEmitterClass::Reset()`, `RenderObjClass::Set_Animation()`

## Globals
- **InactiveModels** (RefRenderObjList): Stores inactive render objects

## Dependencies
- `renderobjectrecycler.h`
- `rendobj.h`
- `assetmgr.h`
- `part_emt.h`
- `matrix3d.h`
