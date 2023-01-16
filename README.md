# .NET Core Console App as a Windows Service
+ .NET Core 3.1
+ Console Application (C#)
+ Windows Service (C#)
+ System.Data.SqlClient Version 4.8.5
+ Dapper 2.0.123
+ Dapper.Contrib 2.0.78
+ Gmail SMTP with App Password Port 587

# Guide
+ .Net Core Console App As A Windows Service: https://www.initpals.com/net-core/net-core-console-app-as-a-windows-service/

+ Solution File: 	d:\CoreWinService\net_core_console_as_windows_service\My.Core.Windows.Service.sln
+ Project File: 	d:\CoreWinService\net_core_console_as_windows_service\MyCoreWindowsService\My.Core.Windows.Service.csproj

+ Change directory
<pre>
cd "d:\CoreWinService\net_core_console_as_windows_service\MyCoreWindowsService"
</pre>

+ Build
</pre>
dotnet publish "My.Core.Windows.Service.csproj" --configuration Release -o "C:\Tools\SqlServerConn"
</pre>

+ Create Windows Service
<pre>
sc create CoreWinService binPath= "C:\Tools\SqlServerConn\My.Core.Windows.Service.exe"
sc start CoreWinService
sc stop CoreWinService
sc delete CoreWinService
</pre>

# References
+ Please read the article https://www.initpals.com/net-core/net-core-console-app-as-a-windows-service/ for step by step instructions
