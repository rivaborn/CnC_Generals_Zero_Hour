# Generals/Code/Tools/Launcher/Toolkit/Support/UTypes.h

## Purpose
Defines generic user type aliases for consistent integer, floating-point, and character types across the codebase.

## Responsibilities
- Provides typed aliases for integers (8/16/32-bit signed/unsigned)
- Defines floating-point type aliases (32/64-bit)
- Declares character types (ASCII, Unicode)
- Introduces a TriState enum for three-state logic

## Key Types
- Int (Class): signed integer alias
- UInt (Class): unsigned integer alias
- Int8 (Class): signed 8-bit integer
- UInt8 (Class): unsigned 8-bit integer
- Int16 (Class): signed 16-bit integer
- UInt16 (Class): unsigned 16-bit integer
- Int32 (Class): signed 32-bit integer
- UInt32 (Class): unsigned 32-bit integer
- Char (Class): signed character (ASCII)
- UChar (Class): unsigned character (ANSI)
- WChar (Class): wide character (Unicode)
- Float32 (Class): 32-bit floating-point
- Float64 (Class): 64-bit floating-point
- Float (Class): 32-bit floating-point alias
- TriState (Class): three-state enum (OFF/ON/PENDING)

## Key Functions
None

## Globals
- NULL (macro): defines null pointer (0L)

## Dependencies
- None (header-only, no external symbols)
