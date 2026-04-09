# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StealthDetectorUpdate.h

## Purpose
Defines a game logic module for detecting stealthed units, including configuration data and update behavior.

## Responsibilities
- Manages stealth detection logic for units
- Handles particle effects and audio cues for detection
- Provides configuration for detection range and update rate
- Supports kind-of filtering for detection targets
- Controls detection while garrisoned/transported

## Key Types
- **StealthDetectorUpdateModuleData (Class)**: Configuration data for stealth detection parameters
- **StealthDetectorUpdate (Class)**: Update module that implements stealth detection logic
- **StealthDetectorUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game object base class

## Key Functions
### StealthDetectorUpdateModuleData::buildFieldParse
- Purpose: Parses configuration data from game files
- Calls: Not inferable (MultiIniFieldParse methods)

### StealthDetectorUpdate::setSDEnabled
- Purpose: Enables/disables the stealth detector
- Calls: Not inferable

### StealthDetectorUpdate::update
- Purpose: Performs stealth detection logic on each update cycle
- Calls: Not inferable

### StealthDetectorUpdate::getDisabledTypesToProcess
- Purpose: Returns which disabled types this module should process
- Calls: Not inferable

## Globals
- None

## Dependencies
- `UpdateModule.h` (base class)
- `MultiIniFieldParse` (for configuration parsing)
- `Thing` (game object base class)
- `UpdateModuleData` (base configuration class)
- `AudioEventRTS`, `ParticleSystemTemplate`, `AsciiString`, `KindOfMaskType` (game framework types)
