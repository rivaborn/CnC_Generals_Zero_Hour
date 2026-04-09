# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/AutoHealBehavior.cpp

## Purpose
Implements auto-healing behavior for game objects, including self-healing, healing allies in range, or healing all friendly units.

## Responsibilities
- Manages healing logic for objects (self, radius-based, or player-wide)
- Handles particle effects for healing visuals
- Processes damage events to trigger healing
- Filters valid targets based on kind-of masks and health status
- Integrates with game update and upgrade systems

## Key Types
- **AutoHealPlayerScanHelper (struct)**: Helper struct for iterating player objects during healing scans
- **AutoHealBehavior (class)**: Main behavior class handling healing logic

## Key Functions
### checkForAutoHeal
- Purpose: Callback for filtering objects during player-wide healing scans
- Calls: None (pure filter logic)

### AutoHealBehavior::update
- Purpose: Main update loop for healing behavior
- Calls: pulseHealObject, iterateObjects, first/next on ObjectIterator

### AutoHealBehavior::pulseHealObject
- Purpose: Applies healing to a target object and spawns effects
- Calls: attemptHealing/attemptHealingFromSoleBenefactor, createParticleSystem

### AutoHealBehavior::onDamage
- Purpose: Handles damage events to reset healing timers
- Calls: setWakeFrame

## Globals
- None

## Dependencies
- Common/Thing.h, Common/ThingTemplate.h, Common/INI.h, Common/Player.h, Common/Xfer.h
- GameClient/ParticleSys.h, GameClient/Anim2D.h, GameClient/InGameUI.h
- GameLogic/Module/AutoHealBehavior.h, GameLogic/Module/BodyModule.h, GameLogic/GameLogic.h, GameLogic/Object.h, GameLogic/PartitionManager.h
