# Generals/Code/Tools/CRCDiff/expander.h

## Purpose
Defines a template expansion class for key/value pair substitution in strings.

## Responsibilities
- Manages a map of key/value pairs for template expansion
- Provides methods to add, clear, and expand templates
- Handles marker-based string replacement

## Key Types
- **ExpansionMap (typedef)**: Alias for `std::map<std::string, std::string>` storing key/value pairs
- **Expander (Class)**: Main class for template expansion functionality

## Key Functions
### Expander::Expander
- Purpose: Constructs an Expander with left/right markers
- Calls: None

### Expander::addExpansion
- Purpose: Adds a key/value pair to the expansion map
- Calls: None

### Expander::clear
- Purpose: Clears all key/value pairs from the expansion map
- Calls: None

### Expander::expand
- Purpose: Expands a template string using the key/value pairs
- Calls: None (implementation not shown)

## Globals
- None

## Dependencies
- `<map>` for `std::map`
- `<hash_map>` (unused in header)
- `<string>` for `std::string`
