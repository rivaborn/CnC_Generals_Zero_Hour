# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PointDefenseLaserUpdate.h

## Purpose
Defines the PointDefenseLaserUpdate module for handling independent targeting of point defense lasers in the game.

## Responsibilities
- Manages laser targeting logic for point defense systems
- Scans for closest targets within range
- Handles firing timing and availability
- Maintains target tracking state

## Key Types
- **PointDefenseLaserUpdateModuleData (Class)**: Contains configuration data for the laser update module
- **PointDefenseLaserUpdate (Class)**: The main update module class that handles laser targeting
- **PointDefenseLaserUpdateMagicEnum (Enum)**: Not inferable (likely internal enum)
- **PointDefenseLaserUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal enum)

## Key Functions
### PointDefenseLaserUpdateModuleData::buildFieldParse
- Purpose: Parses configuration data from ini files
- Calls: Not inferable

### PointDefenseLaserUpdate::onObjectCreated
- Purpose: Initializes the module when attached to an object
- Calls: Not inferable

### PointDefenseLaserUpdate::update
- Purpose: Main update loop for the laser targeting system
- Calls: scanClosestTarget, fireWhenReady

### PointDefenseLaserUpdate::scanClosestTarget
- Purpose: Finds the closest valid target within scan range
- Calls: Not inferable

### PointDefenseLaserUpdate::fireWhenReady
- Purpose: Handles firing logic when target is available
- Calls: Not inferable

## Globals
None

## Dependencies
- Common/KindOf.h
- GameLogic/Module/UpdateModule.h
- ThingTemplate, WeaponTemplate (forward references)
