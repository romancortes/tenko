# Tenko parser test case

- Path: tests/testcases/let_declaration/binding_id/for_header/destruct/for-of/object/double_destruct_with_rename_and_init.md

> :: let declaration : binding id : for header : destruct : for-of : object
>
> ::> double destruct with rename and init

## Input

`````js
for (let {x : y, z, a : b = c} of obj);
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
  loc:{start:{line:1,column:0},end:{line:1,column:39},source:''},
  body: [
    {
      type: 'ForOfStatement',
      loc:{start:{line:1,column:0},end:{line:1,column:39},source:''},
      left: {
        type: 'VariableDeclaration',
        loc:{start:{line:1,column:5},end:{line:1,column:30},source:''},
        kind: 'let',
        declarations: [
          {
            type: 'VariableDeclarator',
            loc:{start:{line:1,column:9},end:{line:1,column:30},source:''},
            id: {
              type: 'ObjectPattern',
              loc:{start:{line:1,column:9},end:{line:1,column:30},source:''},
              properties: [
                {
                  type: 'Property',
                  loc:{start:{line:1,column:10},end:{line:1,column:15},source:''},
                  key: {
                    type: 'Identifier',
                    loc:{start:{line:1,column:10},end:{line:1,column:11},source:''},
                    name: 'x'
                  },
                  kind: 'init',
                  method: false,
                  computed: false,
                  value: {
                    type: 'Identifier',
                    loc:{start:{line:1,column:14},end:{line:1,column:15},source:''},
                    name: 'y'
                  },
                  shorthand: false
                },
                {
                  type: 'Property',
                  loc:{start:{line:1,column:17},end:{line:1,column:18},source:''},
                  key: {
                    type: 'Identifier',
                    loc:{start:{line:1,column:17},end:{line:1,column:18},source:''},
                    name: 'z'
                  },
                  kind: 'init',
                  method: false,
                  computed: false,
                  value: {
                    type: 'Identifier',
                    loc:{start:{line:1,column:17},end:{line:1,column:18},source:''},
                    name: 'z'
                  },
                  shorthand: true
                },
                {
                  type: 'Property',
                  loc:{start:{line:1,column:20},end:{line:1,column:29},source:''},
                  key: {
                    type: 'Identifier',
                    loc:{start:{line:1,column:20},end:{line:1,column:21},source:''},
                    name: 'a'
                  },
                  kind: 'init',
                  method: false,
                  computed: false,
                  value: {
                    type: 'AssignmentPattern',
                    loc:{start:{line:1,column:24},end:{line:1,column:29},source:''},
                    left: {
                      type: 'Identifier',
                      loc:{start:{line:1,column:24},end:{line:1,column:25},source:''},
                      name: 'b'
                    },
                    right: {
                      type: 'Identifier',
                      loc:{start:{line:1,column:28},end:{line:1,column:29},source:''},
                      name: 'c'
                    }
                  },
                  shorthand: false
                }
              ]
            },
            init: null
          }
        ]
      },
      right: {
        type: 'Identifier',
        loc:{start:{line:1,column:34},end:{line:1,column:37},source:''},
        name: 'obj'
      },
      await: false,
      body: {
        type: 'EmptyStatement',
        loc:{start:{line:1,column:38},end:{line:1,column:39},source:''}
      }
    }
  ]
}

tokens (21x):
       ID_for PUNC_PAREN_OPEN ID_let PUNC_CURLY_OPEN IDENT PUNC_COLON
       IDENT PUNC_COMMA IDENT PUNC_COMMA IDENT PUNC_COLON IDENT
       PUNC_EQ IDENT PUNC_CURLY_CLOSE ID_of IDENT PUNC_PAREN_CLOSE
       PUNC_SEMI
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
for (let {x:y, z, a:b = c} of obj) ;
````

Produces same AST