# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DOverlordAircraftDraw.h - Enhanced Analysis

## Architectural Role
This file defines a specialized rendering module for aircraft units that receive portable structure upgrades (e.g., Helix, Spectre Gunship). It extends the W3D rendering pipeline to ensure proper draw order of rider units attached to aircraft, bypassing normal containment visibility rules.

## Cross-References
### Incoming
- **W3DModelDraw.h**: Base class inheritance
- **Thing.h**: Constructor parameter (Thing* thing)
- **MultiIniFieldParse.h**: Used in buildFieldParse()

### Outgoing
- **W3DModelDraw**: Parent class methods (doDrawModule, setHidden)
- **Memory pool macros**: For object allocation tracking

## Design Patterns
- **Template Method**: doDrawModule() provides aircraft-specific draw logic while inheriting from W3DModelDraw
- **Module Pattern**: Encapsulates aircraft draw behavior as a reusable component
- **Memory Pool**: Uses custom allocator for performance-critical rendering objects

*Not inferable*: Exact rider access mechanism or draw order coordination with OverlordContain.
