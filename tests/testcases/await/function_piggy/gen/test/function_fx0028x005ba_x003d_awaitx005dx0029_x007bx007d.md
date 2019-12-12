# Tenko parser autogenerated test case

- From: tests/testcases/await/function_piggy/autogen.md
- Path: tests/testcases/await/function_piggy/gen/test/function_fx0028x005ba_x003d_awaitx005dx0029_x007bx007d.md

> :: await : function piggy : gen : test
>
> ::> function fx0028x005ba x003d awaitx005dx0029 x007bx007d

## Input


`````js
function f([a = await]) {}
`````

## Output

_Note: the whole output block is auto-generated. Manual changes will be overwritten!_

Below follow outputs in four parsing modes: sloppy mode, strict mode script goal, module goal, web compat mode (always sloppy).

Note that the output parts are auto-generated by the test runner to reflect actual result.

### Sloppy mode

Parsed with script goal and as if the code did not start with strict mode header.

`````
ast: {
  type: 'Program',
  loc:{start:{line:1,column:0},end:{line:1,column:26},source:''},
  body: [
    {
      type: 'FunctionDeclaration',
      loc:{start:{line:1,column:0},end:{line:1,column:26},source:''},
      generator: false,
      async: false,
      id: {
        type: 'Identifier',
        loc:{start:{line:1,column:9},end:{line:1,column:10},source:''},
        name: 'f'
      },
      params: [
        {
          type: 'ArrayPattern',
          loc:{start:{line:1,column:11},end:{line:1,column:22},source:''},
          elements: [
            {
              type: 'AssignmentPattern',
              loc:{start:{line:1,column:12},end:{line:1,column:21},source:''},
              left: {
                type: 'Identifier',
                loc:{start:{line:1,column:12},end:{line:1,column:13},source:''},
                name: 'a'
              },
              right: {
                type: 'Identifier',
                loc:{start:{line:1,column:16},end:{line:1,column:21},source:''},
                name: 'await'
              }
            }
          ]
        }
      ],
      body: {
        type: 'BlockStatement',
        loc:{start:{line:1,column:24},end:{line:1,column:26},source:''},
        body: []
      }
    }
  ]
}

tokens (12x):
       ID_function IDENT PUNC_PAREN_OPEN PUNC_BRACKET_OPEN IDENT
       PUNC_EQ ID_await PUNC_BRACKET_CLOSE PUNC_PAREN_CLOSE
       PUNC_CURLY_OPEN PUNC_CURLY_CLOSE
`````

### Strict mode

Parsed with script goal but as if it was starting with `"use strict"` at the top.

_Output same as sloppy mode._

### Module goal

Parsed with the module goal.

`````
throws: Parser error!
  Cannot use `await` as var when goal=module but found `await` outside an async function

function f([a = await]) {}
                     ^------- error
`````


### Web compat mode

Parsed in sloppy script mode but with the web compat flag enabled.

_Output same as sloppy mode._

## AST Printer

Printer output different from input [sloppy]:

````js
function f([a = await,]) {}
````

Produces same AST