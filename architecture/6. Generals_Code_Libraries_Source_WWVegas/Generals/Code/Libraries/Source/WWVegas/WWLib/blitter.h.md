# Generals/Code/Libraries/Source/WWVegas/WWLib/blitter.h

## Purpose
Defines abstract interfaces for pixel blitting operations, including standard and RLE-compressed data handling.

## Responsibilities
- Declares base `Blitter` class for pixel copying
- Declares `RLEBlitter` class for RLE-compressed data handling
- Provides virtual methods for forward/backward blitting
- Includes overlap-safe blitting logic

## Key Types
- **Blitter (Class)**: Abstract base for pixel blitting operations
- **RLEBlitter (Class)**: Abstract base for RLE-compressed pixel blitting

## Key Functions
### Blitter::BlitForward
- Purpose: Virtual method for forward pixel copying
- Calls: None (pure virtual)

### Blitter::BlitBackward
- Purpose: Virtual method for backward pixel copying (for overlapping regions)
- Calls: None (pure virtual)

### Blitter::Blit
- Purpose: Wrapper that selects forward/backward blitting based on memory overlap
- Calls: `BlitForward`, `BlitBackward`

### RLEBlitter::Blit
- Purpose: Virtual method for RLE-compressed blitting with optional lead skip
- Calls: None (pure virtual)

## Globals
- None

## Dependencies
- Key includes: None
- External symbols: None
