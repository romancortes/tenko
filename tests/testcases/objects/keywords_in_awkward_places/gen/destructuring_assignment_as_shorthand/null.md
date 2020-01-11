# Tenko parser autogenerated test case

- From: tests/testcases/objects/keywords_in_awkward_places/autogen.md
- Path: tests/testcases/objects/keywords_in_awkward_places/gen/destructuring_assignment_as_shorthand/null.md

> :: objects : keywords in awkward places : gen : destructuring assignment as shorthand
>
> ::> null

## Input


`````js
({null} = x);
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in five parsing modes: sloppy, sloppy+annexb, strict script, module, module+annexb.

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
throws: Parser error!
  Cannot use this name (`null`) as a variable name because: Cannot never use this reserved word as a variable name

start@1:0, error@1:2
╔══╦════════════════
 1 ║ ({null} = x);
   ║   ^^^^------- error
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