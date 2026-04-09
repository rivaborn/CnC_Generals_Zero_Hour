# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pkstraw.h

## Purpose
Defines the PKStraw class for public-key encryption/decryption using Blowfish and random number generation.

## Responsibilities
- Manages encryption/decryption control flow
- Handles key exchange and staging
- Buffers data for block processing
- Integrates with BlowStraw for symmetric encryption

## Key Types
- **PKStraw (Class)**: Public-key encryption/decryption straw (data pipeline)
- **CryptControl (Enum)**: Encryption/decryption mode selector
- **BlowStraw (Class)**: Internal Blowfish symmetric encryption pipeline
- **RandomStraw (Class)**: Random number generator dependency

## Key Functions
### PKStraw::Get_From
- Purpose: Retrieves encrypted/decrypted data from another straw
- Calls: PKStraw::Get_From (overload)

### PKStraw::Get
- Purpose: Processes data through the encryption/decryption pipeline
- Calls: Not inferable

### PKStraw::Key
- Purpose: Sets the public/private key for encryption/decryption
- Calls: Not inferable

## Globals
None

## Dependencies
- `blwstraw.h` (BlowStraw)
- `pk.h` (PKey)
- `rndstraw.h` (RandomStraw)
- Inherits from `Straw` (base class)
