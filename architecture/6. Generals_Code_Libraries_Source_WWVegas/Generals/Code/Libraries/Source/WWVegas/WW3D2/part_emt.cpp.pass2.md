# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_emt.cpp - Enhanced Analysis

## Architectural Role
Core particle system component in the WW3D2 rendering pipeline, bridging between high-level emitter definitions and low-level particle buffer management. Acts as an intermediary between scene management and particle rendering systems.

## Cross-References
### Incoming
- `SceneClass` (calls `Update_On_Visibilty` for visibility-driven emission control)
- `WW3DAssetManager` (uses `Create_From_Definition` for asset instantiation)
- `ParticleLoaderClass` (likely calls `Save` for serialization)

### Outgoing
- `ParticleBufferClass` (delegates particle storage/rendering)
- `TextureClass`/`ShaderClass` (for material properties)
- `Vector3Randomizer` (for procedural variation)

## Design Patterns
- **Factory Method**: `Create_From_Definition` creates emitters from serialized data
- **Composite**: Emitter manages collection of particles via `ParticleBufferClass`
- **Observer**: Reacts to visibility changes via `Update_On_Visibilty`

*Not inferable*: Exact relationship with `W3D::Get_Frame_Time` timing mechanism.
