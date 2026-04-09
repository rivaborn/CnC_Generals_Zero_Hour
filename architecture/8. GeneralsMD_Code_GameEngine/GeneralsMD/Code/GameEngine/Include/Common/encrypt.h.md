# GeneralsMD/Code/GameEngine/Include/Common/encrypt.h

## Purpose
Header file declaring a string encryption function for obfuscating online passwords.

## Responsibilities
- Declares the `EncryptString` function for password obfuscation
- Defines `MAX_ENCRYPTED_STRING` constant (8)
- Documents non-reentrant behavior and input constraints

## Key Types
- None

## Key Functions
### EncryptString
- Purpose: Obfuscates a 4-8 character string (letters, numbers, '.', '/') into a static buffer.
- Calls: Not inferable (implementation in separate file)

## Globals
- `MAX_ENCRYPTED_STRING` (const int): Maximum length of encrypted string (8)

## Dependencies
- None (header-only, no includes)
