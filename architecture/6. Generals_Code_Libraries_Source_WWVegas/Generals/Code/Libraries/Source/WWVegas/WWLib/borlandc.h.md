# Generals/Code/Libraries/Source/WWVegas/WWLib/borlandc.h

## Purpose
Header file to handle Borland C++ compiler compatibility for the SAGE engine.

## Responsibilities
- Conditionally defines `BORLANDC_H` when using Borland C++ compiler
- Includes compiler-specific pragmas for MSVC
- Notes Borland C++'s compliance with C++ standards

## Key Types
- None

## Key Functions
- None

## Globals
- None

## Dependencies
- Uses `_MSC_VER` (MSVC version macro)
- Uses `__BORLANDC__` (Borland C++ compiler macro)
