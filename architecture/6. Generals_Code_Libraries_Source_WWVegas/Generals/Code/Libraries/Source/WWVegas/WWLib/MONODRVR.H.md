# Generals/Code/Libraries/Source/WWVegas/WWLib/MONODRVR.H

## Purpose
Header file defining IOCTL codes and structures for a monochrome display driver interface.

## Responsibilities
- Defines device type and IOCTL codes for monochrome display driver
- Declares MonoFlagType enum for driver behavior flags
- Provides example usage of the driver interface
- Includes Windows-specific headers for IOCTL support

## Key Types
- MonoFlagType (enum): flags controlling monochrome driver behavior (e.g., text wrapping)

## Key Functions
None: This is a header file with no function implementations.

## Globals
None

## Dependencies
- winioctl.h: for Windows IOCTL definitions
- CTL_CODE macro: from Windows SDK for control code generation
