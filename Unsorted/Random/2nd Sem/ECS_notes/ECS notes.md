3rd Unit

10 marks
1)Compiler, parse tree, xml
2)Converting jack to vm using compiler block diagram and explain tokenizer, parser, code gen some simple examples convert to vm
3)OS types, OS features jack Os specifications (jack lang n jack os specifications diff); 5 to 6 marks


![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250623210232.png)

COMPILATION

  **Syntax Analysis**
   1. Tokenizing or Lexical Analysis: Grouping of input characters to tokens.
      - A tokenizer or scanner divides the source code into individual units known as tokens. It groups them based on predefined rules and patterns.
      - In Jack, there are 5 types of tokens:
        - **Keywords**: `class`, `constructor`, `function`, `void`, `false`
        - **Symbols**: `!`, `{`, `;`, `.`, `+`, `&`
        - **Integers**: Decimal numbers from 0 to 32767
        - **Strings**: Sequence of unique code characters; no `"` or `!` new line
        - **Identifiers**: A name given by user to variable, method, function, class etc
        - **Tokens**: The smallest meaningful unit in a programming language, such as keywords, identifiers, operators, constants, and punctuation symbols.
   
   2. Parsing: Grouping of tokens into structured statements with meaning. These tasks are independent of the target language.
      - Determining if the given input is accepted by grammar.
      - It involves breaking down input into a hierarchical structure, like a parse tree or Abstract Syntax Tree (AST).
      - A parse tree captures every derivation step, including terminal and non-terminals.
      - A syntax error during parsing makes the parsing either halt or report and attempt recovery of the error, providing meaningful error messages.
      - Common parsing algorithms include:
        - Recursive Descent Parsing
        - LL Parsing
        - Shift-Reduce Parsing
        - LR Parsing
      - **Grammar**: A set of rules and order describing how tokens can be combined to create a valid programming language.

		![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624124840.png)

		![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624124906.png)

- A syntax analyser is a program that performs both tokenizing and parsing.
	- The purpose of SA is to process a Jack program and  understand its syntactic structure according to the Jack grammar.
			  
 1) Code Generation
	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624100006.png)
 - Code generation, divided into six sections. 
	1. How compilers use symbol tables for mapping symbolic variables onto virtual memory segments. 
	2. Algorithms for compiling expressions and strings of characters.
	3. Techniques for compiling statements like let, if, while, do, and return. 
	4. Ability to compile variables, expressions, and statements.
	5. The compilation of objects and arrays. 
	6. Mapping Jack programs on the VM platform and language

	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624121542.png)
	
	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624121824.png)

	The compiler handles each…
	•field variable declaration by adding a field i entry to the class-level symbol table
	•static variable declaration by adding a static i entry to the class-level symbol table
	• parameter variable declaration by adding an argument i entry to the subroutine-level
	  symbol table
	•var variable declaration by adding a local i entry to the subroutine-level symbol table.

	Each field, static, local, parameter variable name in the source code is translated
	into this i, static i, local i , argument i, in the generated VM code.

	- Analyser generates infix expression in high level code to infix expression in xml code
	  but compiler turns it into postfix during vmcode compilation
	
	- Jack Lang has no operator priority but compileExpression algorithm evaluates expressions in paranthesis first.

	- Object-oriented languages typically handle strings as instances of a class named String.

	- The Jack programming language features five statements
	1. let,
	2. do,
	3. return,
	4. if,
	5. while.

	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624123600.png)

	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624123650.png)

	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624123726.png)

	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624123812.png)


	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624123833.png)

	-  Each object is physically implemented as a memory block,which can be accessed through static, field, local, or argument variables.
	- The reference variable, also known as an object variable or pointer, contains the base address of the memory block.
	- Once an object is no longer required, its memory block can be freed and returned to the heap for reuse.
	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624124308.png)

	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624124526.png)

	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624124606.png)

	![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250624124636.png)