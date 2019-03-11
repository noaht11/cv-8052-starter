# CV-8052-starter

This is a basic empty project for using Visual Studio Code to write assembly for the CV-8052 Soft Processor to be run on an Altera DE0-CV.
This means you don't have to use CrossIDE as your editor if you don't want to.
Compilation and flashing can be done from within VS Code (through custom tasks) although you do need CrossIDE installed.

# Prerequisites

* CrossIDE
* Quartus

# Setup

1. Install CrossIDE and Quartus if you haven't already (try to make sure these are installed in folders without spaces - I haven't tested this on an install with spaces in the paths)
1. Clone the repo
1. Open the root folder in VS Code
1. Open the `.vscode/tasks.json` file
1. Update the paths to your CrossIDE and Quartus installation if they differ from what's already there:
```
"env": {
    // Modify these paths to match the install locations for CrossIDE and Quartus on your system
    // Don't include trailing slashes
    "CROSSIDE_PATH": "C:\\CrossIDE",
    "QUARTUS_PATH": "C:\\intelFPGA_lite\\18.1\\quartus"
}
```

# Usage

1. Open the assembly file you want to assemble / flash
1. Open the task runner (Ctrl+Alt+T is the default shortcut)
1. Choose `Assemble (A51)`
1. Open the task runner again
1. Choose `Flash (Quartus SignalTap II)`

Note: You can assemble in one step (assuming you have the default shortcuts) by hitting Ctrl+Shift+B

# Syntax Highlighting

You can install this extension: https://marketplace.visualstudio.com/items?itemName=junwatu.8051 to get syntax highlighting on the 8051 assembly (doesn't seem to support all the A51 assembler directives though)
