# Tenko parser test case

- Path: tests/testcases/optional_chaining/good_number2.md

> :: optional chaining
>
> ::> good number2
>
> Should not disallow cases that were legal before  

## PASS

## Input

`````js
a?.0:b

a?.1:b

a?.2:b

a?.3:b

a?.4:b

a?.5:b

a?.6:b

a?.7:b

a?.8:b

a?.9:b
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
  loc:{start:{line:1,column:0},end:{line:19,column:6},source:''},
  body: [
    {
      type: 'ExpressionStatement',
      loc:{start:{line:1,column:0},end:{line:1,column:6},source:''},
      expression: {
        type: 'ConditionalExpression',
        loc:{start:{line:1,column:0},end:{line:1,column:6},source:''},
        test: {
          type: 'Identifier',
          loc:{start:{line:1,column:0},end:{line:1,column:1},source:''},
          name: 'a'
        },
        consequent: {
          type: 'Literal',
          loc:{start:{line:1,column:2},end:{line:1,column:4},source:''},
          value: 0,
          raw: '.0'
        },
        alternate: {
          type: 'Identifier',
          loc:{start:{line:1,column:5},end:{line:1,column:6},source:''},
          name: 'b'
        }
      }
    },
    {
      type: 'ExpressionStatement',
      loc:{start:{line:3,column:0},end:{line:3,column:6},source:''},
      expression: {
        type: 'ConditionalExpression',
        loc:{start:{line:3,column:0},end:{line:3,column:6},source:''},
        test: {
          type: 'Identifier',
          loc:{start:{line:3,column:0},end:{line:3,column:1},source:''},
          name: 'a'
        },
        consequent: {
          type: 'Literal',
          loc:{start:{line:3,column:2},end:{line:3,column:4},source:''},
          value: 0.1,
          raw: '.1'
        },
        alternate: {
          type: 'Identifier',
          loc:{start:{line:3,column:5},end:{line:3,column:6},source:''},
          name: 'b'
        }
      }
    },
    {
      type: 'ExpressionStatement',
      loc:{start:{line:5,column:0},end:{line:5,column:6},source:''},
      expression: {
        type: 'ConditionalExpression',
        loc:{start:{line:5,column:0},end:{line:5,column:6},source:''},
        test: {
          type: 'Identifier',
          loc:{start:{line:5,column:0},end:{line:5,column:1},source:''},
          name: 'a'
        },
        consequent: {
          type: 'Literal',
          loc:{start:{line:5,column:2},end:{line:5,column:4},source:''},
          value: 0.2,
          raw: '.2'
        },
        alternate: {
          type: 'Identifier',
          loc:{start:{line:5,column:5},end:{line:5,column:6},source:''},
          name: 'b'
        }
      }
    },
    {
      type: 'ExpressionStatement',
      loc:{start:{line:7,column:0},end:{line:7,column:6},source:''},
      expression: {
        type: 'ConditionalExpression',
        loc:{start:{line:7,column:0},end:{line:7,column:6},source:''},
        test: {
          type: 'Identifier',
          loc:{start:{line:7,column:0},end:{line:7,column:1},source:''},
          name: 'a'
        },
        consequent: {
          type: 'Literal',
          loc:{start:{line:7,column:2},end:{line:7,column:4},source:''},
          value: 0.3,
          raw: '.3'
        },
        alternate: {
          type: 'Identifier',
          loc:{start:{line:7,column:5},end:{line:7,column:6},source:''},
          name: 'b'
        }
      }
    },
    {
      type: 'ExpressionStatement',
      loc:{start:{line:9,column:0},end:{line:9,column:6},source:''},
      expression: {
        type: 'ConditionalExpression',
        loc:{start:{line:9,column:0},end:{line:9,column:6},source:''},
        test: {
          type: 'Identifier',
          loc:{start:{line:9,column:0},end:{line:9,column:1},source:''},
          name: 'a'
        },
        consequent: {
          type: 'Literal',
          loc:{start:{line:9,column:2},end:{line:9,column:4},source:''},
          value: 0.4,
          raw: '.4'
        },
        alternate: {
          type: 'Identifier',
          loc:{start:{line:9,column:5},end:{line:9,column:6},source:''},
          name: 'b'
        }
      }
    },
    {
      type: 'ExpressionStatement',
      loc:{start:{line:11,column:0},end:{line:11,column:6},source:''},
      expression: {
        type: 'ConditionalExpression',
        loc:{start:{line:11,column:0},end:{line:11,column:6},source:''},
        test: {
          type: 'Identifier',
          loc:{start:{line:11,column:0},end:{line:11,column:1},source:''},
          name: 'a'
        },
        consequent: {
          type: 'Literal',
          loc:{start:{line:11,column:2},end:{line:11,column:4},source:''},
          value: 0.5,
          raw: '.5'
        },
        alternate: {
          type: 'Identifier',
          loc:{start:{line:11,column:5},end:{line:11,column:6},source:''},
          name: 'b'
        }
      }
    },
    {
      type: 'ExpressionStatement',
      loc:{start:{line:13,column:0},end:{line:13,column:6},source:''},
      expression: {
        type: 'ConditionalExpression',
        loc:{start:{line:13,column:0},end:{line:13,column:6},source:''},
        test: {
          type: 'Identifier',
          loc:{start:{line:13,column:0},end:{line:13,column:1},source:''},
          name: 'a'
        },
        consequent: {
          type: 'Literal',
          loc:{start:{line:13,column:2},end:{line:13,column:4},source:''},
          value: 0.6,
          raw: '.6'
        },
        alternate: {
          type: 'Identifier',
          loc:{start:{line:13,column:5},end:{line:13,column:6},source:''},
          name: 'b'
        }
      }
    },
    {
      type: 'ExpressionStatement',
      loc:{start:{line:15,column:0},end:{line:15,column:6},source:''},
      expression: {
        type: 'ConditionalExpression',
        loc:{start:{line:15,column:0},end:{line:15,column:6},source:''},
        test: {
          type: 'Identifier',
          loc:{start:{line:15,column:0},end:{line:15,column:1},source:''},
          name: 'a'
        },
        consequent: {
          type: 'Literal',
          loc:{start:{line:15,column:2},end:{line:15,column:4},source:''},
          value: 0.7,
          raw: '.7'
        },
        alternate: {
          type: 'Identifier',
          loc:{start:{line:15,column:5},end:{line:15,column:6},source:''},
          name: 'b'
        }
      }
    },
    {
      type: 'ExpressionStatement',
      loc:{start:{line:17,column:0},end:{line:17,column:6},source:''},
      expression: {
        type: 'ConditionalExpression',
        loc:{start:{line:17,column:0},end:{line:17,column:6},source:''},
        test: {
          type: 'Identifier',
          loc:{start:{line:17,column:0},end:{line:17,column:1},source:''},
          name: 'a'
        },
        consequent: {
          type: 'Literal',
          loc:{start:{line:17,column:2},end:{line:17,column:4},source:''},
          value: 0.8,
          raw: '.8'
        },
        alternate: {
          type: 'Identifier',
          loc:{start:{line:17,column:5},end:{line:17,column:6},source:''},
          name: 'b'
        }
      }
    },
    {
      type: 'ExpressionStatement',
      loc:{start:{line:19,column:0},end:{line:19,column:6},source:''},
      expression: {
        type: 'ConditionalExpression',
        loc:{start:{line:19,column:0},end:{line:19,column:6},source:''},
        test: {
          type: 'Identifier',
          loc:{start:{line:19,column:0},end:{line:19,column:1},source:''},
          name: 'a'
        },
        consequent: {
          type: 'Literal',
          loc:{start:{line:19,column:2},end:{line:19,column:4},source:''},
          value: 0.9,
          raw: '.9'
        },
        alternate: {
          type: 'Identifier',
          loc:{start:{line:19,column:5},end:{line:19,column:6},source:''},
          name: 'b'
        }
      }
    }
  ]
}

tokens (61x):
       IDENT PUNC_QMARK NUMBER_DEC PUNC_COLON IDENT ASI IDENT
       PUNC_QMARK NUMBER_DEC PUNC_COLON IDENT ASI IDENT PUNC_QMARK
       NUMBER_DEC PUNC_COLON IDENT ASI IDENT PUNC_QMARK NUMBER_DEC
       PUNC_COLON IDENT ASI IDENT PUNC_QMARK NUMBER_DEC PUNC_COLON
       IDENT ASI IDENT PUNC_QMARK NUMBER_DEC PUNC_COLON IDENT ASI
       IDENT PUNC_QMARK NUMBER_DEC PUNC_COLON IDENT ASI IDENT
       PUNC_QMARK NUMBER_DEC PUNC_COLON IDENT ASI IDENT PUNC_QMARK
       NUMBER_DEC PUNC_COLON IDENT ASI IDENT PUNC_QMARK NUMBER_DEC
       PUNC_COLON IDENT ASI
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
(a? .0 : b);
(a? .1 : b);
(a? .2 : b);
(a? .3 : b);
(a? .4 : b);
(a? .5 : b);
(a? .6 : b);
(a? .7 : b);
(a? .8 : b);
(a? .9 : b);
````

Produces same AST