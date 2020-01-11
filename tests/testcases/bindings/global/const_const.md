# Tenko parser test case

- Path: tests/testcases/bindings/global/const_const.md

> :: bindings : global
>
> ::> const const
> 
> https://tc39.github.io/ecma262/#sec-scripts-static-semantics-early-errors
> 
> https://tc39.github.io/ecma262/#sec-module-semantics-static-semantics-early-errors
> 
> > It is a Syntax Error if the LexicallyDeclaredNames of ScriptBody contains any duplicate entries.
> 
> > It is a Syntax Error if any element of the LexicallyDeclaredNames of ScriptBody also occurs in the VarDeclaredNames of ScriptBody.

## Input

`````js
const x = a; const x = b;
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in five parsing modes: sloppy, sloppy+annexb, strict script, module, module+annexb.

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
throws: Parser error!
  Attempted to create a lexical binding for `x` but another binding already existed on the same level

start@1:0, error@1:19
╔══╦═════════════════
 1 ║ const x = a; const x = b;
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