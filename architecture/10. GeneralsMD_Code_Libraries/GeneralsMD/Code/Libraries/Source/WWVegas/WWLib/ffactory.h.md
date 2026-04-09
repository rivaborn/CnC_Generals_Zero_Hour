# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/ffactory.h

## Purpose
Defines file factory classes and smart pointer for file handling in the SAGE engine.

## Responsibilities
- Declares abstract `FileFactoryClass` and concrete implementations (`RawFileFactoryClass`, `SimpleFileFactoryClass`).
- Provides `file_auto_ptr` for RAII file management.
- Manages global file factory instances (`_TheFileFactory`, `_TheWritingFileFactory`, `_TheSimpleFileFactory`).

## Key Types
- **FileFactoryClass (Class)**: Abstract base for file creation/return.
- **file_auto_ptr (Class)**: Smart pointer for automatic file return.
- **RawFileFactoryClass (Class)**: Factory for raw file objects.
- **SimpleFileFactoryClass (Class)**: Extended factory with subdirectory and path stripping support.

## Key Functions
### FileFactoryClass::Get_File
- Purpose: Pure virtual method to obtain a file.
- Calls: None (abstract).

### FileFactoryClass::Return_File
- Purpose: Pure virtual method to return a file.
- Calls: None (abstract).

### file_auto_ptr::operator*
- Purpose: Dereferences the held file.
- Calls: `get()`.

### SimpleFileFactoryClass::Get_File
- Purpose: Retrieves a file with subdirectory support.
- Calls: None (implementation in .cpp).

### SimpleFileFactoryClass::Set_Sub_Directory
- Purpose: Sets the current subdirectory for file operations.
- Calls: None.

## Globals
- `_TheFileFactory (FileFactoryClass*)`: Default file factory instance.
- `_TheWritingFileFactory (RawFileFactoryClass*)`: Factory for writable files.
- `_TheSimpleFileFactory (SimpleFileFactoryClass*)`: Factory with subdirectory support.

## Dependencies
- `rawfile.h`, `mutex.h`, `vector
