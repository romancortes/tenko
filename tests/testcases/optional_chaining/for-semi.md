# Tenko parser test case

- Path: tests/testcases/optional_chaining/for-semi.md

> :: optional chaining
>
> ::> for-semi
>
> ## SKIP

## PASS

## Input

`````js
for (a?.b;;);
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
  loc:{start:{line:1,column:0},end:{line:1,column:13},source:''},
  body: [
    {
      type: 'ForStatement',
      loc:{start:{line:1,column:0},end:{line:1,column:13},source:''},
      init: {
        type: 'OptionalMemberExpression',
        loc:{start:{line:1,column:5},end:{line:1,column:9},source:''},
        optional: true,
        computed: false,
        object: {
          type: 'Identifier',
          loc:{start:{line:1,column:5},end:{line:1,column:6},source:''},
          name: 'a'
        },
        property: {
          type: 'Identifier',
          loc:{start:{line:1,column:8},end:{line:1,column:9},source:''},
          name: 'b'
        }
      },
      test: null,
      update: null,
      body: {
        type: 'EmptyStatement',
        loc:{start:{line:1,column:12},end:{line:1,column:13},source:''}
      }
    }
  ]
}

tokens (10x):
       ID_for PUNC_PAREN_OPEN IDENT QMARK_DOT IDENT PUNC_SEMI
       PUNC_SEMI PUNC_PAREN_CLOSE PUNC_SEMI
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
for ((a?.b);;) ;
````

Produces same AST