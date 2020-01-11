# Tenko parser autogenerated test case

- From: tests/testcases/assigns/to_keyword/autogen.md
- Path: tests/testcases/assigns/to_keyword/gen/should_listen_to_use_strict_directive_in_function_wrapped/yield.md

> :: assigns : to keyword : gen : should listen to use strict directive in function wrapped
>
> ::> yield

## Input


`````js
function f() {
  "use strict";
  (yield = x);
}
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in five parsing modes: sloppy, sloppy+annexb, strict script, module, module+annexb.

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
throws: Parser error!
  Cannot use `yield` outside of generator functions when in strict mode

start@1:0, error@3:3
╔══╦════════════════
 1 ║ function f() {
 2 ║   "use strict";
 3 ║   (yield = x);
   ║    ^^^^^------- error
 4 ║ }
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