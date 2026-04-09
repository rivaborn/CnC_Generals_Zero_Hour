# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blitter.h

## Purpose
Defines abstract blitter interfaces for pixel data transfer operations in the SAGE engine.

## Responsibilities
- Declares base `Blitter` class for forward/backward pixel copying.
- Declares `RLEBlitter` class for RLE-compressed data decompression.
- Provides virtual methods for pixel blitting with overlap handling.

## Key Types
- **Blitter (Class)**: Abstract base for pixel blitting operations.
- **RLEBlitter (Class)**: Abstract base for RLE-compressed pixel decompression.

## Key Functions
### Blitter::BlitForward
- Purpose: Copies pixels from source to destination in forward order.
- Calls: None (pure virtual).

### Blitter::BlitBackward
- Purpose: Copies pixels from source to destination in reverse order.
- Calls: None (pure virtual).

### Blitter::Blit
- Purpose: Dispatches to `BlitForward` or `BlitBackward` based on memory overlap.
- Calls: `BlitForward`, `BlitBackward`.

### RLEBlitter::Blit
- Purpose: Decompresses RLE data to destination with optional leading skip.
- Calls: None (pure virtual).

## Globals
- None.

## Dependencies
- None (header-only interface).
