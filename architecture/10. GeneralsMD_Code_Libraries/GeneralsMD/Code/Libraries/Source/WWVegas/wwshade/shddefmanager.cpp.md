# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shddefmanager.cpp

## Purpose
Manages shader definition factories and provides creation/serialization of shader definitions.

## Responsibilities
- Registers/unregisters shader definition factories
- Looks up factories by class ID or name
- Creates shader definition instances
- Saves/loads shader definitions via chunk I/O

## Key Types
- `ShdDefManagerClass`: Manages shader definition factories and instances
- `ShdDefFactoryClass`: Factory base class for shader definitions (external)
- `ShdDefClass`: Base class for shader definitions (external)

## Key Functions
### `Find_Factory(uint32 class_id)`
- Purpose: Finds factory by class ID
- Calls: None

### `Find_Factory(const char *name)`
- Purpose: Finds factory by name
- Calls: `stricmp`

### `Register_Factory(ShdDefFactoryClass *factory)`
- Purpose: Registers a factory with the system
- Calls: `Link_Factory`

### `Unregister_Factory(ShdDefFactoryClass *factory)`
- Purpose: Removes a factory from the system
- Calls: `Unlink_Factory`

### `Create_ShdDefClass_Instance(uint32 class_id)`
- Purpose: Creates a shader definition instance
- Calls: `Find_Factory`, factory's `Create()`

### `Save_Shader(ChunkSaveClass& csave, ShdDefClass* shddef)`
- Purpose: Saves shader definition to chunk stream
- Calls: `Begin_Chunk`, `Write`, `End_Chunk`, `shddef->Save`

### `Load_Shader(ChunkLoadClass& cload, ShdDefClass** shddef)`
- Purpose: Loads shader definition from chunk stream
- Calls: `Open_Chunk`, `Read`, `Close_Chunk`, `Create_ShdDefClass_Instance`, `shddef->Load`

## Globals
- `_FactoryListHead` (ShdDefFactoryClass*): Head of the factory linked list

## Dependencies
- `w3d_file.h`, `chunkio.h`, `shddef.h`, `shddefmanager.h`, `shddeffactory.h`, `wwdebug.h`, `string.h`
- `ShdDefFactoryClass`, `ShdDefClass`, `ChunkSaveClass`, `ChunkLoadClass`
