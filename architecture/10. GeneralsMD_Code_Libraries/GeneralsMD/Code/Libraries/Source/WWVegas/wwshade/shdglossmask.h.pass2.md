# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdglossmask.h - Enhanced Analysis

## Architectural Role
This file defines the gloss mask shader system, a key component of the SAGE engine's material rendering pipeline. It bridges the editable shader definition system with hardware-specific rendering implementations, specifically for Direct3D 6.

## Cross-References
### Incoming
- Shader manager (`ShdDefClass` hierarchy)
- Rendering pipeline (`RenderInfoClass` consumers)
- Material system (D3DMATERIAL8 usage)

### Outgoing
- Texture management (`TextureClass`)
- Vertex processing pipeline (`VertexStreamStruct`)
- Save/load system (`ChunkSaveClass`/`ChunkLoadClass`)

## Design Patterns
- **Factory Pattern**: `Create()` method for hardware-specific shader instantiation
- **Composite Pattern**: Shader definition (`ShdGlossMaskDefClass`) and implementation (`Shd6GlossMaskClass`) separation
- **Property Bag Pattern**: Vector3/Vector4 members for material properties (ambient/diffuse/specular)

*Not inferable*: No clear Observer or Strategy patterns visible in header.
