# Tenko parser test case

- Path: tests/testcases/objects/destructuring/string/destruct_to_60await_a60_with_destruct.md

> :: objects : destructuring : string
>
> ::> destruct to 60await a60 with destruct

## Input


`````js
s = {"foo": await a = x} = x
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in five parsing modes: sloppy, sloppy+annexb, strict script, module, module+annexb.

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
throws: Parser error!
  Expected the closing curly `}` for an object, found `a` instead

start@1:0, error@1:18
╔══╦═════════════════
 1 ║ s = {"foo": await a = x} = x
   ║                   ^------- error
╚══╩═════════════════

`````

### Strict mode

Parsed with script goal but as if it was starting with `"use strict"` at the top.

_Output same as sloppy mode._

### Module goal

Parsed with the module goal.

`````
throws: Parser error!
  Cannot use `await` as var when goal=module but found `await` outside an async function

start@1:0, error@1:18
╔══╦═════════════════
 1 ║ s = {"foo": await a = x} = x
   ║                   ^------- error
╚══╩═════════════════

`````

### Sloppy mode with AnnexB

Parsed with script goal with AnnexB rules enabled and as if the code did not start with strict mode header.

_Output same as sloppy mode._

### Module goal with AnnexB

Parsed with the module goal with AnnexB rules enabled.

_Output same as module mode._