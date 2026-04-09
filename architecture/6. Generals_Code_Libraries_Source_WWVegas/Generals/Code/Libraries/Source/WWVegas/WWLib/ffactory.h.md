# Generals/Code/Libraries/Source/WWVegas/WWLib/ffactory.h

## Purpose
Defines file factory classes and smart pointer for file handling in the SAGE engine.

## Responsibilities
- Declares abstract `FileFactoryClass` for file creation/management
- Provides `file_auto_ptr` for automatic file resource management
- Implements concrete factories (`RawFileFactoryClass`, `SimpleFileFactoryClass`)
- Manages global file factory instances

## Key Types
- **FileFactoryClass (Class)**: Abstract base for file factories
- **file_auto_ptr (Class)**: Smart pointer for automatic file return
- **RawFileFactoryClass (Class)**: Factory for raw file objects
- **SimpleFileFactoryClass (Class)**: Enhanced factory with subdirectory support
- **FileClass (Class)**: Forward declaration for file objects

## Key Functions
### FileFactoryClass/Get_File
- Purpose: Pure virtual method to get a file by name
- Calls: None

### FileFactoryClass/Return_File
- Purpose: Pure virtual method to return a file
- Calls: None

### file_auto_ptr/file_auto_ptr
- Purpose: Constructor taking factory and filename
- Calls: `Get_File`

### file_auto_ptr/~file_auto_ptr
- Purpose: Destructor that returns the file
- Calls: `Return_File`

### SimpleFileFactoryClass/Get_File
- Purpose: Gets a file with subdirectory support
- Calls: None (implementation not shown)

### SimpleFileFactoryClass/Return_File
- Purpose: Returns a file with logging
- Calls: None (implementation not shown)

## Globals
- **_TheFileFactory (FileFactoryClass*)**: Global read file factory
- **_TheWritingFileFactory (RawFileFactoryClass*)**: Global write file factory

## Dependencies
- `always.h`, `mutex.h`,
