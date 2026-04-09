# Generals/Code/Tools/Autorun/GetCD.h - Enhanced Analysis

## Architectural Role
This header defines the CD drive detection and verification infrastructure for the game's autorun system, bridging legacy CD-ROM access with modern drive enumeration. It serves as the foundation for CD-based content verification during installation or launch.

## Cross-References
### Incoming
- Likely called by installation/autorun tools (e.g., `Generals/Code/Tools/Autorun/main.cpp`) for CD validation
- Potentially referenced by legacy audio systems (if RedBook functionality is used)

### Outgoing
- Depends on DPMI real-mode functions (Win95 only) for legacy CD audio control
- Uses global volume label array (`_CD_Volume_Label`) for verification

## Design Patterns
- **Singleton Pattern**: Global `CDList` instance provides centralized CD drive management
- **Adapter Pattern**: `RedBookClass` adapts legacy CD audio interfaces for Win95 compatibility
- **Iterator Pattern**: `Get_First_CD_Drive`/`Get_Next_CD_Drive` pair enables sequential drive enumeration

*Not inferable*: Exact usage patterns in calling code (e.g., error handling, retry logic).
