# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BoneFXUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the BoneFXUpdate module, which manages skeletal bone-attached visual effects (FX lists, object creation lists, and particle systems) in the SAGE engine. It bridges the animation system (bone resolution) with the visual effects system, allowing effects to be dynamically attached to specific bones and triggered based on damage states.

## Cross-References
### Incoming
- **BodyModule**: Likely calls `changeBodyDamageState` when damage states change
- **DamageModule**: May trigger effects via damage events (implied by `DamageTypeFlags`)
- **Thing-derived classes**: Use this module for bone-attached effects

### Outgoing
- **GameClient/ParticleSys.h**: Uses particle system APIs for effect creation/destruction
- **FXList/OCL systems**: Triggers effects at resolved bone positions
- **W3D rendering system**: Indirectly via particle system and FX list execution

## Design Patterns
- **Strategy Pattern**: Different effect types (FXList, OCL, ParticleSystem) are handled via specialized methods (`doFXListAtBone`, `doOCLAtBone`, etc.)
- **State Pattern**: Effect behavior changes based on `BodyDamageType` (Pristine/Damaged/ReallyDamaged/Rubble)
- **Observer Pattern**: Module reacts to body state changes via `changeBodyDamageState`

**Key Insight**: The module's design allows modders to configure bone-attached effects entirely via INI files, enabling extensive visual customization without code changes. The `BONE_FX_MAX_BONES` limit (8) suggests a performance optimization to cap per-state effects.
