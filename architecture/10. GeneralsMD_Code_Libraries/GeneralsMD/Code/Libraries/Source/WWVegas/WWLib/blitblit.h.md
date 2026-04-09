# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blitblit.h

## Purpose
Defines pixel blitter classes for various rendering operations in the SAGE engine, supporting both 8-bit and 16-bit pixel formats.

## Responsibilities
- Provides templated blitter classes for different pixel operations (plain, transparent, translucent, remapped, darkened)
- Supports color translation between 8-bit and 16-bit formats
- Includes optimized assembly implementations for key operations
- Handles both forward and backward blitting directions

## Key Types
- BlitPlain (Class): Plain pixel copying without translation
- BlitTrans (Class): Transparent pixel copying
- BlitPlainXlat (Class): 8-bit to T format conversion
- BlitTransXlat (Class): Transparent 8-bit to T format conversion
- BlitTransRemapXlat (Class): Transparent 8-bit to T with remapping
- BlitTransZRemapXlat (Class): Transparent 8-bit to T with dynamic remapping
- BlitTransDarken (Class): Darkening effect with transparency
- BlitTransRemapDest (Class): Remap destination pixels based on source
- BlitDarken (Class): Darken all destination pixels
- BlitTransLucent50/25/75 (Class): Translucency effects (50%, 25%, 75%)

## Key Functions
### BlitForward/BlitBackward (all classes)
- Purpose: Perform pixel blitting in forward or backward direction
- Calls: memcpy/memmove (BlitPlain), direct pixel operations (others)

## Globals
None

## Dependencies
- blitter.h (base Blitter class)
- <assert.h>, <string.h> (standard C headers)
- _MSC_VER (for assembly implementations)
