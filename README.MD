# Black Box Maya Plugin Template
## Workspace Setup
### Maya
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
### VS Code
[Python extension](https://github.com/Microsoft/vscode-python)