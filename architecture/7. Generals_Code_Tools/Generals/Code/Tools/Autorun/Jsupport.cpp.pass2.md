# Generals/Code/Tools/Autorun/Jsupport.cpp - Enhanced Analysis

## Architectural Role
This file provides low-level text parsing utilities specifically for Japanese DBCS (Double-Byte Character Set) support, serving as a foundational layer for internationalization in the game's toolchain. It handles character validation and word parsing for mixed single-byte/double-byte text sequences.

## Cross-References
### Incoming
- Not inferable (no callers identified in context)

### Outgoing
- Calls Windows API functions (`IsDBCSLeadByte`, `strchr`)
- Uses Windows types (`BYTE`, `UINT`)

## Design Patterns
- **Utility Class Pattern**: Functions are stateless utilities for text processing
- **Character Validation Table Pattern**: Uses hardcoded byte arrays for DBCS validation rules
- **Early Return Pattern**: Multiple exit points for efficiency in text parsing

(Word count: 100)
