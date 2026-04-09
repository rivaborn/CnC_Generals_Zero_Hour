# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdglossmask.h

## Purpose
Defines shader classes for gloss mask rendering effects in the SAGE engine.

## Responsibilities
- Declares `ShdGlossMaskDefClass` for gloss mask shader definitions
- Declares `Shd6GlossMaskClass` for Direct3D 6-compatible gloss mask rendering
- Manages texture and material properties for gloss effects
- Provides interface for shader creation and validation

## Key Types
- **ShdGlossMaskDefClass (Class)**: Gloss mask shader definition with editable properties
- **Shd6GlossMaskClass (Class)**: D3D6-specific gloss mask shader implementation
- **None**: No enums/structs defined

## Key Functions
### ShdGlossMaskDefClass::Clone
- Purpose: Creates a copy of the shader definition
- Calls: Constructor

### ShdGlossMaskDefClass::Create
- Purpose: Creates a hardware-compatible shader instance
- Calls: Not visible in header

### Shd6GlossMaskClass::Apply_Shared
- Purpose: Applies shared shader state for gloss mask rendering
- Calls: Not visible in header

### Shd6GlossMaskClass::Apply_Instance
- Purpose: Applies instance-specific shader state
- Calls: Not visible in header

## Globals
- **View_Projection_Matrix (Matrix4x4)**: Static matrix for view/projection transformations

## Dependencies
- `shdinterface.h`, `shddef.h`, `saveload.h`, `shader.h`
- `StringClass`, `Vector3`, `Vector4`, `TextureClass`, `D3DMATERIAL8`
- `ShdDefClass`, `ShdInterfaceClass`, `RenderInfoClass`, `VertexStreamStruct
