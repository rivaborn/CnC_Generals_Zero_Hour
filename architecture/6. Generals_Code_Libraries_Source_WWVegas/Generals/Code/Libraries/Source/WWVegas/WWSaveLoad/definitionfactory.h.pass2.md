# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/definitionfactory.h - Enhanced Analysis

## Architectural Role
This file defines the core abstraction for the game's definition system, enabling runtime creation and management of game object definitions (e.g., units, buildings). It serves as the bridge between the save/load system and the concrete definition classes, supporting modding by allowing dynamic registration of new definition types.

## Cross-References
### Incoming
- `DefinitionFactoryMgrClass` (friend) - Manages the linked list of factories
- Concrete factory implementations (e.g., `SimpleDefinitionFactoryClass`) - Inherit and implement pure virtual methods

### Outgoing
- None (pure interface)

## Design Patterns
- **Factory Method**: Abstracts object creation, allowing subclasses to define instantiation logic
- **Linked List**: Uses `m_NextFactory`/`m_PrevFactory` for runtime registry management
- **Dependency Injection**: Factories are injected into the manager, decoupling creation from usage

*Not inferable*: Specific usage patterns in save/load pipeline or modding hooks.
