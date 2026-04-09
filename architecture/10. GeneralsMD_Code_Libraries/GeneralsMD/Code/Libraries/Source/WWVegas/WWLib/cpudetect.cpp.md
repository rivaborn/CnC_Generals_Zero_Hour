# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/cpudetect.cpp

## Purpose
This file implements CPU and OS detection functionality for the game engine, including hardware feature detection, performance measurement, and system information logging.

## Responsibilities
- Detect CPU manufacturer, model, features (CPUID, RDTSC, MMX, SSE, etc.)
- Measure processor speed using RDTSC
- Detect cache sizes and associativity
- Gather OS version information (Windows 9x/NT/XP)
- Log system information in human-readable and compact formats

## Key Types
- **OSInfoStruct (struct)**: Contains OS version and build information
- **CPUDetectInitClass (class)**: Singleton initializer for CPU/OS detection
- **CPUDetectClass (class)**: Main detection class (defined elsewhere)

## Key Functions
### Calculate_Processor_Speed
- Purpose: Measures CPU clock speed using RDTSC and system timer
- Calls: TIMEGETTIME(), inline assembly for RDTSC

### Get_OS_Info
- Purpose: Determines OS version from version info
- Calls: None (uses Windows API via globals)

### CPUDetectClass::Process_Cache_Info
- Purpose: Interprets CPUID cache descriptor values
- Calls: None

### CPUDetectClass::Init_Processor_Log
- Purpose: Generates human-readable system information log
- Calls: Get_Processor_String(), Get_Processor_Speed(), etc.

## Globals
- **_CPU_Detect_Init (CPUDetectInitClass)**: Singleton initializer
- **Windows9xVersionTable (OSInfoStruct[])**: Lookup table for Windows 9x versions

## Dependencies
- Key includes: cpudetect.h, wwstring.h, windows.h, systimer.h
- External symbols: TIMEGETTIME(), GetTimeZoneInformation(), Windows API version info
