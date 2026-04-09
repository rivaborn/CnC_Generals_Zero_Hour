# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DGranny.h

## Purpose
Header file defining Granny model loading, rendering, and animation systems for the SAGE engine.

## Responsibilities
- Declares Granny model loading and rendering classes
- Defines animation management for Granny models
- Provides interface for Granny model prototypes and instances
- Manages render state batching for Granny models

## Key Types
- **GrannyLoaderClass (Class)**: Handles loading Granny model files and material libraries
- **GrannyAnimClass (Class)**: Custom animation class for Granny models
- **GrannyAnimManagerClass (Class)**: Manages animation loading and retrieval
- **GrannyRenderObjClass (Class)**: Render object for Granny models
- **GrannyPrototypeClass (Class)**: Prototype definition for Granny models
- **GrannyRenderObjSystem (Class)**: System for batching and rendering Granny models

## Key Functions
### GrannyLoaderClass::Load_W3D
- Purpose: Loads a Granny model file
- Calls: Not inferable

### GrannyAnimClass::Load_W3D
- Purpose: Loads a Granny animation file
- Calls: Not inferable

### GrannyAnimManagerClass::Load_Anim
- Purpose: Loads an animation by name
- Calls: Load_Raw_Anim

### GrannyRenderObjClass::Render
- Purpose: Renders the Granny model
- Calls: Not inferable

### GrannyRenderObjSystem::Flush
- Purpose: Renders all queued Granny models
- Calls: Not inferable

## Globals
- **_GrannyLoader (GrannyLoaderClass)**: Global loader instance
- **TheGrannyRenderObjSystem (GrannyRenderObjSystem)**: Singleton for Granny rendering

## Dependencies
- "always.h", "hanim.h", "proto.h", "rendobj.h", "LightEnvironment.h", "w3d_file.h", "dx8vertexbuffer.h", "dx8indexbuffer.h", "shader.h", "vertmaterial.h", "Lib/BaseType.h"
- granny.h (included conditionally)
- HashTableClass, Vector3, Quaternion, Matrix3D, SphereClass, AABoxClass, Bool, Int, Real, UnsignedInt, VertexMaterialClass, ShaderClass, RenderInfoClass, RayCollisionTestClass
