# Generals/Code/Tools/mangler/wlib/odevice.h

## Purpose
Defines a virtual base class for output devices used in the debugging package.

## Responsibilities
- Provides an interface for output devices
- Declares pure virtual `print` method
- Manages construction/destruction lifecycle

## Key Types
- **OutputDevice (Class)**: Abstract base class for output devices with a print interface.

## Key Functions
### OutputDevice()
- Purpose: Default constructor.
- Calls: None.

### ~OutputDevice()
- Purpose: Virtual destructor.
- Calls: None.

### print(const char *s, int len)
- Purpose: Pure virtual method to output a string of given length.
- Calls: None.

## Globals
- None.

## Dependencies
- None.
