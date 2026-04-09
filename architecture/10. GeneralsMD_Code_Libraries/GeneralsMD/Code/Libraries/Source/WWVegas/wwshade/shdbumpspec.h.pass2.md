# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdbumpspec.h - Enhanced Analysis

## Architectural Role
This file defines the bump-mapping and specular shading material system in the SAGE engine's rendering pipeline. It extends the base shader definition class to support advanced lighting effects requiring normals and tangent space vectors.

## Cross-References
### Incoming
- Rendering subsystem (uses `Create()` for shader instantiation)
- Material/asset management (calls `Get_Texture_Name()`/`Get_Bump_Map_Name()`)
- Save/load system (invokes `Save()`/`Load()` during serialization)

### Outgoing
- Base shader class (`ShdDefClass`) for inheritance
- Serialization system (`ChunkSaveClass`/`ChunkLoadClass`)
- Math utilities (`Vector3`/`Vector2` for material properties)

## Design Patterns
- **Factory Method**: `Create()` generates shader instances
- **Composite**: Extends `ShdDefClass` hierarchy for shader specialization
- **Property Bag**: Encapsulates material parameters (ambient/diffuse/specular) with getter/setter pairs

*Not inferable*: No clear Observer or Strategy patterns visible in header.
