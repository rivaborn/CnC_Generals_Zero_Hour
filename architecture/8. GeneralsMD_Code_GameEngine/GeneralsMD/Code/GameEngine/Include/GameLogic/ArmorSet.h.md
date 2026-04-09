# GeneralsMD/Code/GameEngine/Include/GameLogic/ArmorSet.h

## Purpose
Defines data structures for armor templates and their conditions in the game's damage system.

## Responsibilities
- Declares `ArmorTemplateSet` class for managing armor templates and damage effects
- Defines `ArmorSetType` enum for armor condition flags
- Provides `ArmorTemplateSetFinder` for sparse matching of armor conditions
- Includes parsing functionality for INI configuration

## Key Types
- **ArmorSetType (Enum)**: Armor condition flags (veteran, elite, hero, etc.)
- **ArmorSetFlags (Class)**: Bitflag wrapper for armor conditions
- **ArmorTemplateSet (Class)**: Stores armor template, damage FX, and condition flags
- **ArmorTemplateSetVector (Class)**: Vector of armor template sets
- **ArmorTemplateSetFinder (Class)**: Sparse match finder for armor conditions

## Key Functions
### ArmorTemplateSet::parseArmorTemplateSet
- Purpose: Parses armor template data from INI file
- Calls: Not inferable (implementation in separate file)

## Globals
- None

## Dependencies
- `ArmorTemplate` (forward declared)
- `DamageFX` (forward declared)
- `INI` (forward declared)
- `BitFlags`, `AsciiString` from game framework
- `SparseMatchFinder` from Common library
