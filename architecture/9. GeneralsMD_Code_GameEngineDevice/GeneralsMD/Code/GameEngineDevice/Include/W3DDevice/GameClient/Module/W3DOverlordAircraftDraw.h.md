# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DOverlordAircraftDraw.h

## Purpose
Defines a module for drawing aircraft units that receive portable structure upgrades, ensuring the rider is drawn after the aircraft.

## Responsibilities
- Extends `W3DModelDraw` to handle aircraft-specific drawing logic
- Manages module data for configuration
- Provides virtual methods for hiding and drawing the module
- Uses memory pool allocation for object management

## Key Types
- **W3DOverlordAircraftDrawModuleData (Class)**: Module data for configuration
- **W3DOverlordAircraftDraw (Class)**: Main aircraft draw module class
- **W3DOverlordAircraftDrawMagicEnum (Enum)**: Not inferable (likely unused placeholder)
- **W3DOverlordAircraftDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder)

## Key Functions
### W3DOverlordAircraftDrawModuleData()
- Purpose: Constructor for module data.
- Calls: None

### W3DOverlordAircraftDrawModuleData::~W3DOverlordAircraftDrawModuleData()
- Purpose: Destructor for module data.
- Calls: None

### W3DOverlordAircraftDrawModuleData::buildFieldParse()
- Purpose: Parses configuration fields for the module.
- Calls: None

### W3DOverlordAircraftDraw::W3DOverlordAircraftDraw()
- Purpose: Constructor for the aircraft draw module.
- Calls: None

### W3DOverlordAircraftDraw::setHidden()
- Purpose: Sets the hidden state of the module.
- Calls: None

### W3DOverlordAircraftDraw::doDrawModule()
- Purpose: Handles the drawing logic for the aircraft.
- Calls: None

## Globals
