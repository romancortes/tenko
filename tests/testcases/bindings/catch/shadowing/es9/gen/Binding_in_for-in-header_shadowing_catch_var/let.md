# Tenko parser autogenerated test case

- From: tests/testcases/bindings/catch/shadowing/es9/autogen.md
- Path: tests/testcases/bindings/catch/shadowing/es9/gen/Binding_in_for-in-header_shadowing_catch_var/let.md

> :: bindings : catch : shadowing : es9 : gen : Binding in for-in-header shadowing catch var
>
> ::> let

## Input


`````js
try {} catch (e) { for (let e in y) {} }
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
  loc:{start:{line:1,column:0},end:{line:1,column:40},source:''},
  body: [
    {
      type: 'TryStatement',
      loc:{start:{line:1,column:0},end:{line:1,column:40},source:''},
      block: {
        type: 'BlockStatement',
        loc:{start:{line:1,column:4},end:{line:1,column:6},source:''},
        body: []
      },
      handler: {
        type: 'CatchClause',
        loc:{start:{line:1,column:7},end:{line:1,column:40},source:''},
        param: {
          type: 'Identifier',
          loc:{start:{line:1,column:14},end:{line:1,column:15},source:''},
          name: 'e'
        },
        body: {
          type: 'BlockStatement',
          loc:{start:{line:1,column:17},end:{line:1,column:40},source:''},
          body: [
            {
              type: 'ForInStatement',
              loc:{start:{line:1,column:19},end:{line:1,column:38},source:''},
              left: {
                type: 'VariableDeclaration',
                loc:{start:{line:1,column:24},end:{line:1,column:29},source:''},
                kind: 'let',
                declarations: [
                  {
                    type: 'VariableDeclarator',
                    loc:{start:{line:1,column:28},end:{line:1,column:29},source:''},
                    id: {
                      type: 'Identifier',
                      loc:{start:{line:1,column:28},end:{line:1,column:29},source:''},
                      name: 'e'
                    },
                    init: null
                  }
                ]
              },
              right: {
                type: 'Identifier',
                loc:{start:{line:1,column:33},end:{line:1,column:34},source:''},
                name: 'y'
              },
              body: {
                type: 'BlockStatement',
                loc:{start:{line:1,column:36},end:{line:1,column:38},source:''},
                body: []
              }
            }
          ]
        }
      },
      finalizer: null
    }
  ]
}

tokens (19x):
       ID_try PUNC_CURLY_OPEN PUNC_CURLY_CLOSE ID_catch
       PUNC_PAREN_OPEN IDENT PUNC_PAREN_CLOSE PUNC_CURLY_OPEN ID_for
       PUNC_PAREN_OPEN ID_let IDENT ID_in IDENT PUNC_PAREN_CLOSE
       PUNC_CURLY_OPEN PUNC_CURLY_CLOSE PUNC_CURLY_CLOSE
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

## AST Printer

Printer output different from input [sloppy][annexb:no]:

````js
try {} catch (e) {for (let e in y) {}}
````

Produces same AST