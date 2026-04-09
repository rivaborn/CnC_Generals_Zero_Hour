# GeneralsMD/Code/GameEngine/Source/Common/Thing/ModuleFactory.cpp - Enhanced Analysis

## Architectural Role
Central registry and factory for game modules, enabling dynamic creation of behaviors, updates, and other game logic components. Acts as a bridge between INI-defined module configurations and runtime object instantiation.

## Cross-References
### Incoming
- Game logic initialization (likely in `GameEngine.cpp` or similar)
- Object/Thing creation systems (e.g., `ThingFactory`)
- Module data serialization (networking/xfer systems)

### Outgoing
- All module implementations (behaviors, updates, etc.)
- `NameKeyGenerator` for module name hashing
- `ModuleData` subclasses for configuration

## Design Patterns
- **Factory Pattern**: Core responsibility - creates modules without exposing instantiation logic
- **Registry Pattern**: Maintains map of module templates for runtime lookup
- **Decorator Pattern**: Uses `makeDecoratedNameKey` to scope module names by type (e.g., "Behavior:AutoHeal")

*Not inferable*: Exact caller relationships without full call graph.
