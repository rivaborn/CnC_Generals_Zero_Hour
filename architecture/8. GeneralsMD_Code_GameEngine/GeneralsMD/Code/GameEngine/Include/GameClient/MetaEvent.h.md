# GeneralsMD/Code/GameEngine/Include/GameClient/MetaEvent.h

## Purpose
Defines enums, classes, and structures for handling game input events and key mappings in the SAGE engine.

## Responsibilities
- Defines key categories, types, transitions, and modifier states for input mapping
- Provides lookup tables for key names and descriptions
- Declares classes for managing meta-event translations and key mappings
- Defines the MetaMap subsystem interface for parsing and managing key bindings

## Key Types
- **MappableKeyCategories (Enum)**: Categories for grouping key bindings (e.g., CONTROL, SELECTION)
- **MappableKeyType (Enum)**: Enumeration of mappable keys (e.g., MK_ESC, MK_A, MK_F1)
- **MappableKeyTransition (Enum)**: Key transition states (DOWN, UP, DOUBLEDOWN)
- **MappableKeyModState (Enum)**: Modifier key states (CTRL, ALT, SHIFT combinations)
- **CommandUsableInType (Enum)**: Contexts where commands are allowed (SHELL, GAME)
- **MetaMapRec (Class)**: Structure for storing key-to-meta-event mappings
- **MetaEventTranslator (Class)**: Translates game messages to meta-events
- **MetaMap (Class)**: Subsystem for managing key mappings and parsing configuration

## Key Functions
### MetaEventTranslator::translateGameMessage
- Purpose: Translates game messages into meta-events.
- Calls: Not inferable from header.

### MetaMap::parseMetaMap
- Purpose: Parses key mapping configuration from an INI file.
- Calls: Not inferable from header.

### MetaMap::getFirstMetaMapRec
- Purpose: Retrieves the first key mapping record.
- Calls: None.

## Globals
- **CategoryListName (LookupListRec[])**: Maps category names to enum values.
- **KeyNames (LookupListRec[])**: Maps key names to MappableKeyType values.
- **TransitionNames (LookupListRec[])**: Maps transition names to enum values.
- **ModifierNames (LookupListRec[])**: Maps modifier names to MappableKeyModState values.
- **TheCommandUsableInNames (char*[])**: Names for CommandUsableInType contexts.
- **TheMetaMap (MetaMap*)**: Global instance of the MetaMap subsystem.

## Dependencies
- **Common/SubsystemInterface.h**: Base class for subsystem interfaces.
- **GameClient/InGameUI.h**: Likely defines GameMessage and related types.
- **LookupListRec**: External type for name-to-value mappings.
- **MemoryPoolObject**: Base class for memory-pooled objects.
- **GameMessageTranslator**: Base class for message translators.
