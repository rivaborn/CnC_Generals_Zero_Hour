# GeneralsMD/Code/GameEngine/Include/GameLogic/Powers.h

## Purpose
Defines unit power types and their bit flags for the game engine.

## Responsibilities
- Declares an enum for unit power types
- Provides bit flags for each power
- Defines power names (when `DEFINE_POWER_NAMES` is set)
- Serves as a header for power-related functionality

## Key Types
- (anonymous enum) (Enum): Bit flags for unit powers
  - POWER_NONE: No power
  - POWER_FASTER: Speed boost power
  - POWER_DOUBLE_SHOT: Double damage power
  - POWER_SELF_HEALING: Regeneration power
  - POWERS_NUM_POWERS: Count of defined powers

## Key Functions
None

## Globals
- PowerNames (char*): Array of power name strings (conditionally defined)

## Dependencies
- None (header-only file)
