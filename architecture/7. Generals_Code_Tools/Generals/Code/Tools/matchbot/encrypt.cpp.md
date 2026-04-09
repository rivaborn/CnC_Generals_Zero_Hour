# Generals/Code/Tools/matchbot/encrypt.cpp

## Purpose
Implements a simple one-way string encryption algorithm for the game's matchmaking system.

## Responsibilities
- Encrypts strings up to 8 characters long using a fixed base string.
- Converts encrypted data into a printable format using a 65-character alphabet.
- Provides a portable encryption method for cross-platform compatibility.

## Key Types
- None

## Key Functions
### do_encrypt
- Purpose: Encrypts an input string using a bitwise algorithm and base64-like encoding.
- Calls: strlen, memset (implied), Base_String lookup

## Globals
- Base_String (char[65]): Alphabet used for encoding (a-z, A-Z, 0-9, './').
- Return_Buffer (char[MAX_ENCRYPTED_STRING+1]): Stores the final encrypted string.
- Temp_Buffer (char[MAX_ENCRYPTED_STRING+1]): Intermediate storage during encryption.

## Dependencies
- <stdio.h>, <string.h>
- MAX_ENCRYPTED_STRING (from encrypt.h)
- encrypt.h header
