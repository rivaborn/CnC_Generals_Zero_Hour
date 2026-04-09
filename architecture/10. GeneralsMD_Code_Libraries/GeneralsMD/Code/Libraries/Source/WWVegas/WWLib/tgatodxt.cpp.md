# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/tgatodxt.cpp

## Purpose
Converts TGA image files to DXT texture formats using NVIDIA's compression library.

## Responsibilities
- Loads TGA files and validates format requirements
- Compresses image data to DXT1 or DXT5 formats
- Handles alpha channel analysis and removal
- Writes compressed data to output file

## Key Types
- TGAToDXTClass (Class): Main converter class managing TGA to DXT conversion
- ErrorCode (Enum): Conversion error status codes
- Targa (Struct): TGA image data structure

## Key Functions
### Convert
- Purpose: Main conversion function that processes TGA to DXT
- Calls: Targa::Load, Targa::YFlip, nvDXTcompress, Write

### Write
- Purpose: Writes compressed DXT data to output file
- Calls: CreateFile, LockFile, WriteFile, UnlockFile, CloseHandle, SetFileTime

### WriteDTXnFile
- Purpose: Callback for writing DXT data chunks
- Calls: memcpy, new, delete

## Globals
- _TGAToDXTConverter (TGAToDXTClass): Singleton instance of converter
- Buffer (unsigned char*): Internal buffer for output data
- BufferSize (unsigned): Current buffer size
- BufferCount (unsigned): Current buffer usage count
- WriteTimePtr (FILETIME*): Pointer to file timestamp

## Dependencies
- nvdxtlib.h: NVIDIA DXT compression library
- targa.h: TGA image loading
- tgatodxt.h: Header for this module
- WWDebug.h: Assertion macros
- Windows API: File operations and memory management
