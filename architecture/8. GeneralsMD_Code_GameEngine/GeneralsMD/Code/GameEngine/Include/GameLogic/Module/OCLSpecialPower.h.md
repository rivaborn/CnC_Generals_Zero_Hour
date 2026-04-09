# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/OCLSpecialPower.h

## Purpose
Defines the OCLSpecialPower module for handling special abilities that create objects via ObjectCreationLists.

## Responsibilities
- Manages special power logic tied to object creation lists
- Handles placement of created objects (edge/location-based)
- Supports science upgrades for special powers
- Provides reference to final product for placement calculations

## Key Types
- **OCLCreateLocType (Enum)**: Specifies where objects should be created (edge near source/target, location, etc.)
- **OCLSpecialPowerModuleData (Class)**: Contains configuration data for the special power module
- **OCLSpecialPower (Class)**: Implements the special power module behavior

## Key Functions
### OCLSpecialPower::doSpecialPower
- Purpose: Executes the special power with given command options
- Calls: findOCL()

### OCLSpecialPower::doSpecialPowerAtObject
- Purpose: Executes the special power targeting a specific object
- Calls: Not inferable

### OCLSpecialPower::doSpecialPowerAtLocation
- Purpose: Executes the special power at a specific location
- Calls: Not inferable

### OCLSpecialPower::getReferenceThingTemplate
- Purpose: Returns the final product template for placement calculations
- Calls: Not inferable

### OCLSpecialPower::findOCL
- Purpose: Locates the appropriate ObjectCreationList to use
- Calls: Not inferable

## Globals
- None

## Dependencies
- SpecialPowerModule.h
- Science.h
- ObjectCreationList (forward reference)
