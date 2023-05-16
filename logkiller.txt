@echo off
color 7
title Log Killer
echo  -====================================================-
echo -=    ____                ____ _                 _   =-
echo -=   / ___|___  _ __ ___ / ___| | ___  _   _  __| |  =-
echo -=  | |   / _ \| '__/ _ \ |   | |/ _ \| | | |/ _` |  =-
echo -=  | |__| (_) | | |  __/ |___| | (_) | |_| | (_| |  =-
echo -=   \____\___/|_|  \___|\____|_|\___/ \__,_|\__,_|  =-
echo -=       Corecloud Log killer v20230516              =-
echo -=   This tool going to delete all logs !            =-
echo  -====================================================-
timeout 5
for /F "tokens=*" %%G in ('wevtutil.exe el') DO (call :clear "%%G")
echo.
echo logs has deleted
goto :theEnd
timeout 5
:clear
echo [+] %1
wevtutil.exe cl %1
goto :eof
:theEnd
timeout 3
