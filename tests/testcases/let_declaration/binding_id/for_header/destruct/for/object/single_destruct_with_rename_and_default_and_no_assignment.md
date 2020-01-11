# Tenko parser test case

- Path: tests/testcases/let_declaration/binding_id/for_header/destruct/for/object/single_destruct_with_rename_and_default_and_no_assignment.md

> :: let declaration : binding id : for header : destruct : for : object
>
> ::> single destruct with rename and default and no assignment

## Input

`````js
for (let {x:y=z};;);
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in five parsing modes: sloppy, sloppy+annexb, strict script, module, module+annexb.

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
throws: Parser error!
  Declaration destructuring must have init

start@1:0, error@1:16
╔══╦═════════════════
 1 ║ for (let {x:y=z};;);
   ║                 ^------- error
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