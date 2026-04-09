# Generals/Code/Tools/Autorun/WSYS_FileSystem.h

## Purpose
Defines the FileSystem interface class for abstracting file system operations in the WSYS library.

## Responsibilities
- Declares the FileSystem abstract base class
- Provides a singleton instance (TheFileSystem)
- Defines the virtual open() method for file access

## Key Types
- FileSystem (Class): Abstract interface for file system operations
- File* (Return type): Pointer to file objects created by open()

## Key Functions
### ~FileSystem()
- Purpose: Virtual destructor for FileSystem class
- Calls: None

### open()
- Purpose: Abstract method to open a file and return a File interface
- Calls: None (pure virtual)

## Globals
- TheFileSystem (FileSystem*): Singleton instance of the file system interface

## Dependencies
- wsys_file.h (included)
- Char, Int (types from external headers)
- File (class from external headers)
