# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/ObjectCreationList.cpp

## Purpose
Handles object creation effects and behaviors in the game, including debris, payload delivery, weapon firing, and attacks.

## Responsibilities
- Defines various "nugget" classes for different creation effects
- Parses INI configurations for object creation lists
- Manages object creation based on game events
- Handles debris generation and disposal logic

## Key Types
- **FireWeaponNugget (Class)**: Fires a weapon at a target
- **AttackNugget (Class)**: Makes an object attack a position
- **DeliverPayloadNugget (Class)**: Delivers payloads (e.g., airstrikes)
- **GenericObjectCreationNugget (Class)**: General-purpose object creation with many options
- **DebrisDisposition (Enum)**: Controls how debris behaves after creation

## Key Functions
### adjustVector
- Purpose: Rotates a vector by a matrix
- Calls: None

### calcRandomForce
- Purpose: Calculates random force vectors for debris
- Calls: None

### parseFrictionPerSec
- Purpose: Parses friction values from INI files
- Calls: None

## Globals
- **TheObjectCreationListStore (ObjectCreationListStore*)**: Global store for object creation lists
- **DebrisDispositionNames (Array)**: Maps debris disposition names to enum values
- **debrisModelNamesGlobalHack (Vector)**: Temporary storage for debris model names

## Dependencies
- Common game systems (INI, Player, ThingTemplate)
- Game logic modules (Object, Weapon, AI)
- Client-side systems (Drawable, FXList)
- Memory management and utility functions
