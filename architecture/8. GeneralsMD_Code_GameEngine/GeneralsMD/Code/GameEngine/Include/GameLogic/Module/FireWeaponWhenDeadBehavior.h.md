# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FireWeaponWhenDeadBehavior.h

## Purpose
Defines a behavior module that fires a weapon when an object dies.

## Responsibilities
- Fires a specified weapon upon object death
- Manages upgrade activation/deactivation
- Handles die module interface for object death events

## Key Types
- **FireWeaponWhenDeadBehaviorModuleData (Class)**: Holds configuration data for the behavior (upgrade settings, weapon template, etc.)
- **FireWeaponWhenDeadBehavior (Class)**: Implements the behavior that fires a weapon when the object dies
- **FireWeaponWhenDeadBehaviorMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **FireWeaponWhenDeadBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### FireWeaponWhenDeadBehaviorModuleData::buildFieldParse
- Purpose: Registers INI field parsing for module data
- Calls: `BehaviorModuleData::buildFieldParse`, `UpgradeMuxData::getFieldParse`, `DieMuxData::getFieldParse`

### FireWeaponWhenDeadBehavior::onDie
- Purpose: Handles object death event and fires the weapon
- Calls: Not inferable (implementation in .cpp)

### FireWeaponWhenDeadBehavior::upgradeImplementation
- Purpose: Placeholder for upgrade logic (empty implementation)
- Calls: None

### FireWeaponWhenDeadBehavior::getUpgradeActivationMasks
- Purpose: Retrieves upgrade activation/deactivation masks
- Calls: `m_upgradeMuxData.getUpgradeActivationMasks`

## Globals
- None

## Dependencies
- `BehaviorModule.h`, `DieModule.h`, `UpgradeModule.h`
- `MultiIniFieldParse`, `UpgradeMuxData`, `DieMuxData`, `WeaponTemplate`
