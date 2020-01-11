# Tenko parser test case

- Path: tests/testcases/strict_mode/directive_headers/ident_3d_5byield5d/class_method/as_method_name_w_directive.md

> :: strict mode : directive headers : ident 3d 5byield5d : class method
>
> ::> as method name w directive

## Input

`````js
class c {yield(){ "use strict"; }}
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
  loc:{start:{line:1,column:0},end:{line:1,column:34},source:''},
  body: [
    {
      type: 'ClassDeclaration',
      loc:{start:{line:1,column:0},end:{line:1,column:34},source:''},
      id: {
        type: 'Identifier',
        loc:{start:{line:1,column:6},end:{line:1,column:7},source:''},
        name: 'c'
      },
      superClass: null,
      body: {
        type: 'ClassBody',
        loc:{start:{line:1,column:8},end:{line:1,column:34},source:''},
        body: [
          {
            type: 'MethodDefinition',
            loc:{start:{line:1,column:9},end:{line:1,column:33},source:''},
            key: {
              type: 'Identifier',
              loc:{start:{line:1,column:9},end:{line:1,column:14},source:''},
              name: 'yield'
            },
            static: false,
            computed: false,
            kind: 'method',
            value: {
              type: 'FunctionExpression',
              loc:{start:{line:1,column:9},end:{line:1,column:33},source:''},
              generator: false,
              async: false,
              id: null,
              params: [],
              body: {
                type: 'BlockStatement',
                loc:{start:{line:1,column:16},end:{line:1,column:33},source:''},
                body: [
                  {
                    type: 'ExpressionStatement',
                    loc:{start:{line:1,column:18},end:{line:1,column:31},source:''},
                    expression: {
                      type: 'Literal',
                      loc:{start:{line:1,column:18},end:{line:1,column:30},source:''},
                      value: 'use strict',
                      raw: '"use strict"'
                    },
                    directive: 'use strict'
                  }
                ]
              }
            }
          }
        ]
      }
    }
  ]
}

tokens (12x):
       ID_class IDENT PUNC_CURLY_OPEN ID_yield PUNC_PAREN_OPEN
       PUNC_PAREN_CLOSE PUNC_CURLY_OPEN STRING_DOUBLE PUNC_SEMI
       PUNC_CURLY_CLOSE PUNC_CURLY_CLOSE
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
class c{yield(){"use strict";};}
````

Produces same AST