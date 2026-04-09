# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AssistedTargetingUpdate.h

## Purpose
Defines the assisted targeting update module for the game engine, allowing external influences to command attacks beyond normal targeting range.

## Responsibilities
- Manages assisted targeting logic for game objects
- Handles feedback lasers for visual targeting cues
- Provides module data configuration for assisted targeting
- Implements update cycle for assisted targeting behavior
- Checks availability for assistance requests

## Key Types
- **AssistedTargetingUpdateModuleData (Class)**: Stores configuration data for assisted targeting (clip size, weapon slot, laser names)
- **AssistedTargetingUpdate (Class)**: Implements the assisted targeting update module behavior
- **AssistedTargetingUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **AssistedTargetingUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### AssistedTargetingUpdateModuleData()
- Purpose: Default constructor initializing module data fields
- Calls: None

### buildFieldParse()
- Purpose: Static method for parsing module data from configuration files
- Calls: None

### update()
- Purpose: Virtual update method for the module's update cycle
- Calls: Not inferable

### isFreeToAssist()
- Purpose: Checks if the object is available for assistance
- Calls: Not inferable

### assistAttack()
- Purpose: Handles attack assistance requests from other objects
- Calls: Not inferable

### makeFeedbackLaser()
- Purpose: Creates visual laser feedback between assisting and target objects
- Calls: Not inferable

## Globals
- None

## Dependencies
- UpdateModule.h (base class)
- MultiIniFieldParse (for configuration parsing)
- Thing, Object, ThingTemplate (game entity classes)
- AsciiString (string handling
