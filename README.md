# mvTools
This library is meant to be a set of tools for MVDB systems (UniVerse/OpenQM).
## mvLog
This tool is a simple logging subroutine.
`SUBROUTINE MVLOG(I.TAG, I.TEXT, I.PGM, RV5, RV4, RV3, RV2, RV1)
   I.TAG (in): Small keyword to identify the log record.
   I.TEXT (in): Whatever you want to be logged.
   I.PGM (in): Program name that calls that subr.
   O.ID (out): ID of the new record, to return to calling pgm.
   O.MSG (out): Message for the calling program. If something is wrong while logging the info, details will be provided there.  Otherwise, it will returns "OK".
   RV4,3,2,1: Reserved for future usage.`

### Setup
Update EQUate FILE.NAME to the file name where you want the log record to be created.

### Tags
Tags are small keywords to identify a group of log.
Each individual tags are stored in the DICT part of the log file, to an item $$TAG*_tag_.
The 2nd attribute of that DICT item is the last sequential number used to create the Record Key.