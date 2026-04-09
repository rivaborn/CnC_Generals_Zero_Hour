# GeneralsMD/Code/GameEngine/Include/Common/SpecialPowerType.h

## Purpose
Defines an enumeration of special power types used in the game, including superweapons and special abilities.

## Responsibilities
- Declares the `SpecialPowerType` enum with all valid special power identifiers
- Ensures backward compatibility by preserving enum values for save files
- Groups related powers (superweapons, special abilities, faction-specific variants)
- Provides a count of total special powers via `SPECIALPOWER_COUNT`

## Key Types
- SpecialPowerType (Enum): enumerates all special power types in the game
- SPECIAL_INVALID (Enum): invalid/placeholder special power value
- SPECIALPOWER_COUNT (Enum): total count of special power types

## Key Functions
None

## Globals
None

## Dependencies
- SpecialPowerMaskType (referenced in comments but not defined here)
- SpecialPower.cpp (where string definitions are located)
