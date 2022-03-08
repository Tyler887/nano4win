# Nano For Windows
This program is a "port" of the nano editor to Windows. It is based on MSYS2.
## Install
### Windows PowerShell or PowerShell Core
```powershell
# Compile nano executable. You may need to run: python -m pip install pyinstaller
pyinstaller --noconfirm --onefile --console --name "nano" "C:/Users/<USER ID HERE>/<YOUR NANO SUBDIRECTORY HERE>/nano-msys2.py"
# Preform MSYS2 base installation.
winget install msys2
# Add Nano to the PATH. Do not use SETX as this will truncate the PATH to 1024 characters.
# Set up MSYS2 then launch nano.
nano
```
### Windows Batch
```batch
: Compile nano executable. You may need to run: python -m pip install pyinstaller
pyinstaller --noconfirm --onefile --console --name "nano" "C:/Users/<USER ID HERE>/<YOUR NANO SUBDIRECTORY HERE>/nano-msys2.py"
: Preform MSYS2 base installation.
winget install msys2
: Add Nano to the PATH. Do not use SETX as this will truncate the PATH to 1024 characters.
: Set up MSYS2 then launch nano.
nano
```
## Errors
### `'msys2' is not recognized as an internal or external command, operable program or batch file.`
This is because MSYS2 was not installed (you forgot to install it). Use WinGet to install
MSYS2: `winget install msys2`
### `bash: msys2: command not found`
You executed nano4win on the wrong OS. Simply run `nano` instead.

If you **are using Windows**, you are running a Cygwin interface (e.g.
MSYS2). You can't call `msys2` in a Cygwin interface, you need to call it
from `cmd`, `pwsh`, or `powershell`.
