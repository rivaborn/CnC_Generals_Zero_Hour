# Generals/Code/Libraries/Source/WWVegas/WWLib/textfile.h

## Purpose
Defines the TextFileClass for reading/writing lines of text in the SAGE engine.

## Responsibilities
- Extends RawFileClass to handle text file operations
- Provides line-based read/write functionality
- Manages text file I/O with CR/LF or LF line endings

## Key Types
- **StringClass (Class)**: Used for storing text lines.
- **TextFileClass (Class)**: Text file I/O wrapper for line operations.

## Key Functions
### TextFileClass()
- Purpose: Default constructor.
- Calls: Not inferable.

### TextFileClass(char const *filename)
- Purpose: Constructor opening a file by name.
- Calls: Not inferable.

### TextFileClass(const TextFileClass &src)
- Purpose: Copy constructor.
- Calls: Not inferable.

### ~TextFileClass()
- Purpose: Destructor.
- Calls: Not inferable.

### operator=(const TextFileClass &src)
- Purpose: Assignment operator.
- Calls: Not inferable.

### Read_Line(StringClass &string)
- Purpose: Reads a line into the provided StringClass.
- Calls: Not inferable.

### Write_Line(const StringClass &string)
- Purpose: Writes a line from the provided StringClass.
- Calls: Not inferable.

## Globals
None.

## Dependencies
- **rawfile.h**: Inherits from RawFileClass.
- **StringClass**: Used for text storage (forward-declared).
