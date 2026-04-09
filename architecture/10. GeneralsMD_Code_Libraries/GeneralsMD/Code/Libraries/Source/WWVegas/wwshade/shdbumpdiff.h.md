# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdbumpdiff.h

## Purpose
Defines the `ShdBumpDiffDefClass` for bump-mapped diffuse shading in the SAGE engine.

## Responsibilities
- Manages bump-mapped diffuse shader configuration
- Handles texture and bump map asset references
- Provides ambient/diffuse lighting and bumpiness parameters
- Implements shader creation and validation logic

## Key Types
- **ShdBumpDiffDefClass (Class)**: Bump-mapped diffuse shader definition class

## Key Functions
### ShdBumpDiffDefClass()
- Purpose: Default constructor
- Calls: None

### Clone()
- Purpose: Creates a copy of the shader definition
- Calls: Constructor

### Init()
- Purpose: Initializes shader hardware/API compatibility
- Calls: Not inferable

### Create()
- Purpose: Creates a shader instance
- Calls: Not inferable

### Is_Valid_Config()
- Purpose: Validates shader configuration
- Calls: Not inferable

### Save_Variables()
- Purpose: Serializes shader parameters
- Calls: ChunkSaveClass methods

### Load_Variables()
- Purpose: Deserializes shader parameters
- Calls: ChunkLoadClass methods

## Globals
- **Version (ShdVersion)**: Shader version identifier

## Dependencies
- `shddef.h`, `saveload.h`, `shader.h`
- `ShdDefClass`, `ShdInterfaceClass`, `StringClass`, `Vector3`, `Vector2`
