# Tenko parser test case

- Path: tests/testcases/strict_mode/directive_headers/ident_3d_5beval5d/class_method/assigned_to_in_param_default_w2fo_directive.md

> :: strict mode : directive headers : ident 3d 5beval5d : class method
>
> ::> assigned to in param default w2fo directive
>
> the default causes the error, not the usage, but whatever

## Input


`````js
class c {foo(x=eval=y){ }}
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in five parsing modes: sloppy, sloppy+annexb, strict script, module, module+annexb.

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
throws: Parser error!
  Cannot assign to `eval` and `arguments` in strict mode

start@1:0, error@1:19
╔══╦═════════════════
 1 ║ class c {foo(x=eval=y){ }}
   ║                    ^------- error
╚══╩═════════════════

`````

### Strict mode

Parsed with script goal but as if it was starting with `"use strict"` at the top.

_Output same as sloppy mode._

### Module goal

Parsed with the module goal.

_Output same as sloppy mode._

### Sloppy mode with AnnexB

Parsed with script goal with AnnexB rules enabled and as if the code did not start with strict mode header.

_Output same as sloppy mode._

### Module goal with AnnexB

Parsed with the module goal with AnnexB rules enabled.

_Output same as sloppy mode._