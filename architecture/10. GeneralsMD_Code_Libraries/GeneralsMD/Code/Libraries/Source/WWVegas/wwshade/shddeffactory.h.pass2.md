# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shddeffactory.h - Enhanced Analysis

## Architectural Role
This file implements the factory pattern for shader definitions in the SAGE engine's rendering pipeline. It enables runtime registration and instantiation of shader types, supporting the engine's modular shader system.

## Cross-References
### Incoming
- Shader definition implementations (e.g., in `wwshade` directory) use `REGISTER_SHDDEF` macro
- `ShdDefManagerClass` iterates over factory instances via `NextFactory`/`PrevFactory` links

### Outgoing
- Calls into `ShdDefClass` derivatives during instantiation
- Relies on `ShdDefManagerClass` for factory registration management

## Design Patterns
- **Factory Pattern**: Abstracts shader creation, allowing dynamic registration of new shader types
- **Template Method**: `SimpleShdDefFactoryClass` provides default implementations for factory methods
- **Double Linked List**: Manages factory instances for iteration (used by `ShdDefManagerClass`)

*Not inferable*: Specific shader implementations or manager usage details.
