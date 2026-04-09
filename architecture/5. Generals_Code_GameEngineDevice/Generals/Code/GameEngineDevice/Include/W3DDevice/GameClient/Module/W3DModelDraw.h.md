# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DModelDraw.h

## Purpose
Header for the W3DModelDraw module, handling 3D model rendering, animations, and state transitions in the SAGE engine.

## Responsibilities
- Defines data structures for model conditions, animations, and rendering states
- Manages model transitions, particle systems, and weapon recoil
- Provides interfaces for model drawing, bone manipulation, and shadow handling

## Key Types
- **W3DModelDraw (Class)**: Main model drawing module handling rendering and animations
- **ModelConditionInfo (Class)**: Contains model state information including animations, turrets, and weapon barrels
- **W3DAnimationInfo (Class)**: Stores animation metadata and handles
- **WeaponRecoilInfo (Class)**: Tracks weapon recoil state and physics
- **GameLODLevel (Enum)**: Defines level-of-detail states

## Key Functions
### buildTransitionSig
- Purpose: Creates a transition signature from source and destination state names
- Calls: None

### recoverSrcState
- Purpose: Extracts source state from a transition signature
- Calls: None

### recoverDstState
- Purpose: Extracts destination state from a transition signature
- Calls: None

## Globals
- **NO_TRANSITION (TransitionSig)**: Constant for no-transition state

## Dependencies
- Common/ModelState.h
- Common/DrawModule.h
- WW3D2/RendObj.h (conditional)
- GameClient/ParticleSys.h
- Common/STLTypedefs.h
