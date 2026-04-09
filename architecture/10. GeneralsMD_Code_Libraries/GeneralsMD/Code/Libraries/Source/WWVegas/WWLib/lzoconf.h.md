# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzoconf.h

## Purpose
Configuration header for the LZO real-time data compression library, defining types, macros, and function prototypes.

## Responsibilities
- Defines integral and pointer types for LZO compression
- Declares compression/decompression function types
- Provides error codes and version information
- Includes platform-specific configuration

## Key Types
- lzo_uint (Type): Unsigned 32-bit integer type
- lzo_int (Type): Signed 32-bit integer type
- lzo_ptr_t (Type): Unsigned type that can store all bits of a pointer
- lzo_compress_t (Function pointer): Compression function signature
- lzo_decompress_t (Function pointer): Decompression function signature
- lzo_progress_callback_t (Function pointer): Progress callback signature

## Key Functions
### lzo_init
- Purpose: Initialize the LZO library
- Calls: Not inferable

### lzo_version
- Purpose: Get LZO library version number
- Calls: Not inferable

### lzo_version_string
- Purpose: Get LZO library version string
- Calls: Not inferable

### lzo_memcmp
- Purpose: Compare memory blocks
- Calls: Not inferable

### lzo_memcpy
- Purpose: Copy memory blocks
- Calls: Not inferable

### lzo_memmove
- Purpose: Move memory blocks
- Calls: Not inferable

### lzo_memset
- Purpose: Set memory blocks to a value
- Calls: Not inferable

### lzo_adler32
- Purpose: Compute Adler-32 checksum
- Calls: Not inferable

### lzo_assert
- Purpose: Assertion macro for debugging
- Calls: Not inferable

### _lzo_config_check
- Purpose: Check configuration validity
- Calls: Not inferable

## Globals
- LZO_VERSION (Macro): Library version number
- LZO_VERSION_STRING (Macro): Library version string
- LZO_VERSION_DATE (Macro): Library version date
- LZO_E_OK (Macro): Success error code
- LZO_E_ERROR (Macro): Generic error code
- LZO_E_NOT_COMPRESSIBLE (Macro): Data not compressible error code
- LZO_E_EOF_NOT_FOUND (Macro): EOF not found error code
- LZO_E_INPUT_OVERRUN (Macro): Input overrun error code
- LZO_E_OUTPUT_OVERRUN (Macro): Output overrun error code
- LZO_E_LOOKBEHIND_OVERRUN (Macro): Lookbehind over
