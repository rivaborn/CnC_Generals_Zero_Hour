# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/textfile.h

## Purpose
Defines the TextFileClass for reading/writing lines of text in the SAGE engine.

## Responsibilities
- Extends RawFileClass to add text file support
- Provides line-based read/write operations
- Manages text file I/O with CR/LF or LF line endings

## Key Types
- **StringClass (Class)**: Used for storing text lines.
- **TextFileClass (Class)**: Text file I/O wrapper for line operations.

## Key Functions
### TextFileClass (Constructors)
- Purpose: Initialize TextFileClass instances.
- Calls: Not inferable (likely calls parent RawFileClass).

### ~TextFileClass (Destructor)
- Purpose: Clean up TextFileClass resources.
- Calls: Not inferable.

### operator= (Assignment)
- Purpose: Assign TextFileClass from another instance.
- Calls: Not inferable.

### Read_Line (StringClass &string)
- Purpose: Read a line of text into a StringClass.
- Calls: Not inferable.

### Write_Line (const StringClass &string)
- Purpose: Write a line of text from a StringClass.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- **rawfile.h**: Inherits from RawFileClass.
- **StringClass**: Used for text storage (forward-declared).
