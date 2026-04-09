# Generals/Code/Libraries/Source/WWVegas/WW3D2/boxrobj.h

## Purpose
Defines render objects for axis-aligned and oriented bounding boxes used in collision detection.

## Responsibilities
- Declares base and derived render object classes for collision boxes
- Provides loading infrastructure for box prototypes
- Manages display masking for debugging visualization
- Implements collision testing interfaces

## Key Types
- **VertexMaterialClass (Class)**: Not inferable (forward declaration)
- **BoxRenderObjClass (Class)**: Base class for collision box render objects
- **AABoxRenderObjClass (Class)**: Axis-aligned bounding box render object
- **OBBoxRenderObjClass (Class)**: Oriented bounding box render object
- **BoxLoaderClass (Class)**: Prototype loader for box objects
- **BoxPrototypeClass (Class)**: Prototype class for box definitions

## Key Functions
### `BoxRenderObjClass::render_box`
- Purpose: Renders a box given center and extent
- Calls: Not inferable (implementation in .cpp)

### `BoxRenderObjClass::vis_render_box`
- Purpose: Special rendering for visualization
- Calls: Not inferable

### `AABoxRenderObjClass::update_cached_box`
- Purpose: Updates the cached axis-aligned box
- Calls: Not inferable

### `OBBoxRenderObjClass::update_cached_box`
- Purpose: Updates the cached oriented box
- Calls: Not inferable

## Globals
- **_BoxLoader (BoxLoaderClass)**: Global loader instance for box prototypes

## Dependencies
- `rendobj.h`, `w3d_file.h`, `shader.h`, `proto.h`, `obbox.h`
- `RenderObjClass`, `W3dBoxStruct`, `AABoxClass`, `OBBoxClass`, `PrototypeLoaderClass`, `PrototypeClass`
