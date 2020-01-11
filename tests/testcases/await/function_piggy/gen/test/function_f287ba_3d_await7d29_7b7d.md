# Tenko parser autogenerated test case

- From: tests/testcases/await/function_piggy/autogen.md
- Path: tests/testcases/await/function_piggy/gen/test/function_f287ba_3d_await7d29_7b7d.md

> :: await : function piggy : gen : test
>
> ::> function f287ba 3d await7d29 7b7d

## Input


`````js
function f({a = await}) {}
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
          type: 'ObjectPattern',
          loc:{start:{line:1,column:11},end:{line:1,column:22},source:''},
          properties: [
            {
              type: 'Property',
              loc:{start:{line:1,column:12},end:{line:1,column:21},source:''},
              key: {
                type: 'Identifier',
                loc:{start:{line:1,column:12},end:{line:1,column:13},source:''},
                name: 'a'
              },
              kind: 'init',
              method: false,
              computed: false,
              value: {
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
              },
              shorthand: true
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
       ID_function IDENT PUNC_PAREN_OPEN PUNC_CURLY_OPEN IDENT PUNC_EQ
       ID_await PUNC_CURLY_CLOSE PUNC_PAREN_CLOSE PUNC_CURLY_OPEN
       PUNC_CURLY_CLOSE
`````

### Strict mode

Parsed with script goal but as if it was starting with `"use strict"` at the top.

_Output same as sloppy mode._

### Module goal

Parsed with the module goal.

`````
throws: Parser error!
  Cannot use `await` as var when goal=module but found `await` outside an async function

start@1:0, error@1:21
╔══╦═════════════════
 1 ║ function f({a = await}) {}
   ║                      ^------- error
╚══╩═════════════════

`````

### Sloppy mode with AnnexB

Parsed with script goal with AnnexB rules enabled and as if the code did not start with strict mode header.

_Output same as sloppy mode._

### Module goal with AnnexB

Parsed with the module goal with AnnexB rules enabled.

_Output same as module mode._

## AST Printer

Printer output was same as input [sloppy][annexb:no]