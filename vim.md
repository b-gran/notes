# Vimscript
`<sfile>`: When executing a `":source"` command, is replaced with the file name of the sourced file.

The `.` is used for string concatenation.

Single-quoted strings are automatically escaped.
Backslashes must be escaped in double-quoted strings.

`\w:variable_name` indicates the scope of the variable.

| Prefix | Meaning |
| --- | --- |
| g:varname	| The variable is global |
| s:varname	| The variable is local to the current script file |
| w:varname	| The variable is local to the current editor window |
| t:varname	| The variable is local to the current editor tab |
| b:varname	| The variable is local to the current editor buffer |
| l:varname	| The variable is local to the current function |
| a:varname	| The variable is a parameter of the current function |
| v:varname	| The variable is one that Vim predefines |

> **Source** [https://www.ibm.com/developerworks/library/l-vim-script-1/index.html](https://www.ibm.com/developerworks/library/l-vim-script-1/index.html)

# Ex mode

`exe[cute]`: Evaluate an expression and execute the resulting string as an **Ex** command.

`source`: read a file and execute the lines as **Ex** commands.

Abbreviated versions of commands can be used when they don't conflict with abbreviations of other commands.
```vim
:buffer 2
:buff 2
:buf 2
```
