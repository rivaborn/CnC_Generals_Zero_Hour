# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/textfile.cpp

## Purpose
Implements text file I/O operations for reading and writing lines of text.

## Responsibilities
- Read lines from text files
- Write lines to text files
- Handle line endings (CR/LF)
- Manage file position during read operations

## Key Types
- TextFileClass (Class): Text file I/O wrapper

## Key Functions
### Read_Line
- Purpose: Reads a line of text from the file into a StringClass
- Calls: Read, Seek, StringClass methods (Empty, +=, Get_Length, Peek_Buffer, Erase)

### Write_Line
- Purpose: Writes a line of text to the file with CR/LF termination
- Calls: Write, StringClass methods (Get_Length)

## Globals
None

## Dependencies
- textfile.h
- wwstring.h
- RawFileClass (inherited)
- StringClass
