# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/regexpr.h

## Purpose
Header file defining a wrapper class for regular expression evaluation using GNU regex library.

## Responsibilities
- Encapsulate GNU regex functionality in a C++ class
- Provide simple interface for compiling and matching regex patterns
- Handle regex compilation errors and validity checks

## Key Types
- **RegularExpressionClass (Class)**: Wrapper for GNU regex evaluation
- **DataStruct (Class)**: Private struct holding regex implementation details

## Key Functions
### RegularExpressionClass::Compile
- Purpose: Compiles a regex pattern string into an internal representation
- Calls: Not inferable (implementation in .cpp)

### RegularExpressionClass::Is_Valid
- Purpose: Checks if the compiled regex is valid
- Calls: Not inferable

### RegularExpressionClass::Match
- Purpose: Tests if a string matches the compiled regex pattern
- Calls: Not inferable

### RegularExpressionClass::operator=
- Purpose: Assignment operator for RegularExpressionClass objects
- Calls: Not inferable

### RegularExpressionClass::operator==
- Purpose: Equality comparison for RegularExpressionClass objects
- Calls: Not inferable

### RegularExpressionClass::operator!=
- Purpose: Inequality comparison for RegularExpressionClass objects
- Calls: Not inferable

## Globals
None

## Dependencies
- GNU regex library (referenced in comments)
- Standard C++ headers (not shown in header)
