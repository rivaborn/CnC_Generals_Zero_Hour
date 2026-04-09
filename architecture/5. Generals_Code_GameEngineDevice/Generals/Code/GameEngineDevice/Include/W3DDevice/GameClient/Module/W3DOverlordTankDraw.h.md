# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DOverlordTankDraw.h

## Purpose
Defines a specialized tank drawing module for the Overlord unit, handling unique rendering requirements like tread animation and rider visibility.

## Responsibilities
- Extends base tank drawing functionality for Overlord-specific needs
- Manages tread debris and animation parameters
- Handles hidden state and custom drawing logic
- Provides module data parsing and initialization

## Key Types
- **W3DOverlordTankDrawModuleData (Class)**: Stores Overlord-specific tank drawing parameters (tread debris names, animation rates)
- **W3DOverlordTankDraw (Class)**: Specialized tank drawing module for Overlord unit
- **W3DOverlordTankDrawMagicEnum (Enum)**: Not inferable
- **W3DOverlordTankDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### W3DOverlordTankDrawModuleData::buildFieldParse
- Purpose: Parses module data from configuration files
- Calls: Not inferable

### W3DOverlordTankDraw::setHidden
- Purpose: Controls visibility of the Overlord tank
- Calls: Not inferable

### W3DOverlordTankDraw::doDrawModule
- Purpose: Handles custom drawing logic for Overlord tank
- Calls: Not inferable

## Globals
- None

## Dependencies
- W3DTankDraw.h (base class)
- MultiIniFieldParse (for configuration parsing)
- Memory pool and module macros (SAGE engine infrastructure)
