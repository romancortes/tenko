# Tenko parser autogenerated test case

- From: tests/testcases/var/binding_generic/reserved_words/autogen.md
- Path: tests/testcases/var/binding_generic/reserved_words/gen/function_object_alias_destructured_arg/protected.md

> :: var : binding generic : reserved words : gen : function object alias destructured arg
>
> ::> protected

## Input


`````js
function fh({x: protected}) {}
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
  loc:{start:{line:1,column:0},end:{line:1,column:30},source:''},
  body: [
    {
      type: 'FunctionDeclaration',
      loc:{start:{line:1,column:0},end:{line:1,column:30},source:''},
      generator: false,
      async: false,
      id: {
        type: 'Identifier',
        loc:{start:{line:1,column:9},end:{line:1,column:11},source:''},
        name: 'fh'
      },
      params: [
        {
          type: 'ObjectPattern',
          loc:{start:{line:1,column:12},end:{line:1,column:26},source:''},
          properties: [
            {
              type: 'Property',
              loc:{start:{line:1,column:13},end:{line:1,column:25},source:''},
              key: {
                type: 'Identifier',
                loc:{start:{line:1,column:13},end:{line:1,column:14},source:''},
                name: 'x'
              },
              kind: 'init',
              method: false,
              computed: false,
              value: {
                type: 'Identifier',
                loc:{start:{line:1,column:16},end:{line:1,column:25},source:''},
                name: 'protected'
              },
              shorthand: false
            }
          ]
        }
      ],
      body: {
        type: 'BlockStatement',
        loc:{start:{line:1,column:28},end:{line:1,column:30},source:''},
        body: []
      }
    }
  ]
}

tokens (12x):
       ID_function IDENT PUNC_PAREN_OPEN PUNC_CURLY_OPEN IDENT
       PUNC_COLON ID_protected PUNC_CURLY_CLOSE PUNC_PAREN_CLOSE
       PUNC_CURLY_OPEN PUNC_CURLY_CLOSE
`````

### Strict mode

Parsed with script goal but as if it was starting with `"use strict"` at the top.

`````
throws: Parser error!
  Cannot use this name (`protected`) as a variable name because: Cannot use this reserved word as a variable name in strict mode

start@1:0, error@1:16
╔══╦═════════════════
 1 ║ function fh({x: protected}) {}
   ║                 ^^^^^^^^^------- error
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
function fh({x:protected}) {}
````

Produces same AST