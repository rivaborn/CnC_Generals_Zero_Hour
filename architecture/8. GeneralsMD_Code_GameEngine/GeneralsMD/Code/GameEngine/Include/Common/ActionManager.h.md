# GeneralsMD/Code/GameEngine/Include/Common/ActionManager.h

## Purpose
Header for the ActionManager class, which centralizes logical queries about object interactions in the game world.

## Responsibilities
- Provides methods to check if objects can perform actions (e.g., repair, attack, capture).
- Validates commands for UI and network input.
- Manages special power and weapon usage checks.
- Handles player-to-unit interaction checks.

## Key Types
- **ActionManager (Class)**: Centralizes action validation logic.
- **CanEnterType (Enum)**: Defines entry check modes (capacity, combat drop).
- **CanAttackResult (Enum)**: Result of attack feasibility checks.
- **SpecialPowerType (Enum)**: Types of special powers.
- **WeaponSlotType (Enum)**: Weapon slot identifiers.
- **CommandSourceType (Enum)**: Source of commands (e.g., player, AI).

## Key Functions
### `canFireWeapon`
- Purpose: Checks if an object can fire a weapon.
- Calls: None (declaration only).

### `canDoSpecialPower`
- Purpose: Validates if an object can use a special power.
- Calls: None (declaration only).

### `canCaptureBuilding`
- Purpose: Checks if an object can capture a building.
- Calls: None (declaration only).

## Globals
- **TheActionManager (ActionManager*)**: Global instance of the ActionManager.

## Dependencies
- **SubsystemInterface.h**: Base class for subsystems.
- Forward declarations: `Object`, `Player`, `SpecialPowerTemplate`, enums (`SpecialPowerType`, `WeaponSlotType`, `CommandSourceType`, `CanAttackResult`).
