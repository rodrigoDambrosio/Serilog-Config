# Serilog-Config

# Main

```
using Serilog; //also add libs like sink file

string pathLog= @"C:\Logs\MyAppLog.txt";
Log.Logger = new LoggerConfiguration()
    .MinimumLevel.Debug()
    .WriteTo.File(pathLog, rollingInterval: RollingInterval.Day)
    .CreateLogger();
```
### With great powers comes great responsibility, dont forget to close the file

```Log.CloseAndFlush();```

# Add log entry

```
Log.Information(" Hi ! ");
```
I can use Log.Debug Log.Error for example

# Variables
```Log.Information("The value of Car is {Car}", Car);```

# Logging in other class

Log.X and don't forget the using of Serilog

# Userfull info
Each line has date-time stamp, Serilog also concats the date automatically to the filename.
The output will be like MyAppLog_20220309
