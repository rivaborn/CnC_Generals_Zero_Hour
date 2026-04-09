# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/definition.cpp

## Purpose
Handles saving and loading of DefinitionClass objects using chunk-based serialization.

## Responsibilities
- Defines chunk IDs and variable IDs for serialization
- Implements Save/Load methods for DefinitionClass
- Manages variable serialization (ID, name)
- Handles dynamic re-registration when ID changes

## Key Types
- (anonymous enum): Chunk ID constants
- CHUNKID_VARIABLES (Enum): Chunk ID for variable data
- (anonymous enum): Variable ID constants
- VARID_INSTANCEID (Enum): Variable ID for instance ID
- XXX_VARID_PARENTID (Enum): Variable ID for parent ID (unused)
- VARID_NAME (Enum): Variable ID for name

## Key Functions
### DefinitionClass::Save
- Purpose: Saves DefinitionClass data to a chunk stream
- Calls: Begin_Chunk, Save_Variables, End_Chunk

### DefinitionClass::Load
- Purpose: Loads DefinitionClass data from a chunk stream
- Calls: Open_Chunk, Cur_Chunk_ID, Close_Chunk, Load_Variables

### DefinitionClass::Save_Variables
- Purpose: Serializes variable data (ID, name) into microchunks
- Calls: WRITE_MICRO_CHUNK, WRITE_MICRO_CHUNK_WWSTRING

### DefinitionClass::Load_Variables
- Purpose: Deserializes variable data from microchunks
- Calls: Open_Micro_Chunk, Cur_Micro_Chunk_ID, Close_Micro_Chunk, READ_MICRO_CHUNK, READ_MICRO_CHUNK_WWSTRING

### DefinitionClass::Set_ID
- Purpose: Updates instance ID and re-registers with definition manager if needed
- Calls: Unregister_Definition, Register_Definition

## Glob
