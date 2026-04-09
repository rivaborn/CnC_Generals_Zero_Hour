# Generals/Code/Tools/wolSetup/StdAfx.h

## Purpose
Precompiled header file for the wolSetup tool, including standard system headers and project-specific common includes.

## Responsibilities
- Defines include guards for the header
- Includes Windows API headers with minimal features
- Provides a placeholder for additional project-specific includes
- Supports Microsoft Visual C++ precompilation directives

## Key Types
None

## Key Functions
None

## Globals
None

## Dependencies
- `<windows.h>`: Windows API headers
- `WIN32_LEAN_AND_MEAN`: Macro to reduce Windows header bloat
- Visual C++ precompilation directives (`#pragma once`, `#if _MSC_VER`)
