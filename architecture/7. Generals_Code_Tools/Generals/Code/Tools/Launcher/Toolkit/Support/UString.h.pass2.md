# Generals/Code/Tools/Launcher/Toolkit/Support/UString.h - Enhanced Analysis

## Architectural Role
This file defines the `UString` class, a Unicode string wrapper used throughout the SAGE engine toolkit for internationalization support. It extends `RefCounted` for memory management, indicating its role in shared string resources across tools.

## Cross-References
### Incoming
- Toolkit utilities (e.g., file I/O, configuration parsing) likely use `UString` for Unicode path/string handling
- Localization systems would depend on this for multi-language support

### Outgoing
- Relies on `RefCounted` base class for reference counting
- Uses `UTypes.h` for fundamental types (e.g., `WChar`, `UInt`)

## Design Patterns
- **Flyweight**: Reference counting suggests shared string instances to optimize memory
- **Facade**: Wraps platform-specific Unicode handling behind a consistent interface
- **Value Object**: Immutable-like behavior (via reference counting) for string data

*Not inferable*: No clear use of other patterns (e.g., no visible Factory, Observer, etc.).
