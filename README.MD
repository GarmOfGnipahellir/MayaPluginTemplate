# Maya Plugin Template
Easy Maya VSCode setup for plugin development.
## Maya
userSetup.py
* Windows: `%USER%/Documents/maya/<ver>/scripts/`
* Mac OS: `$HOME/Library/Prefences/Autodesk/maya/<ver>/scripts/`
``` python
# userSetup.py
import maya.cmds as cmds
# Open new ports
cmds.commandPort(name=":7001", sourceType="mel", echoOutput=True)
cmds.commandPort(name=":7002", sourceType="python", echoOutput=True)
```
## VS Code
### Extensions
* [Python extension](https://github.com/Microsoft/vscode-python)
* [MayaPort extension](https://github.com/NCCA/mayaport)
### Settings
``` json
// .vscode/settings.json
// Windows
{
    "python.pythonPath": "C:/Program Files/Autodesk/maya<ver>/bin/mayapy.exe",
}
// Mac OS:
{
    "python.pythonPath": "/Applications/Autodesk/maya<ver>/Maya.app/Contents/bin/mayapy"
}
```