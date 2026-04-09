# Generals/Code/Libraries/Source/WWVegas/WWLib/blitblit.h

## Purpose
Defines pixel blitting operations for the SAGE engine, supporting various pixel formats and effects.

## Responsibilities
- Provides templated blitter classes for different pixel operations
- Supports 8-bit to 16-bit color translation
- Implements transparency handling and special effects (darkening, translucency)
- Includes optimized assembly implementations for key operations
- Handles both forward and backward blitting directions

## Key Types
- BlitPlain (Class): Basic pixel copying without translation
- BlitTrans (Class): Transparency-aware pixel copying
- BlitPlainXlat (Class): 8-bit to T format conversion
- BlitTransXlat (Class): Transparent 8-bit to T format conversion
- BlitTransRemapXlat (Class): Transparent 8-bit with remapping to T format
- BlitTransZRemapXlat (Class): Dynamic remapping version of BlitTransRemapXlat
- BlitTransDarken (Class): Darkens destination pixels based on source
- BlitTransRemapDest (Class): Remaps destination pixels based on source
- BlitDarken (Class): Darkens all destination pixels
- BlitTransLucent50/25/75 (Class): Translucency effects at different levels

## Key Functions
### BlitForward (various classes)
- Purpose: Perform forward pixel blitting operation
- Calls: memcpy/memmove for BlitPlain, custom loops for others

### BlitBackward (various classes)
- Purpose: Perform backward pixel blitting operation
- Calls: Typically delegates to BlitForward

### Assembly implementations (MSVC)
- Purpose: Optimized versions of key blitter operations
- Calls: Inline assembly for direct memory access

## Globals
None

## Dependencies
- blitter.h: Base Blitter class definition
- <assert.h>: For runtime assertions
- <string.h>: For memcpy/memmove functions
