# Generals/Code/Tools/ParticleEditor/CButtonShowColor.cpp - Enhanced Analysis

## Architectural Role
This file is part of the Particle Editor tooling infrastructure, providing a UI component for color visualization. It bridges the MFC-based tooling framework with the game's color representation system, ensuring consistent color handling across editor tools.

## Cross-References
### Incoming
- Likely called by other Particle Editor UI components that need color preview functionality
- May be referenced by WorldBuilder (as seen in cross-references) for similar color display needs

### Outgoing
- Uses Windows GDI (CPaintDC, CPen, CBrush) for rendering
- Relies on MFC message handling infrastructure (BEGIN_MESSAGE_MAP)
- Depends on ParticleSys.h for color type definitions

## Design Patterns
- **Adapter Pattern**: Converts between RGB and BGR formats to interface with Windows GDI
- **Template Method**: Uses MFC's message map pattern for UI event handling
- **Not inferable**: No clear use of other patterns from this file alone

(Word count: 150)
