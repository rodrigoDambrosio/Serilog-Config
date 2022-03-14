# Serilog-Config

# Main

´´´ using Serilog; //also add libs like el sink file

string pathLog= @"C:\Logs\LogComplemento3_.txt";
Log.Logger = new LoggerConfiguration()
    .MinimumLevel.Debug()
    .WriteTo.File(pathLog, rollingInterval: RollingInterval.Day)
    .CreateLogger();


´´´

# Add log entry

´´´ Log.Information(" Hi ! "); ´´´
I can use Log.Debug Log.Error for example

Logging in other class

Log.X and don't forget the using of Serilog

# Userfull info
Each line has date-time stamp, Serilog concats the date-time automatically to the filename.
