### Ticket Number: 003
### Title: USB Drive Not Mounting on Windows
### Date: 2026-09-19
### Category: Hardware

**Reported Issue:**
User reported SanDisk 32GB USB flash drive was not mounting on Windows. Drive not showing in File Explorer and could not access files.

**Root Cause:**
File system was corrupted / RAW partition after unsafe removal. Drive showed as unallocated with no file system in Disk Management.

**Troubleshooting Steps:**
1. Plugged USB into Windows PC and checked File Explorer - drive not visible
2. Opened Disk Management - drive appeared as RAW / No file system
3. Right-clicked drive to check properties - confirmed file system corruption
4. Formatted drive via Disk Management

**Solution:**
Fixed by formatting USB on Windows. Opened Disk Management > Right-click USB > Format > FAT32, Quick Format enabled. After format, safely ejected and re-plugged. Drive mounted with drive letter and became accessible.

**Time to Resolve:** 10 min
**Prevention:** Always safely eject USB via "Safely Remove Hardware" before unplugging. Use FAT32 or ExFAT for cross-platform compatibility.
