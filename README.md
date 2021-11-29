# OSD Volume Popup Mover

Moves the Windows 10 volume control popup when you mouse over it. The app shows itself as an icon in the system tray.

## Installation

[Download](https://github.com/driazati/windows-volume-popup-mover/releases/tag/v1.0.0) the `.exe` (the `.exe` is unsigned so Chrome and Windows will complain, build from source to avoid these warnings).

### From Source

Install [Visual Studio](https://visualstudio.microsoft.com/downloads/) first (requires MSBuild and .NET 4.7.2).

```bash
# (optional) Find MSBuild.exe
Get-ChildItem -Path C:\ -Filter MSBuild.exe -Recurse -ErrorAction SilentlyContinue -Force

git clone https://github.com/driazati/windows-volume-popup-mover.git
cd windows-volume-popup-mover
MSBuild.exe OSDMover.sln /p:Configuration=Release


./bin/Release/OSDMover.exe
```

