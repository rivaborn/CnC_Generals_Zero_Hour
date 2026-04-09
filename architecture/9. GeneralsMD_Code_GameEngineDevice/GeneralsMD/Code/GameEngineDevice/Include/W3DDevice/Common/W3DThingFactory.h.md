# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/Common/W3DThingFactory.h

## Purpose
Header defining the W3DThingFactory class, a device-dependent extension of ThingFactory for W3D rendering context.

## Responsibilities
- Provides device-dependent thing factory access
- Handles post-processing of Thing database with device-specific data (e.g., model info)
- Inherits from base ThingFactory class
- Manages W3D-specific thing creation

## Key Types
- W3DThingFactory (Class): Device-dependent thing factory for W3D rendering context

## Key Functions
### W3DThingFactory()
- Purpose: Constructor for W3DThingFactory
- Calls: None

### ~W3DThingFactory()
- Purpose: Destructor for W3DThingFactory
- Calls: None

## Globals
- None

## Dependencies
- `Common/ThingFactory.h` (base class)
- Not inferable external symbols
