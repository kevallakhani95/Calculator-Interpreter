# Calculator-Interpreter

This is my first code towards developing an Interpreter. Since, it is my first take on developing an Interpreter from scratch,
I figured I would develop one for a calculator using Python. 
Consider calculator input (for eg. 5+3, 5-8*9, 5*(2-1) and more) as a language.

To produce an output to this language you need to follow various procedures - 
1. Lexical analysis of the input to break the sentance apart into tokens, one token at a time.
2. Parse the lexer object and build a tree structure of the input data.
3. Interpret the parsed object and visit the tree in a post-order form to produce the result.
4. Print the result to the output console.

This is a recursive-descent parser / interpreter and the grammer for the same is given below - 
1. expr : term((PLUS | MINUS) term)*
2. term : factor((MUL | DIV) factor)*
3. factor : (PLUS | MINUS) factor | INTEGER | LPAREN expr RPAREN

It is known as a recursive descent parser since, it is a kind of top-down parser built from a set of mutually 
recursive procedures (or a non-recursive equivalent) where each such procedure usually implements one of the productions of the grammar.

To run the file - 
Simply go to cmd prompt(windows) / Terminal(Linux shell) and switch to the python directory where the file exists, run the calculator_interpreter.py file. 

```
$ python calculator_interpreter.py
```

Keep giving inputs / expressions as long as you want.

Enjoy :D
