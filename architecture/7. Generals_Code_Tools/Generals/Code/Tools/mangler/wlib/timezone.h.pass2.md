# Generals/Code/Tools/mangler/wlib/timezone.h - Enhanced Analysis

## Architectural Role
This header provides timezone utility functions for the build/mangler tools, enabling timezone-aware operations during asset processing. It abstracts platform-specific timezone logic, ensuring consistent behavior across build environments.

## Cross-References
### Incoming
- `Generals/Code/Tools/matchbot/wlib/timezone.h` (duplicate header, likely for tool consistency)
- Build/mangler tools that require timezone info for timestamp handling or log generation

### Outgoing
- Platform-specific timezone APIs (not inferable from header)
- Likely calls into C runtime for timezone data (e.g., `_tzset()`, `localtime()`)

## Design Patterns
- **Facade Pattern**: Wraps complex timezone logic behind simple functions
- **Static Data Caching**: Returns const string/offset, suggesting internal caching
- **Reference Parameter**: Uses output parameters for `GetTimezoneInfo` to avoid struct allocation

*Not inferable: No clear use of Singleton or Factory patterns.*
