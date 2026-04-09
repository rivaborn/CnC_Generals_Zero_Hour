# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/light.cpp

## Purpose
Implements the LightClass for the WW3D2 engine, handling light types, properties, and serialization.

## Responsibilities
- Manages light properties (type, intensity, color, attenuation, spot properties)
- Handles W3D file loading/saving for lights
- Implements persistence via ChunkSave/ChunkLoad
- Registers/unregisters lights with the scene
- Provides bounding volume calculations for lights

## Key Types
- LightClass (Class): Main light implementation with properties and serialization
- (anonymous enum) (Enum): Chunk IDs for persistence (LIGHT_CHUNK_W3DFILE, LIGHT_CHUNK_VARIABLES, LIGHT_VARIABLE_TRANSFORM)
- LIGHT_CHUNK_W3DFILE (Enum): Persistence chunk ID for W3D format data
- LIGHT_CHUNK_VARIABLES (Enum): Persistence chunk ID for additional state
- LIGHT_VARIABLE_TRANSFORM (Enum): Micro-chunk ID for transform data

## Key Functions
### LightClass::Load_W3D
- Purpose: Loads light data from a W3D file chunk
- Calls: cload.Open_Chunk, cload.Read, cload.Close_Chunk, W3dUtilityClass::Convert_Color, W3dUtilityClass::Convert_Vector

### LightClass::Save_W3D
- Purpose: Saves light data to a W3D file chunk
- Calls: csave.Begin_Chunk, csave.Write, csave.End_Chunk, W3dUtilityClass::Convert_Color

### LightClass::Save
- Purpose: Persistence support for saving light state
- Calls: Save_W3D, csave.Begin_Chunk, csave.End_Chunk, WRITE_MICRO_CHUNK

### LightClass::Load
- Purpose: Persistence support for loading light state
- Calls: Load_W3D, cload.Open_Chunk, cload.Read, cload.Close_Chunk, READ_MICRO_CHUNK

### LightClass::Notify_Added
- Purpose: Registers light with scene when added
- Calls: RenderObjClass::Notify_Added, scene->Register

### LightClass::Notify_Removed
- Purpose: Unregisters light from scene when removed
- Calls: scene->Unregister, RenderObjClass::Notify_Removed

## Globals
- _LightFactory (SimplePersistFactoryClass<LightClass,WW3D_PERSIST_CHUNKID_LIGHT>): Persistence factory for LightClass

## Dependencies
- light.h, ww3d.h, ww3dids.h, w3d_file.h, w3d_util.h, w3derr.h, chunkio.h, rinfo.h, scene.h, persistfactory.h, statistics.h
- W3dLightStruct, W3dSpotLightStruct, W3dLightAttenuationStruct, ChunkLoadClass, ChunkSaveClass, SceneClass, PersistFactoryClass, RenderObjClass, Matrix3D, Vector3, SphereClass, AABoxClass
