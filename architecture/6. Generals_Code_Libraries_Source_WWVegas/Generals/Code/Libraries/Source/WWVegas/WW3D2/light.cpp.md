# Generals/Code/Libraries/Source/WWVegas/WW3D2/light.cpp

## Purpose
Implements the LightClass for the WW3D2 engine, handling light types, properties, and W3D file I/O.

## Responsibilities
- Manages light properties (type, intensity, color, attenuation, spot parameters)
- Handles W3D file loading/saving for lights
- Implements persistence via ChunkSave/ChunkLoad
- Registers/unregisters lights with the scene
- Provides bounding volume calculations for lights

## Key Types
- LightClass (Class): Main light object with properties and W3D I/O
- (anonymous enum) (Enum): Chunk IDs for persistence (LIGHT_CHUNK_W3DFILE, LIGHT_CHUNK_VARIABLES, LIGHT_VARIABLE_TRANSFORM)

## Key Functions
### LightClass::Load_W3D
- Purpose: Loads light data from a W3D file chunk
- Calls: cload.Open_Chunk, cload.Read, cload.Close_Chunk, W3dUtilityClass::Convert_Color, W3dUtilityClass::Convert_Vector

### LightClass::Save_W3D
- Purpose: Saves light data to a W3D file chunk
- Calls: csave.Begin_Chunk, csave.Write, csave.End_Chunk, W3dUtilityClass::Convert_Color

### LightClass::Save
- Purpose: Persistence save support
- Calls: Save_W3D, WRITE_MICRO_CHUNK

### LightClass::Load
- Purpose: Persistence load support
- Calls: Load_W3D, READ_MICRO_CHUNK

## Globals
- _LightFactory (SimplePersistFactoryClass<LightClass,WW3D_PERSIST_CHUNKID_LIGHT>): Persistence factory for LightClass

## Dependencies
- light.h, ww3d.h, ww3dids.h, w3d_file.h, w3d_util.h, w3derr.h, chunkio.h, rinfo.h, scene.h, persistfactory.h, statistics.h
