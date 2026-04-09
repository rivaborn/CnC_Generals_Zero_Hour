# GeneralsMD/Code/GameEngine/Include/GameLogic/VictoryConditions.h

## Purpose
Defines the interface for managing multiplayer victory conditions in Command & Conquer Generals.

## Responsibilities
- Declares the `VictoryConditionsInterface` abstract class
- Defines victory condition types via `VictoryType` enum
- Provides global access to victory conditions via `TheVictoryConditions`
- Declares factory function `createVictoryConditions`

## Key Types
- **Player (Class)**: Reference to game player entity
- **VictoryType (Enum)**: Bitfield for victory condition flags
- **VictoryConditionsInterface (Class)**: Abstract interface for victory condition management

## Key Functions
### createVictoryConditions
- Purpose: Factory function to create victory conditions instance
- Calls: Not inferable

## Globals
- **TheVictoryConditions (VictoryConditionsInterface*)**: Global pointer to victory conditions instance

## Dependencies
- `Common/SubsystemInterface.h`
- `Lib/BaseType.h`
- `Player` class (forward declared)
