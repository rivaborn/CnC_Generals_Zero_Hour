# Generals/Code/Tools/mangler/wlib/configfile.h

## Purpose
Provides a class for reading, writing, and manipulating configuration files with key-value pairs organized into sections.

## Responsibilities
- Parse and read configuration files
- Retrieve string and integer values by key (with optional section)
- Enumerate configuration entries
- Modify configuration entries (add/update/remove)
- Write configuration changes back to file

## Key Types
- ConfigFile (Class): Manages configuration file data and operations
- Dictionary<Wstring,Wstring> (Member): Stores key-value string mappings
- ArrayList<Wstring> (Member): Stores section names
- CritSec (Member): Provides thread synchronization for dictionary access

## Key Functions
### ConfigFile::readFile
- Purpose: Reads and parses a configuration file
- Calls: Dictionary operations

### ConfigFile::getString
- Purpose: Retrieves a string value by key (with optional section)
- Calls: Dictionary lookup

### ConfigFile::getInt
- Purpose: Retrieves an integer value by key (with optional section)
- Calls: Dictionary lookup

### ConfigFile::enumerate
- Purpose: Iterates through configuration entries (with optional section)
- Calls: Dictionary iteration

### ConfigFile::setString/setInt
- Purpose: Updates or adds a configuration entry
- Calls: Dictionary operations

### ConfigFile::removeEntry
- Purpose: Removes a configuration entry
- Calls: Dictionary operations

### ConfigFile::writeFile
- Purpose: Writes current configuration to a file
- Calls: Dictionary iteration

## Globals
None

## Dependencies
- wstypes.h (bit8, sint32, sint16)
- dictionary.h (Dictionary)
- wstring.h (Wstring)
- critsec.h (CritSec)
- arraylist.h (ArrayList)
