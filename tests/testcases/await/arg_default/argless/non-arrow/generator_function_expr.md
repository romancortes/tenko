# Tenko parser test case

- Path: tests/testcases/await/arg_default/argless/non-arrow/generator_function_expr.md

> :: await : arg default : argless : non-arrow
>
> ::> generator function expr

## Input

`````js
let x = function *f(foo = await){}
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
  loc:{start:{line:1,column:0},end:{line:1,column:34},source:''},
  body: [
    {
      type: 'VariableDeclaration',
      loc:{start:{line:1,column:0},end:{line:1,column:34},source:''},
      kind: 'let',
      declarations: [
        {
          type: 'VariableDeclarator',
          loc:{start:{line:1,column:4},end:{line:1,column:34},source:''},
          id: {
            type: 'Identifier',
            loc:{start:{line:1,column:4},end:{line:1,column:5},source:''},
            name: 'x'
          },
          init: {
            type: 'FunctionExpression',
            loc:{start:{line:1,column:8},end:{line:1,column:34},source:''},
            generator: true,
            async: false,
            id: {
              type: 'Identifier',
              loc:{start:{line:1,column:18},end:{line:1,column:19},source:''},
              name: 'f'
            },
            params: [
              {
                type: 'AssignmentPattern',
                loc:{start:{line:1,column:20},end:{line:1,column:31},source:''},
                left: {
                  type: 'Identifier',
                  loc:{start:{line:1,column:20},end:{line:1,column:23},source:''},
                  name: 'foo'
                },
                right: {
                  type: 'Identifier',
                  loc:{start:{line:1,column:26},end:{line:1,column:31},source:''},
                  name: 'await'
                }
              }
            ],
            body: {
              type: 'BlockStatement',
              loc:{start:{line:1,column:32},end:{line:1,column:34},source:''},
              body: []
            }
          }
        }
      ]
    }
  ]
}

tokens (15x):
       ID_let IDENT PUNC_EQ ID_function PUNC_STAR IDENT
       PUNC_PAREN_OPEN IDENT PUNC_EQ ID_await PUNC_PAREN_CLOSE
       PUNC_CURLY_OPEN PUNC_CURLY_CLOSE ASI
`````

### Strict mode

Parsed with script goal but as if it was starting with `"use strict"` at the top.

_Output same as sloppy mode._

### Module goal

Parsed with the module goal.

`````
throws: Parser error!
  Cannot use `await` as var when goal=module but found `await` outside an async function

start@1:0, error@1:31
╔══╦═════════════════
 1 ║ let x = function *f(foo = await){}
   ║                                ^------- error
╚══╩═════════════════

`````

### Sloppy mode with AnnexB

Parsed with script goal with AnnexB rules enabled and as if the code did not start with strict mode header.

_Output same as sloppy mode._

### Module goal with AnnexB

Parsed with the module goal with AnnexB rules enabled.

_Output same as module mode._

## AST Printer

Printer output different from input [sloppy][annexb:no]:

````js
let x = function* f(foo = await) {};
````

Produces same AST