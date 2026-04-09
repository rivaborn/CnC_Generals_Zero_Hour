# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DOverlordTankDraw.h

## Purpose
Defines the W3DOverlordTankDraw module for rendering the Overlord tank with special drawing requirements.

## Responsibilities
- Extends W3DTankDraw to handle Overlord-specific rendering
- Manages tread debris and animation parameters
- Provides direct access to the rider model for proper draw order
- Implements custom draw logic for the Overlord tank

## Key Types
- **W3DOverlordTankDrawModuleData (Class)**: Contains Overlord-specific rendering parameters (tread debris names, animation rates)
- **W3DOverlordTankDraw (Class)**: Main module class for Overlord tank rendering
- **W3DOverlordTankDrawMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **W3DOverlordTankDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### W3DOverlordTankDrawModuleData::buildFieldParse
- Purpose: Parses module data from configuration files
- Calls: Not inferable

### W3DOverlordTankDraw::setHidden
- Purpose: Controls visibility of the Overlord tank
- Calls: Not inferable

### W3DOverlordTankDraw::doDrawModule
- Purpose: Handles custom rendering of the Overlord tank
- Calls: Not inferable

## Globals
- None

## Dependencies
- W3DTankDraw.h (base class)
- MultiIniFieldParse (for configuration parsing)
- Memory pool and module macros (internal SAGE engine infrastructure)
