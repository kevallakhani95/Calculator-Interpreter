# Calculator-Interpreter

This is my first code towards developing an Interpreter. Since, it is my first take on developing an Interpreter from scratch,
I figured I would develop one for a calculator using Python. 
Consider calculator input (for eg. 5+3, 5-8*9, 5*(2-1) and more) as a language.

To produce an output to this language you need to follow various procedures - 
1. Lexical analysis of the input.
2. Parse the input and build a tree structure of the input data.
3. Interpret the input and visit the tree in a post-order form to produce the result.
4. Print the result to the output console.

This is a recursive-descent parser / interpreter and the grammer for the same is given below - 
expr : term((PLUS | MINUS) term)*
term : factor((MUL | DIV) factor)*
factor : (PLUS | MINUS) factor | INTEGER | LPAREN expr RPAREN

It is known as a recursive descent parser since, it is a kind of top-down parser built from a set of mutually 
recursive procedures (or a non-recursive equivalent) where each such procedure usually implements one of the productions of the grammar.

To run the file - 
Simply go to cmd prompt and run the calculator_interpreter.py file. Keep giving inputs / expressions as long as you want.
Enjoy :D
