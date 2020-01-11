# Tenko parser autogenerated test case

- From: tests/testcases/yield/arrow_piggy/autogen.md
- Path: tests/testcases/yield/arrow_piggy/gen/test/287ba3a_b_3d_yield7d29_3d3e_x.md

> :: yield : arrow piggy : gen : test
>
> ::> 287ba3a b 3d yield7d29 3d3e x

## Input


`````js
({a: b = yield}) => x
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
  loc:{start:{line:1,column:0},end:{line:1,column:21},source:''},
  body: [
    {
      type: 'ExpressionStatement',
      loc:{start:{line:1,column:0},end:{line:1,column:21},source:''},
      expression: {
        type: 'ArrowFunctionExpression',
        loc:{start:{line:1,column:0},end:{line:1,column:21},source:''},
        params: [
          {
            type: 'ObjectPattern',
            loc:{start:{line:1,column:1},end:{line:1,column:15},source:''},
            properties: [
              {
                type: 'Property',
                loc:{start:{line:1,column:2},end:{line:1,column:14},source:''},
                key: {
                  type: 'Identifier',
                  loc:{start:{line:1,column:2},end:{line:1,column:3},source:''},
                  name: 'a'
                },
                kind: 'init',
                method: false,
                computed: false,
                value: {
                  type: 'AssignmentPattern',
                  loc:{start:{line:1,column:5},end:{line:1,column:14},source:''},
                  left: {
                    type: 'Identifier',
                    loc:{start:{line:1,column:5},end:{line:1,column:6},source:''},
                    name: 'b'
                  },
                  right: {
                    type: 'Identifier',
                    loc:{start:{line:1,column:9},end:{line:1,column:14},source:''},
                    name: 'yield'
                  }
                },
                shorthand: false
              }
            ]
          }
        ],
        id: null,
        generator: false,
        async: false,
        expression: true,
        body: {
          type: 'Identifier',
          loc:{start:{line:1,column:20},end:{line:1,column:21},source:''},
          name: 'x'
        }
      }
    }
  ]
}

tokens (13x):
       PUNC_PAREN_OPEN PUNC_CURLY_OPEN IDENT PUNC_COLON IDENT PUNC_EQ
       ID_yield PUNC_CURLY_CLOSE PUNC_PAREN_CLOSE PUNC_EQ_GT IDENT ASI
`````

### Strict mode

Parsed with script goal but as if it was starting with `"use strict"` at the top.

`````
throws: Parser error!
  Cannot use `yield` outside of generator functions when in strict mode

start@1:0, error@1:9
╔══╦════════════════
 1 ║ ({a: b = yield}) => x
   ║          ^^^^^------- error
╚══╩════════════════

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
({a:b = yield}) => (x);
````

Produces same AST