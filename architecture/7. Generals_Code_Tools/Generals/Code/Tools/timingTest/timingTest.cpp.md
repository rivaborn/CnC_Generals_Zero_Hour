# Generals/Code/Tools/timingTest/timingTest.cpp

## Purpose
This file implements a precision timer benchmark tool for measuring CPU clock cycles per millisecond/second.

## Responsibilities
- Measures CPU clock cycles using RDTSC instruction
- Calculates ticks per second/millisecond via calibration
- Outputs timing data to console and file
- Performs looping tests with Sleep() to measure overhead

## Key Types
- None

## Key Functions
### GetPrecisionTimer
- Purpose: Reads CPU time-stamp counter into provided INT64 pointer
- Calls: None (inline assembly)

### InitPrecisionTimer
- Purpose: Calibrates timer by measuring ticks over 1-second intervals
- Calls: GetPrecisionTimer, timeGetTime, cout, sprintf

### main
- Purpose: Runs benchmark loop and outputs timing statistics
- Calls: InitPrecisionTimer, GetPrecisionTimer, Sleep, fopen/fwrite/fflush/fclose, cout, sprintf

## Globals
- s_ticksPerSec (double): Stores calibrated ticks per second
- s_ticksPerMSec (double): Stores calibrated ticks per millisecond
- buffer (char[1024]): Temporary string buffer for output formatting

## Dependencies
- windows.h, mmsystem.h, iostream.h, string.h
- timeGetTime, Sleep, fopen/fwrite/fflush/fclose
- cout, sprintf
