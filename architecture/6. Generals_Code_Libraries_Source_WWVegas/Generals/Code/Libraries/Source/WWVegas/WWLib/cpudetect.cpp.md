# Generals/Code/Libraries/Source/WWVegas/WWLib/cpudetect.cpp

## Purpose
This file implements CPU and OS detection functionality for the game engine, including hardware feature detection, performance measurement, and system information logging.

## Responsibilities
- Detect CPU manufacturer, model, and features (CPUID, RDTSC, MMX, SSE, etc.)
- Measure processor speed using RDTSC
- Detect cache sizes and associativity
- Gather OS version information
- Generate detailed system logs

## Key Types
- **OSInfoStruct (struct)**: Contains OS version and build information
- **CPUDetectInitClass (class)**: Singleton initializer for CPU detection
- **CPUDetectClass (class)**: Main CPU detection interface (defined elsewhere)

## Key Functions
### Calculate_Processor_Speed
- Purpose: Measures CPU clock speed using RDTSC instruction
- Calls: TIMEGETTIME

### Get_OS_Info
- Purpose: Determines OS version from version numbers
- Calls: None (uses Windows9xVersionTable)

### CPUDetectClass::CPUID
- Purpose: Executes CPUID instruction and returns results
- Calls: None (inline assembly)

## Globals
- **_CPU_Detect_Init (CPUDetectInitClass)**: Singleton initializer
- **Windows9xVersionTable (OSInfoStruct[])**: Lookup table for Windows 9x versions

## Dependencies
- Key includes: cpudetect.h, wwstring.h, wwdebug.h, thread.h, mpu.h, windows.h, systimer.h
- External symbols: TIMEGETTIME, VER_PLATFORM_*, GetTimeZoneInformation (Windows)
