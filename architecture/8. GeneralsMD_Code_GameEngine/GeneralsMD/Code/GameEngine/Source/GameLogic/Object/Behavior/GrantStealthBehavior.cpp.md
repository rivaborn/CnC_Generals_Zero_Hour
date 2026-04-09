# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/GrantStealthBehavior.cpp

## Purpose
Implements behavior for granting stealth to nearby objects, including particle effects and scan logic.

## Responsibilities
- Manages stealth granting via radius-based scanning
- Handles particle system for visual feedback
- Processes object filtering and stealth application
- Self-destructs after final scan completes

## Key Types
- **GrantStealthPlayerScanHelper (struct)**: Helper struct for object scanning with kind-of mask and grantor reference
- **GrantStealthBehavior (class)**: Main behavior class handling stealth granting logic

## Key Functions
### checkForGrantStealth
- Purpose: Callback for filtering and collecting objects eligible for stealth granting
- Calls: `testObj->isEffectivelyDead()`, `testObj->getControllingPlayer()`, `testObj->isOffMap()`, `testObj->isAnyKindOf()`, `testObj->getContain()`, `testObj->getContain()->friend_getRider()`

### GrantStealthBehavior::update
- Purpose: Main update loop that grows scan radius and applies stealth
- Calls: `ThePartitionManager->iterateObjectsInRange()`, `grantStealthToObject()`, `TheGameLogic->destroyObject()`

### GrantStealthBehavior::grantStealthToObject
- Purpose: Applies stealth effect to a specific object
- Calls: `obj->isAnyKindOf()`, `obj->getStealth()`, `stealth->receiveGrant()`, `obj->getDrawable()`, `draw->flashAsSelected()`

## Globals
- None

## Dependencies
- `Thing`, `ThingTemplate`, `INI`, `Player`, `Xfer`, `ParticleSys`, `Anim2D`, `InGameUI`, `ContainModule`, `GrantStealthBehavior`, `StealthUpdate`, `BodyModule`, `GameLogic`, `Object`, `PartitionManager`
