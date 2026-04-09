# GeneralsMD/Code/GameEngine/Source/Common/System/encrypt.cpp

## Purpose
Implements a simple one-way string encryption/obfuscation for online password handling.

## Responsibilities
- Encrypts strings up to 8 characters long using a fixed base string.
- Converts encrypted data into a base64-like format using `Base_String`.
- Provides a portable encryption function for cross-platform use.

## Key Types
- None

## Key Functions
### EncryptString
- Purpose: Encrypts a string using bitwise operations and a fixed base string.
- Calls: `strlen`, `Base_String` lookup.

## Globals
- Base_String (char[65]): Base64-like character set for encoding.
- Return_Buffer (char[MAX_ENCRYPTED_STRING + 1]): Stores the final encrypted string.
- Temp_Buffer (char[MAX_ENCRYPTED_STRING + 1]): Intermediate buffer for encryption.

## Dependencies
- `<stdio.h>`, `<string.h>`
- `Common/encrypt.h` (for `MAX_ENCRYPTED_STRING`)
- `PreRTS.h` (game engine precompiled header)
