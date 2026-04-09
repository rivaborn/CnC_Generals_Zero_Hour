# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/tgatodxt.h

## Purpose
Header file for a TGA to DXT texture converter utility class.

## Responsibilities
- Declares `TGAToDXTClass` for converting TGA images to DXT compressed textures.
- Defines error codes for conversion failures.
- Provides interface for file conversion with timestamp and alpha channel handling.
- Manages buffer for intermediate data during conversion.

## Key Types
- `TGAToDXTClass` (Class): Main converter class handling TGA to DXT conversion.
- `ErrorCode` (Enum): Conversion error status codes (OK, INVALID_BIT_DEPTH, etc.).

## Key Functions
### `Convert`
- Purpose: Converts TGA file to DXT format with optional alpha channel check.
- Calls: `Write`, `ReadDTXnFile`, `WriteDTXnFile` (via friends).

### `Write`
- Purpose: Writes DXT data to output file.
- Calls: Not inferable.

## Globals
- `_TGAToDXTConverter` (TGAToDXTClass): Global instance of the converter.

## Dependencies
- `always.h`, `<windows.h>`, `<winbase.h>`
- `ReadDTXnFile`, `WriteDTXnFile` (external functions used via friendship).
