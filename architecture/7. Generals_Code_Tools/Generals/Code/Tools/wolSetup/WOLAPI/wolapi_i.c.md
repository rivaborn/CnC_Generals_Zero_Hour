# Generals/Code/Tools/wolSetup/WOLAPI/wolapi_i.c

## Purpose
Defines COM interface identifiers (IIDs) and class identifiers (CLSIDs) for the WOLAPI library.

## Responsibilities
- Declares IID and CLSID constants for various COM interfaces
- Provides type definitions for IID and CLSID
- Exposes identifiers for chat, download, network utility, and patcher components

## Key Types
- IID (struct): Interface identifier structure
- CLSID (typedef): Class identifier (alias for IID)

## Key Functions
None

## Globals
- IID_IRTPatcher (IID): Interface ID for RTPatcher
- IID_IRTPatcherEvent (IID): Event interface ID for RTPatcher
- IID_IChat (IID): Interface ID for chat functionality
- IID_IChatEvent (IID): Event interface ID for chat
- IID_IDownload (IID): Interface ID for download functionality
- IID_IDownloadEvent (IID): Event interface ID for download
- IID_INetUtil (IID): Interface ID for network utilities
- IID_INetUtilEvent (IID): Event interface ID for network utilities
- IID_IChat2 (IID): Second version of chat interface ID
- IID_IChat2Event (IID): Event interface ID for chat version 2
- IID_IIGROptions (IID): Interface ID for IGROptions
- LIBID_WOLAPILib (IID): Library ID for WOLAPI
- CLSID_RTPatcher (CLSID): Class ID for RTPatcher
- CLSID_Chat (CLSID): Class ID for chat component
- CLSID_Download (CLSID): Class ID for download component
- CLSID_IGRO
