# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/regexpr.cpp

## Purpose
Implements a C++ wrapper for GNU regex library, providing regular expression compilation and matching functionality.

## Responsibilities
- Wraps GNU regex library calls for pattern compilation and string matching
- Manages regex syntax options and memory cleanup
- Provides C++ interface with RAII for regex patterns
- Supports pattern comparison and assignment operations

## Key Types
- **RegularExpressionClass::DataStruct (Class)**: Internal data structure holding compiled regex pattern and state
- **RegularExpressionClass (Class)**: Main regex wrapper class

## Key Functions
### RegularExpressionClass::Compile
- Purpose: Compiles a regex pattern string into an internal format
- Calls: Data->ClearExpression(), re_set_syntax(), re_compile_pattern()

### RegularExpressionClass::Match
- Purpose: Tests if a string matches the compiled regex pattern
- Calls: re_set_syntax(), re_match()

### RegularExpressionClass::operator=
- Purpose: Assigns one regex object to another by recompiling the pattern
- Calls: Compile()

## Globals
- **OUR_SYNTAX_OPTIONS (macro)**: Defines the regex syntax flags used by this implementation

## Dependencies
- "regexpr.h" (header for this class)
- "wwstring.h" (for StringClass)
- "gnu_regex.h" (external regex library)
- <assert.h> (for assertions)
