# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/DemoralizeSpecialPower.cpp - Enhanced Analysis

## Architectural Role
This file implements the demoralization special power, a game mechanic that temporarily reduces enemy infantry effectiveness. It extends the base `SpecialPowerModule` class and integrates with the AI system, partition manager, and FX system to apply status effects and visual feedback.

## Cross-References
### Incoming
- Called by UI command handlers when player activates demoralize power
- Referenced in modding INI files for special power configuration

### Outgoing
- Uses `SpecialPowerModule` base class methods
- Queries `ContainModuleInterface` for captured unit count
- Applies effects via `AIUpdateInterface::setDemoralized`
- Spawns FX using `FXList::doFXPos`
- Scans objects via `PartitionManager::iterateObjectsInRange`

## Design Patterns
- **Template Method**: Extends base `SpecialPowerModule` with specific demoralize behavior
- **Strategy**: Demoralization effect is applied as a strategy pattern via `AIUpdateInterface`
- **Observer**: FX playback triggers visual feedback without direct coupling
