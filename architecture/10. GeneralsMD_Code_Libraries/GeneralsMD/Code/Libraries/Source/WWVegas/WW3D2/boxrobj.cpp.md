# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/boxrobj.cpp

## Purpose
Implements box rendering objects (axis-aligned and oriented bounding boxes) for collision and visualization in the SAGE engine.

## Responsibilities
- Manages box geometry, rendering, and collision detection
- Handles initialization/shutdown of box rendering system
- Provides AABox and OBBox render object implementations
- Supports ray and box collision tests
- Loads box definitions from W3D files

## Key Types
- `BoxRenderObjClass` (Class): Base class for box render objects
- `AABoxRenderObjClass` (Class): Axis-aligned bounding box render object
- `OBBoxRenderObjClass` (Class): Oriented bounding box render object
- `BoxLoaderClass` (Class): W3D loader for box objects
- `BoxPrototypeClass` (Class): Prototype for box objects

## Key Functions
### `BoxRenderObjClass::Init`
- Purpose: Initializes global box rendering system
- Calls: `NEW_REF`, `VertexMaterialClass` methods

### `BoxRenderObjClass::render_box`
- Purpose: Submits box geometry to rendering pipeline
- Calls: `DX8Wrapper` methods, `_BoxMaterial`, `_BoxShader`

### `AABoxRenderObjClass::Cast_Ray`
- Purpose: Tests ray collision against AABox
- Calls: `CollisionMath::Collide`

### `OBBoxRenderObjClass::update_cached_box`
- Purpose: Updates world-space cached box from object-space data
- Calls: `Matrix3D::Transform_Vector`

## Globals
- `_BoxFaces` (TriIndex[]): Predefined box face indices
- `_BoxVerts` (Vector3[]): Predefined box vertex positions
- `_BoxVertexNormals` (Vector3[]): Predefined vertex normals
- `_BoxMaterial` (VertexMaterialClass*): Shared material for boxes
- `_BoxShader` (ShaderClass): Shared shader for boxes
- `_BoxLoader` (BoxLoaderClass): Global box loader instance

## Dependencies
- `boxrobj.h`, `w3d_util.h`, `wwdebug.h`, `vertmaterial.h`, `ww3d.h`
- `chunkio.h`, `rinfo.h`, `coltest.h`, `inttest.h`, `dx8wrapper.h`
- `dx8indexbuffer.h`, `dx8vertexbuffer.h`, `dx8fvf.h`
- `sortingrenderer.h`, `visrasterizer.h`, `meshgeometry.h`
