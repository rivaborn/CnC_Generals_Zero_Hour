# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/GrantUpgradeCreate.h

## Purpose
Defines a game logic module that grants upgrades to objects upon creation or build completion.

## Responsibilities
- Grants upgrades to objects when created or built
- Handles upgrade name and status exemption logic
- Provides module data parsing and management

## Key Types
- **Thing (Class)**: Base object type in the game.
- **GrantUpgradeCreateModuleData (Class)**: Holds upgrade name and exemption status.
- **GrantUpgradeCreate (Class)**: Main module class that implements upgrade granting.
- **GrantUpgradeCreateMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **GrantUpgradeCreate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### GrantUpgradeCreateModuleData::buildFieldParse
- Purpose: Parses module data from configuration files.
- Calls: Not inferable (likely MultiIniFieldParse methods).

### GrantUpgradeCreate::onCreate
- Purpose: Grants upgrade when object is created.
- Calls: Not inferable.

### GrantUpgradeCreate::onBuildComplete
- Purpose: Grants upgrade when object build is complete.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `CreateModule.h`, `GameLogic/Object.h`, `Common/ObjectStatusTypes.h`
- `AsciiString`, `MultiIniFieldParse`, `ObjectStatusMaskType`
