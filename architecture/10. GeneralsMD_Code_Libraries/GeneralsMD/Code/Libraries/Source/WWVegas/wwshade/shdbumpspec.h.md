# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdbumpspec.h

## Purpose
Defines the `ShdBumpSpecDefClass` for bump-mapping and specular shading effects in the SAGE engine.

## Responsibilities
- Manages bump-mapping and specular material properties
- Handles texture and bump map asset references
- Provides shader creation and validation logic
- Implements serialization for save/load functionality

## Key Types
- **ShdBumpSpecDefClass (Class)**: Bump-mapping and specular shader definition

## Key Functions
### ShdBumpSpecDefClass()
- Purpose: Default constructor
- Calls: None

### Clone()
- Purpose: Creates a copy of the shader definition
- Calls: Constructor

### Init()
- Purpose: Initializes shader for current hardware/API
- Calls: Not inferable

### Create()
- Purpose: Creates a shader instance
- Calls: Not inferable

### Is_Valid_Config()
- Purpose: Validates shader configuration
- Calls: Not inferable

### Save_Variables()
- Purpose: Serializes shader properties
- Calls: ChunkSaveClass methods

### Load_Variables()
- Purpose: Deserializes shader properties
- Calls: ChunkLoadClass methods

## Globals
- **Version (ShdVersion)**: Shader version tracking

## Dependencies
- `shddef.h` (ShdDefClass)
- `saveload.h` (ChunkSaveClass, ChunkLoadClass)
- `StringClass`, `Vector3`, `Vector2`
