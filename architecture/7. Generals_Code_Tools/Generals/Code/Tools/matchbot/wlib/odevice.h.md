# Generals/Code/Tools/matchbot/wlib/odevice.h

## Purpose
Defines an abstract base class for output devices used in debugging.

## Responsibilities
- Declares a virtual interface for output devices
- Provides a pure virtual `print` method for text output
- Serves as a base class for concrete output implementations

## Key Types
- **OutputDevice (Class)**: Abstract base class for output devices with a `print` interface.

## Key Functions
### OutputDevice()
- Purpose: Default constructor.
- Calls: None.

### ~OutputDevice()
- Purpose: Virtual destructor.
- Calls: None.

### print(const char *s, int len)
- Purpose: Pure virtual method to output a string of specified length.
- Calls: None.

## Globals
- None.

## Dependencies
- None (header-only, no includes or external symbols).
