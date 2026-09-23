### Ticket Number: 004
### Title: USB Drive Not Visible on macOS After Windows Format
### Date: 2026-09-20
### Category: Hardware / OS

**Reported Issue:**
User formatted USB on Windows and it worked. When the same USB was plugged into MacBook Air 2015, it could not be seen on Desktop or Finder.

**Root Cause:**
USB was formatted as NTFS / Microsoft Basic Data on Windows. macOS cannot write to NTFS and does not mount it on Desktop, so it appeared as Microsoft Basic Data in diskutil but not in Finder.

**Troubleshooting Steps:**
1. Plugged USB into Mac and checked Desktop / Finder - drive not visible
2. Ran diskutil list external - drive showed as 31.5GB with type Microsoft Basic Data
3. Ran ls /Volumes/ - MYUSB not listed, confirming it was not mounted
4. Confirmed formatting issue - NTFS from Windows format incompatible with macOS

**Solution:**
Fixed by re-formatting USB to cross-platform format. On macOS ran diskutil eraseDisk ExFAT MYUSB MBR /dev/disk2 (use FAT32 for 32GB and below). After erase, drive mounted automatically and appeared on Desktop.

**Time to Resolve:** 15 min
**Prevention:** For drives used on both Windows and macOS, always format as ExFAT with MBR. Avoid NTFS if you need to use the drive on Mac. Always check format compatibility before cross-platform use.
