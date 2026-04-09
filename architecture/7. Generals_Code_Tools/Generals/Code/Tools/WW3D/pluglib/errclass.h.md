# Generals/Code/Tools/WW3D/pluglib/errclass.h

## Purpose
Defines a simple error handling class for managing formatted error messages.

## Responsibilities
- Stores formatted error messages
- Handles memory allocation/deallocation for messages
- Supports copy construction and assignment

## Key Types
- ErrorClass (Class): wraps a formatted error message string

## Key Functions
### ErrorClass(char * format,...)
- Purpose: Constructs an ErrorClass with a formatted error message
- Calls: va_start, vsprintf, va_end, strdup

### ErrorClass(const ErrorClass & that)
- Purpose: Copy constructor for ErrorClass
- Calls: operator=

### operator=(const ErrorClass & that)
- Purpose: Assignment operator for ErrorClass
- Calls: free, strdup

## Globals
- None

## Dependencies
- <stdarg.h>
- strdup, free, strlen, assert, vsprintf, va_list, va_start, va_end
