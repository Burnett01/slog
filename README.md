# slog
Advanced logging library for C/C++ which parses log level from config file and prints log if log level is equal or higher than level while printing with slog() function.

# Simple API
At first you must initialise slog
```
slog_init("filename", 1, 3);
```
First argument "filename" is a filename where logs will be saved.
File name will be generated from argument and also from system date.
Finally file name will be something like that:
```
filename-2015-04-02.log
```

Second argument is for enabling/disabling log to file.

Enable   | Disable
---------|---------
1        | 0

If 1 is given, logs will be saved in file, but it wont if argument is 2.

Third argument is maximum of log levels.

# Usage
```
slog(0, "[LIVE] Test message with level 0");
```
Where first argument is log level and second is message to print and/or save.
