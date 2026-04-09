# Generals/Code/GameEngine/Source/Common/RTS/ActionManager.cpp

## Purpose
This file contains the implementation of `ActionManager`, a class responsible for managing various actions and queries related to game objects, such as repairing, healing, docking, and using special powers.

## Responsibilities
- Manage logical queries about what objects can do in the world.
- Validate commands for user interface and network interfaces.
- Assist in determining legality of actions based on relationships, health status, and other conditions.

## Key Types
- None

## Key Functions
### appearsToContainFriendlies
- Purpose: Check if an object contains friendly units that are not visible due to stealth.
- Calls: `getContain`, `getApparentControllingPlayer`, `getTeam`

### isObjectShroudedForAction
- Purpose: Determine if a target object is shrouded for action based on player type and command source.
- Calls: `getControllingPlayer`, `getPlayerType`, `getShroudedStatus`

### canGetRepairedAt
- Purpose: Check if an object can be repaired at a specified destination.
- Calls: `getRelationship`, `isEffectivelyDead`, `getStatusBits`, `getBodyModule`, `isAboveTerrain`, `isKindOf`, `isObjectShroudedForAction`

### canTransferSuppliesAt
- Purpose: Check if an object can transfer supplies to a specified destination.
- Calls: `isEffectivelyDead`, `getStatusBits`, `getAI`, `getSupplyTruckAIInterface`, `findUpdateModule`, `getBoxesStored`, `getRelationship`, `isAvailableForSupplying`

### canDockAt
- Purpose: Check if an object can dock at a specified destination.
- Calls: `getBehaviorModules`, `getDockUpdateInterface`, `canTransferSuppliesAt`, `findUpdateModule`

### canGetHealedAt
- Purpose: Check if an object can be healed at a specified destination.
- Calls: `getRelationship`, `isEffectivelyDead`, `getStatusBits`, `getBodyModule`, `isObjectShroudedForAction`

### canRepairObject
- Purpose: Check if an object can repair another object.
- Calls: `getRelationship`, `isEffectivelyDead`, `getStatusBits`, `hasSpecialPower`, `findSpecialAbilityUpdate`, `estimateWeaponDamage`

### canDoSpecialPower
- Purpose: Check if an object can perform a special power.
- Calls: `hasSpecialPower`, `getPercentReady`, `getSpecialPowerType`

### canFireWeaponAtLocation
- Purpose: Check if an object can fire a weapon at a location.
- Calls: `getWeaponInWeaponSlot`

### canFireWeaponAtObject
- Purpose: Check if an object can fire a weapon at another object.
- Calls: `getWeaponInWeaponSlot`, `getAbleToAttackSpecificObject`, `estimateWeaponDamage`

### canFireWeapon
- Purpose: Check if an object can fire a weapon.
- Calls: `getWeaponInWeaponSlot`

### canGarrison
- Purpose: Check if an object can garrison another object.
- Calls: `isKindOf`, `getContain`, `isValidContainerFor`

### canPlayerGarrison
- Purpose: Check if a player can garrison an object.
- Calls: `isEffectivelyDead`, `isKindOf`, `getContain`, `isValidContainerFor`

### canOverrideSpecialPowerDestination
- Purpose: Check if an object can override the destination of a special power.
- Calls: `findSpecialPowerWithOverridableDestinationActive`, `getShroudStatusForPlayer`

## Globals
- TheActionManager (ActionManager*): Singleton instance of ActionManager.

## Dependencies
- Key includes:
  - "Common/ActionManager.h"
  - "Common/GlobalData.h"
  - "Common/Player.h"
