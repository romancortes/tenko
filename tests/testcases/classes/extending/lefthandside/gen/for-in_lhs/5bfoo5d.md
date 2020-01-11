# Tenko parser autogenerated test case

- From: tests/testcases/classes/extending/lefthandside/autogen.md
- Path: tests/testcases/classes/extending/lefthandside/gen/for-in_lhs/5bfoo5d.md

> :: classes : extending : lefthandside : gen : for-in lhs
>
> ::> 5bfoo5d

## Input


`````js
for ([foo] in x) ;
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
  loc:{start:{line:1,column:0},end:{line:1,column:18},source:''},
  body: [
    {
      type: 'ForInStatement',
      loc:{start:{line:1,column:0},end:{line:1,column:18},source:''},
      left: {
        type: 'ArrayPattern',
        loc:{start:{line:1,column:5},end:{line:1,column:10},source:''},
        elements: [
          {
            type: 'Identifier',
            loc:{start:{line:1,column:6},end:{line:1,column:9},source:''},
            name: 'foo'
          }
        ]
      },
      right: {
        type: 'Identifier',
        loc:{start:{line:1,column:14},end:{line:1,column:15},source:''},
        name: 'x'
      },
      body: {
        type: 'EmptyStatement',
        loc:{start:{line:1,column:17},end:{line:1,column:18},source:''}
      }
    }
  ]
}

tokens (10x):
       ID_for PUNC_PAREN_OPEN PUNC_BRACKET_OPEN IDENT
       PUNC_BRACKET_CLOSE ID_in IDENT PUNC_PAREN_CLOSE PUNC_SEMI
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

Printer output was same as input [sloppy][annexb:no]