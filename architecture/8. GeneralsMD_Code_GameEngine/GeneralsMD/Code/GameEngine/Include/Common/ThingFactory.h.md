# GeneralsMD/Code/GameEngine/Include/Common/ThingFactory.h

## Purpose
Manages creation and lookup of game object templates, objects, and drawables.

## Responsibilities
- Creates and manages `ThingTemplate` instances
- Provides factory methods for `Object` and `Drawable` creation
- Maintains a hash map for fast template lookup
- Handles template overrides and parsing from INI files

## Key Types
- `ThingTemplate` (Class): Base template for game objects
- `ThingTemplateHashMap` (Class): Hash map storing templates by name
- `ThingFactory` (Class): Singleton factory for game objects

## Key Functions
### `newTemplate`
- Purpose: Creates a new template with given name
- Calls: `addTemplate`

### `findTemplate`
- Purpose: Retrieves template by name via hash map lookup
- Calls: `findTemplateInternal`

### `newObject`
- Purpose: Creates a new game object from a template
- Calls: Not inferable (external)

### `parseObjectDefinition`
- Purpose: Parses object definitions from INI files
- Calls: Not inferable (external)

### `findTemplateInternal`
- Purpose: Internal template lookup with optional validation
- Calls: Not inferable (hash map operations)

## Globals
- `TheThingFactory` (ThingFactory*): Singleton instance of the factory

## Dependencies
- `SubsystemInterface`, `AsciiString`, `Object`, `Drawable`, `INI`
- STL hash_map with custom hash/equal_to for AsciiString
