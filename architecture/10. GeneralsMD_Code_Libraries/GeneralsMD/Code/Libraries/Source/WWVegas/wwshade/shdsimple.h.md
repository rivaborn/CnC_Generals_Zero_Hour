# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdsimple.h

## Purpose
Defines simple shader classes for the SAGE engine, including a basic shader definition and its implementation.

## Responsibilities
- Declares `ShdSimpleDefClass` for shader configuration
- Declares `Shd6SimpleClass` for shader runtime implementation
- Manages texture, ambient, and diffuse properties
- Provides shader creation and validation interfaces

## Key Types
- **ShdSimpleDefClass (Class)**: Shader definition with texture, ambient, and diffuse properties
- **Shd6SimpleClass (Class)**: Runtime shader implementation for Direct3D 6
- **None**: No enums/structs defined

## Key Functions
### ShdSimpleDefClass::Create
- Purpose: Creates a shader instance compatible with current hardware/API
- Calls: Not inferable

### Shd6SimpleClass::Apply_Shared
- Purpose: Applies shared shader state for rendering
- Calls: Not inferable

### Shd6SimpleClass::Apply_Instance
- Purpose: Applies per-instance shader state for rendering
- Calls: Not inferable

## Globals
- **Shd6SimpleClass::View_Projection_Matrix (Matrix4x4)**: Stores the combined view/projection matrix

## Dependencies
- `shdinterface.h` (ShdDefClass, ShdInterfaceClass)
- `shddef.h` (Shader definitions)
- `StringClass`, `Vector3`, `Vector4`, `TextureClass`, `Matrix4x4`, `D3DMATERIAL8` (External types)
