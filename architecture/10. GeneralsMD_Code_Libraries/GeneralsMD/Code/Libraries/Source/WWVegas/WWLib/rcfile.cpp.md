# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rcfile.cpp

## Purpose
Implements a resource file wrapper for reading embedded resources from a module.

## Responsibilities
- Loads resources from a module using Windows API
- Provides file-like operations (read, seek, size) on the resource data
- Manages resource name and memory cleanup

## Key Types
- ResourceFileClass (Class): wraps a resource file for reading operations

## Key Functions
### ResourceFileClass::ResourceFileClass
- Purpose: Constructor that loads a resource from a module
- Calls: FindResource, LoadResource, LockResource, SizeofResource, strdup

### ResourceFileClass::Set_Name
- Purpose: Sets the resource name and returns the previous name
- Calls: free, strdup

### ResourceFileClass::Read
- Purpose: Reads data from the resource into a buffer
- Calls: memcpy

### ResourceFileClass::Seek
- Purpose: Changes the read position within the resource
- Calls: None

### ResourceFileClass::Size
- Purpose: Returns the size of the resource in bytes
- Calls: None

### ResourceFileClass::Error
- Purpose: Placeholder for error handling (does nothing)
- Calls: None

## Globals
- RESOURCE_FILE_TYPE_NAME (const char*): Resource type name for finding resources

## Dependencies
- rcfile.h
- Windows API (FindResource, LoadResource, LockResource, SizeofResource)
- C runtime (free, strdup, memcpy)
