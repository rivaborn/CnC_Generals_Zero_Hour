# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/HiveStructureBody.cpp - Enhanced Analysis

## Architectural Role
This file implements the damage propagation logic for "hive" structures (e.g., China's Hive in Zero Hour), which redirect damage to slave units or absorb it if no slaves are present. It bridges the damage system with the spawn/containment systems, demonstrating the engine's modular object composition.

## Cross-References
### Incoming
- Damage system calls `attemptDamage` when damage is applied to hive structures
- Serialization system calls `crc`, `xfer`, and `loadPostProcess` for network sync
- Object initialization calls `loadPostProcess` during template loading

### Outgoing
- Calls into `SpawnBehavior` and `ContainModule` interfaces to locate slave/rider targets
- Delegates to parent `StructureBody` for non-propagated damage
- Uses `GameLogic` singleton to resolve object IDs

## Design Patterns
- **Strategy Pattern**: Damage handling behavior varies based on damage type flags (propagate/swallow)
- **Template Method**: Extends parent class methods while preserving base behavior
- **Dependency Injection**: Module data is injected via constructor, enabling runtime configuration
