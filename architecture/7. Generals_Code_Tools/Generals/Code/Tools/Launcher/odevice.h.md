# Generals/Code/Tools/Launcher/odevice.h

## Purpose
Defines an abstract base class for output devices used in the debugging system.

## Responsibilities
- Declares a virtual interface for output devices
- Provides a pure virtual `print` method for text output
- Serves as a base class for concrete output implementations

## Key Types
- **OutputDevice (Class)**: Abstract base class for output devices in the debugging system

## Key Functions
### OutputDevice()
- Purpose: Default constructor
- Calls: None

### ~OutputDevice()
- Purpose: Virtual destructor
- Calls: None

### print(const char *s, int len)
- Purpose: Pure virtual method to output text
- Calls: None

## Globals
- None

## Dependencies
- None (header-only, no includes)
