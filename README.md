Compiler Project for CSCI489


Language Grammar:

BNF Grammar

<program> ::= <st group> ## | <decl part>  <st group> ##



<decl part> ::= declare <declare list> enddeclare

<decl list> ::= <decl> | <decl list> ; <decl>

<decl> ::=  integer <identifier list>



<st group> ::= <st> | <st group> ; <st>

<st> = <asgn> | <read> | <write> | <cond> | <loop>



<read> ::= read <identifier list>

<write> ::= write <output list>



<identifier list> ::= <identifier> | <identifier list> , <identifier>

<output list> ::= <expression> | <quote> | <output list> , <expression>
		                                                    | <output list> , <quote>


<quote> ::= ‘ <word> ‘

<word> ::= <letter> | <digit> | <word> <letter> | <word> <digit>



<identifier> ::= <letter> | <identifier> <letter> | <identifier> <digit>

<letter>::=a | b | c | d | e | f | g | h | i | j | k | l | m | n | o | p | q |
                    r | s | t | u | v | w | x | y | z

<digit> ::= 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9

<const> ::= <digit> | - <digit> | <const> <digit> 
