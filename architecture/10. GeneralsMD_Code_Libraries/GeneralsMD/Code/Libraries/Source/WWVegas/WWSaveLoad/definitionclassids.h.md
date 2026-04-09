# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/definitionclassids.h

## Purpose
Defines class IDs for game object definitions and provides a function to determine super-class IDs.

## Responsibilities
- Defines an enum of class IDs for various game object types
- Provides a function to map class IDs to super-class IDs
- Establishes constants for class ID ranges

## Key Types
- (anonymous enum) (Enum): Contains all class IDs for game definitions
- CLASSID_TERRAIN (Enum): ID for terrain definitions
- CLASSID_TILE (Enum): ID for tile definitions
- CLASSID_GAME_OBJECTS (Enum): ID for game object definitions
- CLASSID_LIGHT (Enum): ID for light definitions
- CLASSID_SOUND (Enum): ID for sound definitions
- CLASSID_WAYPATH (Enum): ID for waypath definitions
- CLASSID_ZONE (Enum): ID for zone definitions
- CLASSID_TRANSITION (Enum): ID for transition definitions
- CLASSID_PHYSICS (Enum): ID for physics definitions
- CLASSID_EDITOR_OBJECTS (Enum): ID for editor object definitions
- CLASSID_MUNITIONS (Enum): ID for munition definitions
- CLASSID_DUMMY_OBJECTS (Enum): ID for dummy object definitions
- CLASSID_BUILDINGS (Enum): ID for building definitions
- CLASSID_TWIDDLERS (Enum): ID for twiddler definitions
- CLASSID_GLOBAL_SETTINGS (Enum): ID for global settings definitions

## Key Functions
### SuperClassID_From_ClassID
- Purpose: Determines which super-class a given class ID belongs to
- Calls: None

## Globals
- DEF_CLASSID_START (int): Starting value for class ID ranges
- DEF_CLASSID_RANGE (int): Size of each class ID range

##
