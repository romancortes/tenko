# Tenko parser test case

- Path: tests/testcases/call_expression/calling_with_a_pattern_2314/func_name_async/when_the_object_must_be_a_pattern_28shorthand2bassignment29.md

> :: call expression : calling with a pattern 2314 : func name async
>
> ::> when the object must be a pattern 28shorthand2bassignment29
>
> The object must be a pattern because of the assignment

## Input

`````js
async({a=1})
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in five parsing modes: sloppy, sloppy+annexb, strict script, module, module+annexb.

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
throws: Parser error!
  Group contained a value that must destruct but this was not an arrow so it is invalid (at EOF)

start@1:0, error@1:5
╔══╦════════════════
 1 ║ async({a=1})
   ║      ^^^^^^^------- error
╚══╩════════════════

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