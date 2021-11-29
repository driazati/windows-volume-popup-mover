# OSD Volume Popup Mover

Moves the Windows 10 volume control popup when you mouse over it. The app shows itself as an icon in the system tray.

## Installation

[Download](https://github.com/driazati/windows-volume-popup-mover/releases/tag/v1.0.0) the `.exe` (the `.exe` is unsigned so Chrome and Windows will complain, build from source to avoid these warnings).

### From Source

Install [Visual Studio](https://visualstudio.microsoft.com/downloads/) first (requires MSBuild and .NET 4.7.2). Then in Powershell:

```powershell
# (optional) Find MSBuild.exe
Get-ChildItem -Path C:\ -Filter MSBuild.exe -Recurse -ErrorAction SilentlyContinue -Force

# Get the code
git clone https://github.com/driazati/windows-volume-popup-mover.git
cd windows-volume-popup-mover

# Build it
MSBuild.exe OSDMover.sln /p:Configuration=Release

# Run it
./bin/Release/OSDMover.exe

# Copy it to the startup folder to run it automatically
Copy-Item .\bin\Release\OSDMover.exe -Destination $env:APPDATA\Microsoft\Windows\"Start Menu"\Programs\Startup
```
