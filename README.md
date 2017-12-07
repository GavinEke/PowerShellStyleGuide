# PowerShell Style Guide

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt).

- Code MUST use One True Brace Style (OTBS)
- Code MUST be indented between braces
- Indents MUST use 4 spaces
- Functions MUST always start with CmdletBinding
- Functions MUST include a Begin, Process and End blocks
- Function and variable names SHOULD use PascalCase
- A whitespace is REQUIRED before an open brace
- A whitespace is REQUIRED before an open paren
- A whitespace is REQUIRED around operators
- A whitespace is REQUIRED after a seperator
- There SHOULD be no trailing whitespace on lines
- Code MUST NOT use aliases
- Parameters SHOULD include a HelpMessage
- Parameters SHOULD be called by parameter name
- All files MUST end on a new line

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
