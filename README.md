---
title: PowerShell Style Guide
---

- Code must use One True Brace Style (OTBS)
- Code must be indented between braces
- Indents must use 4 spaces
- Functions must always start with CmdletBinding
- Functions must include a Begin, Process and End blocks
- Function and variable names should use PascalCase
- A whitespace is required before an open brace
- A whitespace is required before an open paren
- A whitespace is required around operators
- A whitespace is required after a seperator
- There should be no trailing whitespace on lines
- Code must not use aliases
- Parameters should be called by parameter name not parameter position
- All files must end on a new line

Example:

```powershell
Function Test-Code {
    [CmdletBinding()]
    Param(
        [int]$ParameterOne
    )

    Begin {}

    Process {
        If (10 -gt $ParameterOne) {
            'Greater'
        } Else {
            'Lesser'
        }
    }

    End {}
}

```
