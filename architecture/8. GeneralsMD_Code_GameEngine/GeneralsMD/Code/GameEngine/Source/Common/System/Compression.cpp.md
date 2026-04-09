# GeneralsMD/Code/GameEngine/Source/Common/System/Compression.cpp

## Purpose
Provides compression and decompression functionality for the game, with optional performance testing.

## Responsibilities
- Implements data compression/decompression via `CompressionManager`
- Contains test code for benchmarking different compression methods
- Handles memory allocation/deallocation for test buffers
- Compares original vs. compressed data integrity
- Logs compression statistics

## Key Types
- `CompData` (struct): tracks original and compressed sizes for test data

## Key Functions
### `DoCompressTest`
- Purpose: Benchmarks compression methods using real map files
- Calls: `CompressionManager::getMaxCompressedSize`, `CompressionManager::compressData`, `CompressionManager::decompressData`, `memcmp`, `DEBUG_LOG`, `NEW`, `delete[]`

## Globals
- `s_sizes` (std::map<AsciiString, CompData>): stores compression test results

## Dependencies
- `Compression.h` (header)
- `PreRTS.h`
- `GameClient/MapUtil.h`
- `Common/FileSystem.h`
- `Common/File.h`
- `Common/PerfTimer.h`
- `CompressionManager` class methods
- `TheMapCache`, `TheFileSystem` globals
