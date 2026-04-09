# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DDisplayString.h

## Purpose
Defines the W3DDisplayString class for rendering Unicode text in the W3D engine.

## Responsibilities
- Manage text rendering with fonts, colors, and clipping
- Handle text changes and resource tracking
- Support word wrapping and hotkey display
- Compute text extents for layout

## Key Types
- **W3DDisplayString (Class)**: Unicode text rendering with W3D-specific features
- **W3DDisplayStringManager (Class)**: Friend class (not defined here)
- **W3DDisplayStringMagicEnum (Enum)**: Not inferable
- **W3DDisplayString_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### W3DDisplayString::notifyTextChanged
- Purpose: Updates internal state when text content changes
- Calls: Not inferable

### W3DDisplayString::draw
- Purpose: Renders text at specified position with optional drop shadow
- Calls: Not inferable

### W3DDisplayString::getSize
- Purpose: Retrieves rendered text dimensions
- Calls: Not inferable

### W3DDisplayString::computeExtents
- Purpose: Calculates text width and height
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/GameMemory.h`
- `GameClient/DisplayString.h`
- `WW3D2/Render2DSentence.h`
- `Render2DSentenceClass` (external)
- `DisplayString` (base class)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
