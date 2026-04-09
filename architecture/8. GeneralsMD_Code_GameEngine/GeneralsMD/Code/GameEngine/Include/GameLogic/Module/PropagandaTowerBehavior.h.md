# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PropagandaTowerBehavior.h

## Purpose
Defines the behavior module for Propaganda Towers, handling scanning, healing effects, and influence management.

## Responsibilities
- Manages propaganda tower scanning and healing effects
- Tracks objects within influence range
- Handles upgrade-dependent effects
- Processes updates even when disabled

## Key Types
- **PropagandaTowerBehaviorModuleData (Class)**: Configuration data for propaganda tower behavior
- **PropagandaTowerBehavior (Class)**: Main behavior module implementing scanning and effect logic
- **PropagandaTowerBehaviorMagicEnum (Enum)**: Not inferable
- **PropagandaTowerBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### PropagandaTowerBehaviorModuleData::buildFieldParse
- Purpose: Parses configuration data from INI files
- Calls: Not inferable

### PropagandaTowerBehavior::update
- Purpose: Handles periodic scanning and effect updates
- Calls: doScan, effectLogic

### PropagandaTowerBehavior::onDie
- Purpose: Cleans up when the tower is destroyed
- Calls: removeAllInfluence

### PropagandaTowerBehavior::onCapture
- Purpose: Handles ownership change of the tower
- Calls: removeAllInfluence

### PropagandaTowerBehavior::doScan
- Purpose: Scans for objects within influence range
- Calls: Not inferable

### PropagandaTowerBehavior::effectLogic
- Purpose: Applies/removes healing effects on objects
- Calls: Not inferable

## Globals
None

## Dependencies
- BehaviorModule.h, UpdateModule.h, DieModule.h
- ObjectTracker, FXList, UpgradeTemplate (forward references)
