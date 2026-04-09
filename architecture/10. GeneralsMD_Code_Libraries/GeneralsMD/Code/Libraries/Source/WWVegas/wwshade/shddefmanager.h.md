# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shddefmanager.h

## Purpose
Manages shader definition factories and provides factory registration, lookup, and iteration.

## Responsibilities
- Register/unregister shader definition factories
- Find factories by ID or name
- Create shader definition instances
- Save/load shader definitions
- Iterate through factories by class or globally

## Key Types
- **ShdDefClass (Class)**: Base class for shader definitions
- **ShdDefFactoryClass (Class)**: Factory for creating shader definitions
- **ChunkSaveClass (Class)**: Class for saving data chunks
- **ChunkLoadClass (Class)**: Class for loading data chunks
- **ShdDefManagerClass (Class)**: Manages shader definition factories

## Key Functions
### Find_Factory (uint32 class_id)
- Purpose: Find a factory by class ID
- Calls: None

### Find_Factory (const char *name)
- Purpose: Find a factory by name
- Calls: None

### Register_Factory (ShdDefFactoryClass *factory)
- Purpose: Register a shader definition factory
- Calls: Link_Factory

### Unregister_Factory (ShdDefFactoryClass *factory)
- Purpose: Unregister a shader definition factory
- Calls: Unlink_Factory

### Create_ShdDefClass_Instance (uint32 class_id)
- Purpose: Create a shader definition instance
- Calls: None

### Save_Shader (ChunkSaveClass& csave, ShdDefClass* shddef)
- Purpose: Save a shader definition
- Calls: None

### Load_Shader (ChunkLoadClass& cload, ShdDefClass** shddef)
- Purpose: Load a shader definition
- Calls: None

## Globals
- **_FactoryListHead (ShdDefFactory
