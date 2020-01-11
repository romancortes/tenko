# Tenko parser test case

- Path: tests/testcases/var/binding_generic/in_a_for-header/destruct/invalid_colorless_for-statement/object/single_var_with_trailing_comma.md

> :: var : binding generic : in a for-header : destruct : invalid colorless for-statement : object
>
> ::> single var with trailing comma

## Input

`````js
for (var {x,} = obj);
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in five parsing modes: sloppy, sloppy+annexb, strict script, module, module+annexb.

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
throws: Parser error!
  Missing first semi in `for` header, found `)` instead

start@1:0, error@1:19
╔══╦═════════════════
 1 ║ for (var {x,} = obj);
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