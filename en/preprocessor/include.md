# Include

Includes one source file into another.

## Syntax

`include "filename"`

## Explanation

Removes the corresponding two tokens ("include" and string-literal) from the current source file.
Writes the content of the source file, identified by filename, in place of the removed tokens.

Search the directory where the current file is located, if the file is not found, search the include directories.
In the case the file is not found anyway, the program is invalid.

## Example

```
include "math.hk"

include "mylib.hk" /: ... :/

/: ... :/ include "main.ck"

/: ... :/ include "./GL/freeglut.hk" /: ... :/
```
