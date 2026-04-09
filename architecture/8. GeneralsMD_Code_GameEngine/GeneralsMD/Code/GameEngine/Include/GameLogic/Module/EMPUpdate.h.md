# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/EMPUpdate.h

## Purpose
Defines modules for handling EMP (electromagnetic pulse) effects and leaflet drop behavior in the game.

## Responsibilities
- Manages EMP field growth, fading, and disabling effects on objects
- Controls leaflet drop timing and particle effects
- Handles victim targeting based on kind-of masks
- Manages particle system effects for disabled units
- Provides module data parsing from INI files

## Key Types
- **EMPUpdateModuleData (Class)**: Configuration data for EMP effects
- **EMPUpdate (Class)**: Module implementing EMP field behavior
- **LeafletDropBehaviorModuleData (Class)**: Configuration for leaflet drop effects
- **LeafletDropBehavior (Class)**: Module handling leaflet drop timing and effects
- **EMPUpdateMagicEnum (Enum)**: Not inferable
- **LeafletDropBehaviorMagicEnum (Enum)**: Not inferable

## Key Functions
### EMPUpdateModuleData::buildFieldParse
- Purpose: Parses INI configuration for EMP module data
- Calls: UpdateModuleData::buildFieldParse

### LeafletDropBehaviorModuleData::buildFieldParse
- Purpose: Parses INI configuration for leaflet drop module data
- Calls: UpdateModuleData::buildFieldParse

### EMPUpdate::update
- Purpose: Updates EMP field state each frame
- Calls: Not inferable

### LeafletDropBehavior::update
- Purpose: Updates leaflet drop state each frame
- Calls: Not inferable

### EMPUpdate::doDisableAttack
- Purpose: Disables attacks for affected units
- Calls: Not inferable

### LeafletDropBehavior::doDisableAttack
- Purpose: Disables attacks for affected units during leaflet drop
- Calls: Not inferable

## Globals
- None

## Dependencies
- UpdateModule.h
- DieModule.h
- GameLogic/Weapon.h
- MultiIniFieldParse
- INI parsing utilities
- ParticleSystemTemplate
- RGBColor
- KindOfMaskType
