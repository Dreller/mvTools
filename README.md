# mvTools
This library is meant to be a set of tools for MVDB systems (UniVerse/OpenQM).



## mvLog
This tool is a simple logging subroutine.
```
SUBROUTINE MVLOG(TAG, LEVEL, TEXT, PGM, ID, MSG, RV4, RV3, RV2, RV1)
   TAG (in): Small keyword to identify the log record.
   LEVEL (in): Level of priority for that log.
   TEXT (in): Whatever you want to be logged.
   PGM (in): Program name that calls that subr.
   ID (in/out): ID of the new record, to return to calling pgm.
   MSG (out): Message for the calling program. If something is wrong while logging the info, details will be provided there.  Otherwise, it will returns "OK".

   RV4,3,2,1: Reserved for future usage.
```
### Levels
Accepted levels are:
- FATAL
- ERROR
- WARN
- INFO
- DEBUG

### Setup
- Update EQUate **FILE.NAME** to the file name where you want the log record to be created.

#### Optional
- Update the EQUate **DEFAULT.LEVEL** to the default Level you want to use if the passed level is not valid.

### Tags
Tags are small keywords to identify a group of log.
Each individual tags are stored in the DICT part of the log file, to an item $$TAG*_tag_.
The 2nd attribute of that DICT item is the last sequential number used to create the Record Key.

### Usage
Note: If you want to append logs to an existing Log Record, simply pass the ID of the existing record.


## mvDICT
Tool to create DICT items
(To write)
