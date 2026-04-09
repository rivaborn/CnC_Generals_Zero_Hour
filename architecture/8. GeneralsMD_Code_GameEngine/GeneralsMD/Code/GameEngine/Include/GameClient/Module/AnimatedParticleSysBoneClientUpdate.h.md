# GeneralsMD/Code/GameEngine/Include/GameClient/Module/AnimatedParticleSysBoneClientUpdate.h

## Purpose
Defines a client update module for translating particle systems with animation.

## Responsibilities
- Manages client-side updates for animated particle systems attached to bones
- Handles lifecycle via `m_life` counter
- Implements `ClientUpdateModule` interface
- Provides memory pool and module macros for SAGE engine integration

## Key Types
- **AnimatedParticleSysBoneClientUpdate (Class)**: Client update module for bone-attached particle systems
- **Thing (Class)**: Forward reference to game object this module attaches to
- **AnimatedParticleSysBoneClientUpdateMagicEnum (Enum)**: Not inferable
- **AnimatedParticleSysBoneClientUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### AnimatedParticleSysBoneClientUpdate()
- Purpose: Constructor initializing the module
- Calls: Not inferable

### clientUpdate()
- Purpose: Updates particle system position based on bone animation
- Calls: Not inferable

### MAKE_STANDARD_MODULE_MACRO functions
- Purpose: SAGE engine module registration macros
- Calls: Not inferable

## Globals
- **None**

## Dependencies
- `Common/ClientUpdateModule.h`
- `Thing` class (forward declared)
- SAGE engine memory pool and module macros
