# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DOverlordTruckDraw.h

## Purpose
Defines a specialized truck drawing module for the Overlord unit, ensuring its rider is drawn after the Overlord and providing direct access to the rider.

## Responsibilities
- Extends `W3DTruckDraw` for Overlord-specific rendering
- Manages tread debris and animation parameters
- Handles hidden state and module drawing
- Provides module data parsing and management

## Key Types
- **W3DOverlordTruckDrawModuleData (Class)**: Stores Overlord-specific tread and animation parameters
- **W3DOverlordTruckDraw (Class)**: Main drawing module for Overlord units
- **W3DOverlordTruckDrawMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **W3DOverlordTruckDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### W3DOverlordTruckDrawModuleData::buildFieldParse
- Purpose: Parses module data fields from configuration
- Calls: `MultiIniFieldParse` methods

### W3DOverlordTruckDraw::setHidden
- Purpose: Controls visibility of the Overlord truck
- Calls: Parent class `setHidden`

### W3DOverlordTruckDraw::doDrawModule
- Purpose: Handles the actual drawing of the Overlord truck
- Calls: Not specified in header

## Globals
- None

## Dependencies
- `W3DTruckDraw.h` (parent class)
- `MultiIniFieldParse` (for configuration parsing)
- Memory pool and module macro utilities (internal SAGE framework)
