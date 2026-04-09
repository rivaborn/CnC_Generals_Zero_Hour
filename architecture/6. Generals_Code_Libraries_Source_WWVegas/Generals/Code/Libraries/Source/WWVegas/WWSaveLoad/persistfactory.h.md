# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/persistfactory.h

## Purpose
Defines the PersistFactoryClass hierarchy and SimplePersistFactoryClass template for object serialization in the SAGE engine.

## Responsibilities
- Declares the base PersistFactoryClass interface for object persistence.
- Provides a template-based SimplePersistFactoryClass for automatic factory generation.
- Manages chunk-based save/load operations for persistent objects.
- Handles object pointer remapping during load operations.

## Key Types
- **PersistClass (Class)**: Base class for persistable objects.
- **PersistFactoryClass (Class)**: Abstract factory for creating and serializing PersistClass objects.
- **SimplePersistFactoryClass (Class)**: Template-based factory for simple persistence.
- **(anonymous enum) (Enum)**: Internal chunk IDs for SimplePersistFactoryClass.
- **SIMPLEFACTORY_CHUNKID_OBJPOINTER (Enum)**: Chunk ID for object pointer data.
- **SIMPLEFACTORY_CHUNKID_OBJDATA (Enum)**: Chunk ID for object data.

## Key Functions
### PersistFactoryClass::Chunk_ID
- Purpose: Returns the chunk ID for this factory.
- Calls: None

### PersistFactoryClass::Load
- Purpose: Loads a PersistClass object from a chunk.
- Calls: None

### PersistFactoryClass::Save
- Purpose: Saves a PersistClass object to a chunk.
- Calls: None

### SimplePersistFactoryClass::Load
- Purpose: Loads a template object and handles pointer remapping.
- Calls: `W3DNEW`, `cload.Open_Chunk`, `cload.Read`, `cload.Close_Chunk`, `SaveLoadSystemClass::Register_Pointer`

### SimplePersistFactoryClass::Save
- Purpose: Saves a
