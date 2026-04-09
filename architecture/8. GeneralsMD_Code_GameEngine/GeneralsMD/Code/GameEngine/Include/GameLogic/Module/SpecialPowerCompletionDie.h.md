# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpecialPowerCompletionDie.h

## Purpose
Defines a die module that notifies the script engine when a special power is completed.

## Responsibilities
- Notifies script engine on unit death
- Stores creator ID for tracking
- Parses INI data for special power template

## Key Types
- **SpecialPowerTemplate (Class)**: Not inferable.
- **SpecialPowerCompletionDieModuleData (Class)**: Holds special power template reference.
- **SpecialPowerCompletionDie (Class)**: Die module for special power completion.
- **SpecialPowerCompletionDieMagicEnum (Enum)**: Not inferable.
- **SpecialPowerCompletionDie_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### SpecialPowerCompletionDieModuleData::buildFieldParse
- Purpose: Registers INI field parsing for module data.
- Calls: `DieModuleData::buildFieldParse`

### SpecialPowerCompletionDie::onDie
- Purpose: Handles unit death and notifies script engine.
- Calls: `notifyScriptEngine`

### SpecialPowerCompletionDie::notifyScriptEngine
- Purpose: Sends completion notification to script engine.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `Common/INI.h`
- `GameLogic/Module/DieModule.h`
- `SpecialPowerTemplate` (forward declared)
