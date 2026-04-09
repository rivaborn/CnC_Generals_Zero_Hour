# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DGranny.h - Enhanced Analysis

## Architectural Role
This header bridges the SAGE engine's rendering pipeline with the Granny animation system, handling model loading, animation management, and optimized batch rendering of skeletal meshes. It serves as the primary interface between the game's W3D rendering system and the third-party Granny SDK.

## Cross-References
### Incoming
- **Rendering Pipeline**: `RenderInfoClass` consumers (e.g., `W3DDevice`) call `GrannyRenderObjClass::Render`
- **Animation System**: `HAnimManagerClass` derivatives use `GrannyAnimClass` for skeletal animation
- **Resource Management**: `PrototypeClass` factory methods create `GrannyPrototypeClass` instances

### Outgoing
- **Granny SDK**: Direct calls to `granny.h` functions for model/animation loading
- **Rendering Backend**: Uses `DX8VertexBufferClass`/`DX8IndexBufferClass` for hardware acceleration
- **Lighting System**: Integrates with `LightEnvironmentClass` for per-model lighting

## Design Patterns
- **Singleton Pattern**: `TheGrannyRenderObjSystem` manages global Granny rendering state
- **Prototype Pattern**: `GrannyPrototypeClass` serves as a blueprint for model instantiation
- **Batch Processing**: `GrannyRenderObjSystem` batches render states to minimize state changes

*Not inferable*: Exact implementation of `GrannyRenderObjSystem`'s batching strategy (e.g., sorting criteria).
