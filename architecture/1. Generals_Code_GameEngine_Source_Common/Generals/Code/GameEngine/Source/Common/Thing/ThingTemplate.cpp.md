# Generals/Code/GameEngine/Source/Common/Thing/ThingTemplate.cpp

## Purpose
This file contains the implementation of `ThingTemplate`, a class that defines templates for game entities (things) in Command & Conquer Generals. It handles parsing configuration data, managing modules, and providing various utility functions for these templates.

## Responsibilities
- Parse configuration data for thing templates.
- Manage armor, weapon, and module sets.
- Resolve names and dependencies between templates.
- Calculate build costs and times based on player conditions.
- Provide utility functions for checking equivalence and buildability of templates.

## Key Types
- `ThingTemplate`: Manages template data for game entities.
- `ModuleInfo::Nugget`: Stores information about modules associated with a thing template.
- `ArmorTemplateSet`, `WeaponTemplateSet`: Define sets of armor and weapons for templates.

## Key Functions
### parsePrerequisiteUnit
- Purpose: Parses prerequisite unit requirements from configuration.
- Calls: Not inferable.

### parsePrerequisiteScience
- Purpose: Parses prerequisite science requirements from configuration.
- Calls: Not inferable.

### parseArbitraryFXIntoMap
- Purpose: Parses arbitrary effects into a map.
- Calls: Not inferable.

### parseArbitrarySoundsIntoMap
- Purpose: Parses arbitrary sounds into a map.
- Calls: Not inferable.

## Globals
- `USE_EXP_VALUE_FOR_SKILL_VALUE (Int)`: A constant used to indicate that experience value should be used for skill points.

## Dependencies
- Key includes and external symbols:
  - `Common/DamageFX.h`
  - `Common/GameAudio.h`
  - `Common/GlobalData.h`
  - `Common/INI.h`
  - `Common/MessageStream.h`
  - `Common/Module.h`
  - `Common/Player.h`
  - `Common/Radar.h`
  - `GameClient/FXList.h`
  - `GameLogic/Armor.h`
  - `GameLogic/Object.h`
  - `GameLogic/Powers.h`
  - `GameLogic/Weapon.h`
