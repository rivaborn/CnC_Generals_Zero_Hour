# Generals/Code/Tools/Launcher/Toolkit/Support/RefPtr.h - Enhanced Analysis

## Architectural Role
This file defines the core smart pointer infrastructure for the SAGE engine's toolkit, enabling reference-counted object management across the toolchain. It bridges the gap between raw pointers and modern memory management, enforcing factory-based object creation patterns.

## Cross-References
### Incoming
- Toolkit components using reference-counted objects (e.g., asset loaders, scene graph nodes)
- Factory methods in derived `RefCounted` classes

### Outgoing
- `RefCounted.h` for base reference counting functionality
- Platform-specific headers (`VisualC.h`) for compiler compatibility

## Design Patterns
- **Factory Method**: Enforces object creation through factory methods by making constructors private/friends
- **Proxy**: `RefPtr` acts as a proxy for the underlying object, controlling access and lifetime
- **Template Method**: Base class (`RefPtrBase`) defines reference counting behavior, subclasses implement type-specific operations

*Not inferable*: Exact usage patterns in toolkit components (e.g., asset pipeline integration)
