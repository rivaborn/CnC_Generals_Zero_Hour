# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdlegacyw3d.h

## Purpose
Header file defining legacy W3D shader classes for backward compatibility with the old material system.

## Responsibilities
- Defines `ShdLegacyW3DDefClass` for shader definition and creation
- Defines `Shd6LegacyW3DClass` for shader instance management
- Provides interfaces for texture, material, and shader handling
- Supports serialization and validation of shader configurations

## Key Types
- **ShdLegacyW3DDefClass (Class)**: Legacy shader definition wrapper for old material system
- **Shd6LegacyW3DClass (Class)**: Legacy shader instance implementation

## Key Functions
### `ShdLegacyW3DDefClass::Init`
- Purpose: Initialize the shader definition
- Calls: None visible

### `ShdLegacyW3DDefClass::Create`
- Purpose: Create a shader instance compatible with current hardware/API
- Calls: None visible

### `Shd6LegacyW3DClass::Apply_Shared`
- Purpose: Apply shared shader state for a render pass
- Calls: None visible

### `Shd6LegacyW3DClass::Apply_Instance`
- Purpose: Apply instance-specific shader state for a render pass
- Calls: None visible

## Globals
- None

## Dependencies
- `shdinterface.h`, `shddef.h`, `meshmatdesc.h`
- `ShdDefClass`, `ShdInterfaceClass`, `StringClass`, `ChunkSaveClass`, `ChunkLoadClass`, `W3dShaderStruct`, `W3dVertexMaterialStruct`, `VertexMaterialClass`, `ShaderClass`, `TextureClass`, `RenderInfoClass`, `VertexStreamStruct`
