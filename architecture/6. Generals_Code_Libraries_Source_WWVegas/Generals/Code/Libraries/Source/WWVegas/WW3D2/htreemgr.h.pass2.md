# Generals/Code/Libraries/Source/WWVegas/WW3D2/htreemgr.h - Enhanced Analysis

## Architectural Role
Centralizes management of hierarchy trees (base poses) for W3D models, acting as a registry for model animation data. Critical for model loading/unloading and memory management in the rendering pipeline.

## Cross-References
### Incoming
- Likely called by model loading systems (e.g., `W3DModelClass`) during asset initialization
- Used by animation systems for pose retrieval
- Referenced by level streaming/unloading logic for selective tree unloading

### Outgoing
- Interacts with `ChunkLoadClass` for asset loading
- Manages `HTreeClass` instances
- Uses `W3DExclusionListClass` for memory optimization during level transitions

## Design Patterns
- **Registry Pattern**: Maintains a centralized collection of trees with lookup by name/ID
- **Resource Pool**: Fixed-size array (`TreePtr[MAX_TREES]`) for predictable memory usage (though noted as suboptimal)
- **Exclusion-Based Cleanup**: Supports selective unloading via exclusion lists for memory management

*Not inferable*: No clear use of Factory, Observer, or other patterns from header alone.
