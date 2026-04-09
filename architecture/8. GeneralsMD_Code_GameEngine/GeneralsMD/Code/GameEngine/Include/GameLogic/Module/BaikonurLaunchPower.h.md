# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BaikonurLaunchPower.h

## Purpose
Defines the BaikonurLaunchPower module, which triggers the GLA end-game launch sequence from the Baikonur launch tower.

## Responsibilities
- Triggers the Baikonur launch tower's end-game sequence
- Provides module data for special power behavior
- Implements special power execution at a location
- Manages detonation object reference

## Key Types
- **BaikonurLaunchPowerModuleData (Class)**: Holds module-specific data including detonation object reference
- **BaikonurLaunchPower (Class)**: Special power module for triggering the launch sequence
- **BaikonurLaunchPowerMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **BaikonurLaunchPower_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### BaikonurLaunchPower::doSpecialPower
- Purpose: Executes the special power with given command options
- Calls: Not inferable

### BaikonurLaunchPower::doSpecialPowerAtLocation
- Purpose: Executes the special power at a specific location with angle and command options
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/Module/SpecialPowerModule.h`
- `Object`, `SpecialPowerTemplate`, `FieldParse`, `ScienceType` (forward declarations)
- `MultiIniFieldParse`, `AsciiString`, `UnsignedInt`, `Real`, `Coord3D`, `Thing`, `ModuleData` (external types)
