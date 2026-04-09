# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DGranny.h

## Purpose
Header file defining Granny model loading, rendering, and animation systems for the SAGE engine.

## Responsibilities
- Declares Granny model loading and rendering classes
- Defines animation management for Granny models
- Provides interface for Granny model prototypes and instances
- Manages render state batching for performance

## Key Types
- **GrannyLoaderClass** (Class): Handles loading Granny model files and material libraries
- **GrannyAnimClass** (Class): Custom animation class for Granny models
- **GrannyAnimManagerClass** (Class): Manages animation assets and loading
- **GrannyRenderObjClass** (Class): Renderable Granny model instance
- **GrannyPrototypeClass** (Class): Prototype definition for Granny models
- **GrannyRenderObjSystem** (Class): System for batching and rendering Granny models
- **GrannyAnimManagerIterator** (Class): Iterator for animation manager
- **GrannyMeshDesc** (Struct): Description of a Granny mesh (indices/vertices)

## Key Functions
### GrannyLoaderClass::Load_W3D
- Purpose: Loads a Granny model file
- Calls: Granny API functions (not visible in header)

### GrannyAnimClass::Load_W3D
- Purpose: Loads animation data from a Granny file
- Calls: Granny API functions (not visible in header)

### GrannyRenderObjClass::Render
- Purpose: Renders a Granny model instance
- Calls: Granny API functions, RenderInfoClass methods

### GrannyRenderObjSystem::Flush
- Purpose: Renders all queued Granny models
- Calls: Granny API functions, rendering pipeline

## Globals
- **_GrannyLoader** (GrannyLoaderClass): Global loader instance
- **TheGrannyRenderObjSystem** (GrannyRenderObjSystem*): Singleton for Granny rendering

## Dependencies
- Granny SDK headers (granny.h)
- SAGE engine components (HAnimClass, PrototypeClass, RenderObjClass)
- Rendering infrastructure (LightEnvironmentClass, VertexMaterialClass)
- DirectX 8 components (DX8VertexBufferClass, DX8IndexBufferClass)
- Core utilities (HashTableClass, AABoxClass, SphereClass)
