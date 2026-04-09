# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DModelDraw.h

## Purpose
Header file defining the W3DModelDraw class and related structures for 3D model rendering in the SAGE engine.

## Responsibilities
- Defines model rendering infrastructure (animations, transitions, particle systems)
- Manages model states, conditions, and weapon effects
- Handles shadows, terrain decals, and LOD management
- Provides bone transformation and projectile launch offset calculations

## Key Types
- **W3DModelDraw (Class)**: Main model rendering module handling animations, states, and effects
- **ModelConditionInfo (Class)**: Contains model state information (animations, turrets, weapon barrels)
- **W3DAnimationInfo (Class)**: Stores animation metadata (name, duration, distance covered)
- **WeaponRecoilInfo (Class)**: Tracks weapon recoil state and physics
- **GameLODLevel (Enum)**: Defines level-of-detail states

## Key Functions
### buildTransitionSig
- Purpose: Creates a transition signature from source and destination state keys
- Calls: None

### recoverSrcState
- Purpose: Extracts source state from transition signature
- Calls: None

### recoverDstState
- Purpose: Extracts destination state from transition signature
- Calls: None

## Globals
- **NO_TRANSITION (TransitionSig)**: Constant for no-transition state

## Dependencies
- Common/ModelState.h, Common/DrawModule.h
- WW3D2/RendObj.h (conditional)
- GameClient/ParticleSys.h
- Common/STLTypedefs.h
