# Generals/Code/Tools/WW3D/pluglib/borlandc.h

## Purpose
Header file for Borland C++ compiler compatibility in the WW3D plugin library.

## Responsibilities
- Defines `BORLANDC_H` guard when using Borland C++ compiler
- Notes that Borland C++ closely matches C++ standards
- Includes conditional `#pragma once` for MSVC compatibility

## Key Types
- None

## Key Functions
- None

## Globals
- None

## Dependencies
- Uses `__BORLANDC__` macro (compiler intrinsic)
- Uses `_MSC_VER` macro (MSVC compiler intrinsic)
