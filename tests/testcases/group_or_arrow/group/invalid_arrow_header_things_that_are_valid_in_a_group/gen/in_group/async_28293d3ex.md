# Tenko parser autogenerated test case

- From: tests/testcases/group_or_arrow/group/invalid_arrow_header_things_that_are_valid_in_a_group/autogen.md
- Path: tests/testcases/group_or_arrow/group/invalid_arrow_header_things_that_are_valid_in_a_group/gen/in_group/async_28293d3ex.md

> :: group or arrow : group : invalid arrow header things that are valid in a group : gen : in group
>
> ::> async 28293d3ex

## Input


`````js
( async ()=>x )
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
  loc:{start:{line:1,column:0},end:{line:1,column:15},source:''},
  body: [
    {
      type: 'ExpressionStatement',
      loc:{start:{line:1,column:0},end:{line:1,column:15},source:''},
      expression: {
        type: 'ArrowFunctionExpression',
        loc:{start:{line:1,column:2},end:{line:1,column:13},source:''},
        params: [],
        id: null,
        generator: false,
        async: true,
        expression: true,
        body: {
          type: 'Identifier',
          loc:{start:{line:1,column:12},end:{line:1,column:13},source:''},
          name: 'x'
        }
      }
    }
  ]
}

tokens (9x):
       PUNC_PAREN_OPEN ID_async PUNC_PAREN_OPEN PUNC_PAREN_CLOSE
       PUNC_EQ_GT IDENT PUNC_PAREN_CLOSE ASI
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
async () => (x);
````

Produces same AST