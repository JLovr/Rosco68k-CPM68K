# Rosco68k-CPM68K
A set of disks providing base CPM support for the Rosco68K kit computer.

This is a work in progress.  Assembled from various sources.
Includes:
A:  A working environment. Finished.
C:  A general CP/M-68K disk set repository.  Finished
D:  BASIC development environment acquired from Malcolm Harrow WIP
F:  DISK for Forth Development - WIP
G:  RED editor development disk - WIP
H:  MEMACS editor development disk - WIP
I:  CPM object and header files.  Finished.
J:  X, Transfer utility files and SUBS.

Incorporated on othe A drive are two sub files to set up the memory drive (B:) as a workspace.
  REDWKSP.SUB
  MEMACSWK.SUB
Required for use:
  1.5 MEG ram drive
  1 Meg Memory
This permits a user to work on either RED or MEMACS (Not both at once) with all project modules being available.
Doing that requires a large RAMdrive.  However you can set up your own if you just need to work on one of the modules.
That might fit in a 512K Ramdrive.

Both MEMACS and RED compile, but are nonfunctional.  I have already made changes to the code on these disks to permit
them to compile using the Alcyon compiler that came with CP/M-68K.

Issues experienced that have been addressed are as follows:
  Nested Includes (not supported)
  Limits on the size of variable names (less than 8 characters).
  Missing functions (BDOS, BIOS direct access)
  I have already added the BDOS function to CLIB to reduce clutter and to make working with OS routines directly
  easier.

Remaining Issues: Debugging RED.REL and MEMACS (ME.REL) for now.  RED has a problme with a switch structure with duplicate cases:
