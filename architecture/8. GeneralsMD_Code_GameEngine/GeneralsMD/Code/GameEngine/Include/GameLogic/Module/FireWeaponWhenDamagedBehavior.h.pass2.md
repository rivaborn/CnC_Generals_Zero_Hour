# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FireWeaponWhenDamagedBehavior.h - Enhanced Analysis

## Architectural Role
This file implements a reactive combat behavior system where objects automatically fire weapons when damaged, integrating tightly with the damage system and upgrade framework. It bridges the gap between damage events and weapon firing logic, with configurable responses for different damage states.

## Cross-References
### Incoming
- Damage system calls `onDamage()` when damage occurs
- Update system calls `update()` for continuous weapon firing
- Upgrade system calls upgrade-related methods during upgrades

### Outgoing
- Calls `Weapon` system to fire weapons
- Uses `UpgradeMux` for upgrade handling
- Accesses `DamageModule` for damage state queries
- Interacts with `UpdateModule` for timing control

## Design Patterns
- **Strategy Pattern**: Different weapon templates for various damage states (pristine, damaged, etc.)
- **Observer Pattern**: Reacts to damage events via `onDamage()` callback
- **Template Method**: `upgradeImplementation()` provides extensible upgrade behavior

Rules followed. Output under 400 tokens.
