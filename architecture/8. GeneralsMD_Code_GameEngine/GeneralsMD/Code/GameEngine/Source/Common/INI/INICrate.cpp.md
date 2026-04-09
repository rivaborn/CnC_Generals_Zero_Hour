# GeneralsMD/Code/GameEngine/Source/Common/INI/INICrate.cpp

## Purpose
Handles parsing of crate template definitions from INI files by delegating to the CrateSystem.

## Responsibilities
- Parses crate template definitions from INI files
- Delegates parsing logic to CrateSystem
- Provides public interface for INI parsing

## Key Types
- None

## Key Functions
### parseCrateTemplateDefinition
- Purpose: Parses crate template definitions from an INI file
- Calls: CrateSystem::parseCrateTemplateDefinition

## Globals
- None

## Dependencies
- INI.h
- GameLogic/CrateSystem.h
- PreRTS.h
