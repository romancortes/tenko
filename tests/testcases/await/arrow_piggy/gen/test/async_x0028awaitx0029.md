# Tenko parser autogenerated test case

- From: tests/testcases/await/arrow_piggy/autogen.md
- Path: tests/testcases/await/arrow_piggy/gen/test/async_x0028awaitx0029.md

> :: await : arrow piggy : gen : test
>
> ::> async x0028awaitx0029

## Input


`````js
async (await)
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
  loc:{start:{line:1,column:0},end:{line:1,column:13},source:''},
  body: [
    {
      type: 'ExpressionStatement',
      loc:{start:{line:1,column:0},end:{line:1,column:13},source:''},
      expression: {
        type: 'CallExpression',
        loc:{start:{line:1,column:0},end:{line:1,column:13},source:''},
        callee: {
          type: 'Identifier',
          loc:{start:{line:1,column:0},end:{line:1,column:5},source:''},
          name: 'async'
        },
        arguments: [
          {
            type: 'Identifier',
            loc:{start:{line:1,column:7},end:{line:1,column:12},source:''},
            name: 'await'
          }
        ]
      }
    }
  ]
}

tokens (6x):
       ID_async PUNC_PAREN_OPEN ID_await PUNC_PAREN_CLOSE ASI
`````

### Strict mode

Parsed with script goal but as if it was starting with `"use strict"` at the top.

_Output same as sloppy mode._

### Module goal

Parsed with the module goal.

`````
throws: Parser error!
  Cannot use `await` as var when goal=module but found `await` outside an async function

async (await)
            ^------- error
`````


### Web compat mode

Parsed in sloppy script mode but with the web compat flag enabled.

_Output same as sloppy mode._

## AST Printer

Printer output different from input [sloppy]:

````js
(async(await));
````

Produces same AST