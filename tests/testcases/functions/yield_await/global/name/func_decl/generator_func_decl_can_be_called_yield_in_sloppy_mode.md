# Tenko parser test case

- Path: tests/testcases/functions/yield_await/global/name/func_decl/generator_func_decl_can_be_called_yield_in_sloppy_mode.md

> :: functions : yield await : global : name : func decl
>
> ::> generator func decl can be called yield in sloppy mode
>
> barring exceptions -- for all functions and methods goes:
>
> - name of the func keeps outer scope await/yield state. exception: function expressions clear it.
> - args and body explicitly set it according to the type of this function (so async sets await clears yield, etc)
>
> This means you can use `await` as a function name as long as you are not in strict mode and not already inside an async function and it's okay if the function whose name is being defined is actually async itself.
>
> the cases to test are a cross product of:
>
> - `<global, inside async, inside generator>` 
> - `x` 
> - `<yield, await>`
> - `x` 
> - `<regular, async, generator, async gen>`
> - `x` 
> - `<name, arg-name, arg-default, body>`
> - `x`
> - `<class method, obj method, decl, expr, default>`

## Input

`````js
function *yield() {}
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in five parsing modes: sloppy, sloppy+annexb, strict script, module, module+annexb.

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
ast: {
  type: 'Program',
  loc:{start:{line:1,column:0},end:{line:1,column:20},source:''},
  body: [
    {
      type: 'FunctionDeclaration',
      loc:{start:{line:1,column:0},end:{line:1,column:20},source:''},
      generator: true,
      async: false,
      id: {
        type: 'Identifier',
        loc:{start:{line:1,column:10},end:{line:1,column:15},source:''},
        name: 'yield'
      },
      params: [],
      body: {
        type: 'BlockStatement',
        loc:{start:{line:1,column:18},end:{line:1,column:20},source:''},
        body: []
      }
    }
  ]
}

tokens (8x):
       ID_function PUNC_STAR ID_yield PUNC_PAREN_OPEN PUNC_PAREN_CLOSE
       PUNC_CURLY_OPEN PUNC_CURLY_CLOSE
`````

### Strict mode

Parsed with script goal but as if it was starting with `"use strict"` at the top.

`````
throws: Parser error!
  Cannot use this name (`yield`) as a variable name because: Cannot use this reserved word as a variable name in strict mode

start@1:0, error@1:10
╔══╦═════════════════
 1 ║ function *yield() {}
   ║           ^^^^^------- error
╚══╩═════════════════

`````

### Module goal

Parsed with the module goal.

_Output same as strict mode._

### Sloppy mode with AnnexB

Parsed with script goal with AnnexB rules enabled and as if the code did not start with strict mode header.

_Output same as sloppy mode._

### Module goal with AnnexB

Parsed with the module goal with AnnexB rules enabled.

_Output same as strict mode._

## AST Printer

Printer output different from input [sloppy][annexb:no]:

````js
function* yield() {}
````

Produces same AST