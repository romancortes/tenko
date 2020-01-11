# Tenko parser test case

- Path: tests/testcases/bindings/arrow_args/dupe_between_args_and_local_bindings/complex_arg_as_lex.md

> :: bindings : arrow args : dupe between args and local bindings
>
> ::> complex arg as lex
> 
> https://tc39.github.io/ecma262/#sec-arrow-function-definitions-static-semantics-early-errors
>
> > It is a Syntax Error if any element of the BoundNames of ArrowParameters also occurs in the LexicallyDeclaredNames of ConciseBody.


## Input


`````js
([a,b,c]) => { const c = x; }
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in five parsing modes: sloppy, sloppy+annexb, strict script, module, module+annexb.

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
throws: Parser error!
  Cannot create lexical binding for `c` because it shadows a function parameter

start@1:0, error@1:21
╔══╦═════════════════
 1 ║ ([a,b,c]) => { const c = x; }
   ║                      ^------- error
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