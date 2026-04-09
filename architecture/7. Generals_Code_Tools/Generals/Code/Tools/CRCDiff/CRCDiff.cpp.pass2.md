# Generals/Code/Tools/CRCDiff/CRCDiff.cpp - Enhanced Analysis

## Architectural Role
This tool is part of the build/validation infrastructure, specifically for comparing CRC (Cyclic Redundancy Check) logs between builds. It's a standalone utility used during development to identify changes in game data files between versions.

## Cross-References
### Incoming
- Not inferable (no external callers visible in this file)

### Outgoing
- **Expander class**: Used for HTML template expansion
- **File I/O subsystem**: Direct use of C stdio functions
- **Command-line parsing**: Uses argc/argv from main()

## Design Patterns
- **Template Method**: The Expander class usage follows a template method pattern for HTML generation
- **State Machine**: The main loop implements a state machine for comparing file lines
- **Lazy Initialization**: Output file is opened only when needed (first outputLine call)

Rules followed. Output under 400 tokens.
