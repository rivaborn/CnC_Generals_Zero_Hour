# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PrisonBehavior.h

## Purpose
Defines the PrisonBehavior module for managing prisoner containment and visualization in the game.

## Responsibilities
- Manages prisoner containment within a structure
- Handles prisoner visualization in prison yards
- Provides module data for configuration
- Implements containment behavior for prisoners

## Key Types
- PrisonBehaviorModuleData (Class): Module data for prison configuration
- PrisonBehavior (Class): Main prison behavior class handling containment and visualization

## Key Functions
### PrisonBehavior::onContaining
- Purpose: Handles when an object is contained
- Calls: addVisual

### PrisonBehavior::onRemoving
- Purpose: Handles when an object is removed from containment
- Calls: removeVisual

### PrisonBehavior::pickVisualLocation
- Purpose: Selects a location inside the prison yard for visualization

### PrisonBehavior::addVisual
- Purpose: Adds prisoner visual representation

### PrisonBehavior::removeVisual
- Purpose: Removes prisoner visual representation

## Globals
- None

## Dependencies
- OpenContain.h (include)
- MultiIniFieldParse (external)
- PrisonVisual (forward reference)
- Thing (forward reference)
- Object (forward reference)
- Coord3D (forward reference)
- AsciiString (forward reference)
