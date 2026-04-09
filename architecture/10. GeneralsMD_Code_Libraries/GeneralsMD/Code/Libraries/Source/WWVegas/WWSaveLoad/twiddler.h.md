# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/twiddler.h

## Purpose
Defines the `TwiddlerClass`, a persistence class for managing indirect class references in save/load operations.

## Responsibilities
- Manages indirect class ID references for save/load operations
- Provides factory methods for object creation
- Handles serialization/deserialization of twiddler data
- Maintains a list of definition indices

## Key Types
- **TwiddlerClass (Class)**: Base class for managing indirect class references in persistence operations

## Key Functions
### TwiddlerClass()
- Purpose: Default constructor
- Calls: None

### ~TwiddlerClass()
- Purpose: Destructor
- Calls: None

### Get_Class_ID()
- Purpose: Returns the class ID for this twiddler type
- Calls: None

### Create()
- Purpose: Factory method to create a new instance
- Calls: None

### Save()
- Purpose: Serializes the twiddler data
- Calls: Save_Variables()

### Load()
- Purpose: Deserializes the twiddler data
- Calls: Load_Variables()

### Get_Factory()
- Purpose: Returns the persistence factory for this class
- Calls: None

### Twiddle()
- Purpose: Virtual method for creating a new definition instance
- Calls: None

### Get_Indirect_Class_ID()
- Purpose: Returns the stored indirect class ID
- Calls: None

### Set_Indirect_Class_ID()
- Purpose: Sets the indirect class ID
- Calls: None

### Save_Variables()
- Purpose: Serializes member variables
- Calls: None

### Load_Variables()
- Purpose: Deserializes member variables
- Calls: None

## Globals
- None

## Dependencies
-
