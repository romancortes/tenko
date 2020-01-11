# Tenko parser test case

- Path: tests/testcases/objects/destructuring/identifier_properties/a3ab_identifier_check/strict-mode_only_assign_keyword3dyield.md

> :: objects : destructuring : identifier properties : a3ab identifier check
>
> ::> strict-mode only assign keyword3dyield

## Input

`````js
({xxxx:yield} = null)
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
        type: 'AssignmentExpression',
        loc:{start:{line:1,column:1},end:{line:1,column:20},source:''},
        left: {
          type: 'ObjectPattern',
          loc:{start:{line:1,column:1},end:{line:1,column:13},source:''},
          properties: [
            {
              type: 'Property',
              loc:{start:{line:1,column:2},end:{line:1,column:12},source:''},
              key: {
                type: 'Identifier',
                loc:{start:{line:1,column:2},end:{line:1,column:6},source:''},
                name: 'xxxx'
              },
              kind: 'init',
              method: false,
              computed: false,
              value: {
                type: 'Identifier',
                loc:{start:{line:1,column:7},end:{line:1,column:12},source:''},
                name: 'yield'
              },
              shorthand: false
            }
          ]
        },
        operator: '=',
        right: {
          type: 'Literal',
          loc:{start:{line:1,column:16},end:{line:1,column:20},source:''},
          value: null,
          raw: 'null'
        }
      }
    }
  ]
}

tokens (11x):
       PUNC_PAREN_OPEN PUNC_CURLY_OPEN IDENT PUNC_COLON ID_yield
       PUNC_CURLY_CLOSE PUNC_EQ ID_null PUNC_PAREN_CLOSE ASI
`````

### Strict mode

Parsed with script goal but as if it was starting with `"use strict"` at the top.

`````
throws: Parser error!
  Cannot use `yield` outside of generator functions when in strict mode

start@1:0, error@1:7
╔══╦════════════════
 1 ║ ({xxxx:yield} = null)
   ║        ^^^^^------- error
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
({xxxx:yield} = null);
````

Produces same AST