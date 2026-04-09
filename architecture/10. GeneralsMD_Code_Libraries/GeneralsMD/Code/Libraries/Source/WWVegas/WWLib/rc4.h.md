# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rc4.h

## Purpose
Implements the RC4 stream cipher for encryption/decryption.

## Responsibilities
- Provides RC4 encryption/decryption functionality
- Handles key preparation for different key lengths
- Manages internal state for stream cipher operations
- Supports state copying and debugging output

## Key Types
- **RC4Class (Class)**: Main RC4 cipher implementation
- **RC4Key (Struct)**: Internal state container (256-byte state + 2 counters)

## Key Functions
### RC4Class()
- Purpose: Default constructor
- Calls: Not inferable

### Prepare_Key()
- Purpose: Initializes cipher state with a key
- Calls: Prepare_Key_16bytes or Prepare_Key_8bytes

### RC4()
- Purpose: Performs in-place encryption/decryption
- Calls: Not inferable

### operator=()
- Purpose: Copies cipher state from another instance
- Calls: Not inferable

### Print_State()
- Purpose: Debug function to output internal state
- Calls: Not inferable

### Prepare_Key_16bytes()
- Purpose: Optimized key preparation for 16-byte keys
- Calls: Not inferable

### Prepare_Key_8bytes()
- Purpose: Optimized key preparation for 8-byte keys
- Calls: Not inferable

## Globals
None

## Dependencies
- Standard C++ headers (not explicitly shown)
- Uses unsigned char for byte operations
