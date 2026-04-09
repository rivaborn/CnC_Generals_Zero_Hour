# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blowpipe.cpp

## Purpose
Implements a Blowfish encryption/decryption pipe for secure data transfer in the game engine.

## Responsibilities
- Encrypts/decrypts data blocks using Blowfish algorithm
- Manages partial block buffering for stream processing
- Flushes pending data through the pipe chain
- Handles key submission for encryption/decryption

## Key Types
- BlowPipe (Class): Encryption/decryption pipe handler
- BlowfishEngine (Class): Underlying Blowfish cryptographic engine

## Key Functions
### BlowPipe::Flush
- Purpose: Forces any pending data to be processed and flushed through the pipe
- Calls: Pipe::Put, Pipe::Flush

### BlowPipe::Put
- Purpose: Processes data blocks for encryption/decryption before passing to next pipe
- Calls: Pipe::Put, BF->Encrypt, BF->Decrypt

### BlowPipe::Key
- Purpose: Submits encryption key to initialize the Blowfish engine
- Calls: new BlowfishEngine, BF->Submit_Key

## Globals
- None

## Dependencies
- blowpipe.h (header)
- always.h (header)
- string.h (memmove)
- assert.h (assert)
- Pipe class (base class)
- BlowfishEngine class (external)
