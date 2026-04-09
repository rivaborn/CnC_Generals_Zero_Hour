# GeneralsMD/Code/GameEngine/Source/Common/Thing/ThingFactory.cpp

## Purpose
Manages creation, storage, and retrieval of game object templates (ThingTemplate) and instantiation of game objects (Object/Drawable).

## Responsibilities
- Maintains a database of ThingTemplate instances
- Provides factory methods for creating game objects
- Handles template overrides and inheritance
- Loads and parses template definitions from INI files
- Manages template lifecycle (init/reset/update)

## Key Types
- **ThingFactory (Class)**: Singleton manager for game object templates
- **ThingTemplate (Class)**: Template definition for game objects
- **TEMPLATE_HASH_SIZE (Enum)**: Hash table size constant (12288)

## Key Functions
### `newObject`
- Purpose: Creates a new game object from a template
- Calls: `TheGameLogic->friend_createObject`, `ThePartitionManager->registerObject`, `obj->initObject`

### `newDrawable`
- Purpose: Creates a new drawable object from a template
- Calls: `TheGameClient->friend_createDrawable`

### `parseObjectDefinition`
- Purpose: Parses INI definitions to create/update templates
- Calls: `findTemplateInternal`, `newTemplate`, `newOverride`, `ini->initFromINI`

### `postProcessLoad`
- Purpose: Validates and resolves template references after loading
- Calls: `thingTemplate->resolveNames`

## Globals
- **TheThingFactory (ThingFactory*)**: Singleton instance of the factory

## Dependencies
- Key includes: `ThingTemplate.h`, `GameLogic.h`, `INI.h`, `PartitionManager.h`
- External symbols: `TheGameLogic`, `ThePartitionManager`, `TheGameClient`
