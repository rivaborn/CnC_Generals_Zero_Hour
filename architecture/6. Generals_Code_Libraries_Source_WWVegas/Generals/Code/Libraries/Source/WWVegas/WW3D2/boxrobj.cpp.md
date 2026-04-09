# Generals/Code/Libraries/Source/WWVegas/WW3D2/boxrobj.cpp

## Purpose
Implements box rendering objects (axis-aligned and oriented bounding boxes) for collision detection and visualization in the SAGE engine.

## Responsibilities
- Manages box geometry, rendering, and collision testing
- Handles global initialization/shutdown of box rendering system
- Provides AABox and OBBox render object classes with transform support
- Implements collision detection (ray, AABox, OBBox)
- Loads box definitions from W3D files

## Key Types
- `BoxRenderObjClass` (Class): Base class for box render objects
- `AABoxRenderObjClass` (Class): Axis-aligned bounding box render object
- `OBBoxRenderObjClass` (Class): Oriented bounding box render object
- `BoxPrototypeClass` (Class): Prototype for loading box definitions
- `BoxLoaderClass` (Class): W3D loader for box objects

## Key Functions
### `BoxRenderObjClass::Init()`
- Purpose: Initializes global box rendering resources
- Calls: `NEW_REF`, `VertexMaterialClass` methods

### `AABoxRenderObjClass::Cast_Ray()`
- Purpose: Tests ray collision against AABox
- Calls: `CollisionMath::Collide`

### `OBBoxRenderObjClass::update_cached_box()`
- Purpose: Updates world-space cached OBBox
- Calls: `Matrix3D::Transform_Vector`

### `BoxLoaderClass::Load_W3D()`
- Purpose: Loads box definition from W3D chunk
- Calls: `cload.Read`

## Globals
- `_BoxFaces` (Vector3i[]): Face connectivity for box geometry
- `_BoxVerts` (Vector3[]): Vertex positions for unit box
- `_BoxVertexNormals` (Vector3[]): Precomputed vertex normals
- `_BoxMaterial` (VertexMaterialClass*): Shared material for boxes
- `_BoxShader` (ShaderClass): Shader used for box rendering
- `_BoxLoader` (BoxLoaderClass): Global box loader instance

## Dependencies
- `boxrobj.h`, `w3d_util.h`, `wwdebug.h`, `vertmaterial.h`
- `ww3d.h`, `chunkio.h`, `rinfo.h`, `coltest.h`
- `inttest.h`, `dx8wrapper.h`, `dx8indexbuffer.h`
- `dx8vertexbuffer.h`, `dx8fvf.h`, `sortingrenderer.h`
- `visrasterizer.h`
