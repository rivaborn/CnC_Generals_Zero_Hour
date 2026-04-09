# Generals/Code/Tools/CRCDiff/CRCDiff.cpp

## Purpose
This file implements a command-line tool for comparing two text files and generating an HTML diff report.

## Responsibilities
- Parse two input files with frame:index line format
- Compare lines between files and categorize differences
- Generate HTML output using templates (header, row, footer)
- Queue and dump lines for diff visualization
- Handle command-line arguments and file I/O

## Key Types
- **Expander (Class)**: Template expansion utility for HTML generation
- **KVPair (Class)**: Not directly used here, but included via header
- **std::list<std::string> (Type)**: Used for queuing lines before output

## Key Functions
### exitWait
- Purpose: Pause execution before exit (Windows-specific)
- Calls: system("PAUSE")

### getNextLine
- Purpose: Read next valid line with frame:index format from file
- Calls: fgets, fclose, sscanf, strlen, strcpy

### readInFile
- Purpose: Read entire file into string
- Calls: fopen, fgets, fclose

### outputLine (const char*)
- Purpose: Output raw text to HTML file
- Calls: dumpQueued, fputs

### outputLine (int, int, int, const char*, const char*, const char*, const char*, bool)
- Purpose: Generate HTML diff row with template expansion
- Calls: dumpQueued, Expander methods, fputs

### queueLine
- Purpose: Queue identical lines for later output
- Calls: Expander methods, queuedLines operations

### dumpQueued
- Purpose: Output all queued lines
- Calls: fputs

### main
- Purpose: Main program loop comparing files and generating diff
- Calls: All other functions, fopen, fclose, strcmp, system

## Globals
- **tableRow (std::string)**: HTML template for diff rows
- **ofp (FILE*)**: Output file handle
- **queuedLines (std::list<std::string>)**: Buffer for identical lines

## Dependencies
- debug.h, expander.h, KVPair.h, misc.h
- <iostream>, <list>, <stdlib.h>, <stdio.h>
- system(), fopen(), fgets(), fputs(), fclose(), sscanf(), strlen(), strcpy(), strcmp(), atexit()
