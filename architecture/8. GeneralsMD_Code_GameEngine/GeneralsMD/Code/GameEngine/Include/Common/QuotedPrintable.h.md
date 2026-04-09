# GeneralsMD/Code/GameEngine/Include/Common/QuotedPrintable.h

## Purpose
Header file declaring functions for quoted-printable encoding/decoding between ASCII and Unicode strings.

## Responsibilities
- Declares quoted-printable encoding/decoding functions
- Provides conversions between ASCII and Unicode strings
- Supports both ways of conversion (to/from quoted-printable)

## Key Types
None

## Key Functions
### QuotedPrintableToUnicodeString
- Purpose: Converts quoted-printable encoded ASCII string to Unicode string
- Calls: Not inferable

### UnicodeStringToQuotedPrintable
- Purpose: Converts Unicode string to quoted-printable encoded ASCII string
- Calls: Not inferable

### QuotedPrintableToAsciiString
- Purpose: Converts quoted-printable encoded ASCII string to regular ASCII string
- Calls: Not inferable

### AsciiStringToQuotedPrintable
- Purpose: Converts ASCII string to quoted-printable encoded ASCII string
- Calls: Not inferable

## Globals
None

## Dependencies
- Uses `UnicodeString` and `AsciiString` types (not defined here)
- Likely depends on string manipulation utilities
