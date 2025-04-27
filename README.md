# cse-340---project-4-solved
**TO GET THIS SOLUTION VISIT:** [CSE 340 – Project 4 Solved](https://www.ankitcodinghub.com/product/cse-340-project-4-solved-3/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;10244&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE 340 – Project 4 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
<strong>Abstract</strong>

The goal of this project is to give you some hands-on experience with implementing a small compiler. You will write a compiler for a simple language. You will not be generating low level code. Instead, you will generate an intermediate representation (a data structure that represents the program). The execution of the program will be done after compilation by <em>interpreting </em>the generated intermediate representation.

<h1>1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Introduction</h1>
You will write a small compiler that will read an input program and represent it in an internal data structure. The data structure will contain representation of instructions to be executed as well as a part that represents the memory of the program (locations for variables). Then your compiler will execute the data structure (interpret it). This means that the program will traverse the data structure and at every node it visits, it will execute the node by changing the content of memory locations and deciding what is the next instruction to execute (program counter). The output of your compiler is the output that the input program should produce. These steps are illustrated in the following figure

<img data-recalc-dims="1" decoding="async" class="aligncenter lazyload" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/04/647.png?w=980&amp;ssl=1" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">The remainder of this document is organized as follows:

<ol>
<li><strong>Grammar </strong>Defines the programming language syntax including grammar.</li>
<li><strong>Execution Semantics </strong>Describe statement semantics for if, while, switch and print</li>
<li><strong>How to generate the intermediate representation </strong>Explains step by step how to generate the intermediate representation (data structure). You should read this sequentially and not skip around.</li>
<li><strong>Executing the intermediate representation </strong>Basically, you have two options. If you are using C/C++, you should use the code we provide to execute the intermediate representation. If you are using Java, it describes the strict rules to follow in executing the intermediate representation. Those rules will be enforced.</li>
<li><strong>Requirements </strong>Lists the programming languages you are allowed to use in your solution (C/C++ or Java) and other requirements.</li>
<li><strong>Grading </strong>Describes the grading scheme.</li>
<li><strong>Bonus Project </strong>Describes the requirements for the bonus project.</li>
</ol>
<h1>2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Grammar</h1>
The grammar for this project is a simplified form of the grammar from the previous project, but there are a couple extensions.

<table width="578">
<tbody>
<tr>
<td width="84"><em>program</em></td>
<td width="32">→</td>
<td width="227"><em>var section&nbsp;&nbsp;&nbsp; body</em></td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>var section</em></td>
<td width="32">→</td>
<td width="227"><em>id list </em>SEMICOLON</td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>id list</em></td>
<td width="32">→</td>
<td width="227">ID COMMA&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>id list </em>|&nbsp;&nbsp;&nbsp;&nbsp; ID</td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>body</em></td>
<td width="32">→</td>
<td width="227">LBRACE&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>stmt list </em>RBRACE</td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>stmt list</em></td>
<td width="32">→</td>
<td width="227"><em>stmt&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; stmt list </em>|&nbsp;&nbsp;&nbsp;&nbsp; stmt</td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>stmt</em></td>
<td width="32">→</td>
<td width="227"><em>assign stmt </em>| <em>print stmt </em>| <em>while stmt</em></td>
<td width="14">|</td>
<td width="45"><em>if stmt</em></td>
<td width="14">|</td>
<td width="71"><em>switch stmt</em></td>
<td width="14">|</td>
<td width="54"><em>for stmt</em></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>assign stmt</em></td>
<td width="32">→</td>
<td width="227">ID EQUAL&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>primary </em>SEMICOLON</td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>assign stmt</em></td>
<td width="32">→</td>
<td width="227">ID EQUAL&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>expr </em>SEMICOLON</td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>expr</em></td>
<td width="32">→</td>
<td width="227"><em>primary&nbsp;&nbsp;&nbsp; op&nbsp;&nbsp;&nbsp; primary</em></td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>primary</em></td>
<td width="32">→</td>
<td width="227">ID |&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; NUM</td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>op</em></td>
<td width="32">→</td>
<td width="227">PLUS | MINUS | MULT&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | DIV</td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>print stmt</em></td>
<td width="32">→</td>
<td width="227"><strong>print </strong>ID&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; SEMICOLON</td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>while stmt</em></td>
<td width="32">→</td>
<td width="227">WHILE <em>condition&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; body</em></td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>if stmt</em></td>
<td width="32">→</td>
<td width="227">IF&nbsp;&nbsp;&nbsp;&nbsp; <em>condition&nbsp;&nbsp;&nbsp; body</em></td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>condition</em></td>
<td width="32">→</td>
<td width="227"><em>primary&nbsp;&nbsp;&nbsp; relop&nbsp;&nbsp;&nbsp; primary</em></td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>relop</em></td>
<td width="32">→</td>
<td width="227">GREATER&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | LESS | NOTEQUAL</td>
<td width="14"></td>
<td width="45"></td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>switch stmt</em></td>
<td width="32">→</td>
<td colspan="3" width="286">SWITCH ID&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; LBRACE&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>case list </em>RBRACE</td>
<td width="14"></td>
<td width="71"></td>
<td width="14"></td>
<td width="54"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>switch stmt</em></td>
<td width="32">→</td>
<td colspan="5" width="371">SWITCH ID&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; LBRACE&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>case list&nbsp;&nbsp;&nbsp; default case&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </em>RBRACE</td>
<td colspan="2" width="68"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>for </em><em>stmt</em></td>
<td width="32">→</td>
<td colspan="5" width="371">FOR LPAREN <em>assign stmt&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; condition </em>SEMICOLON <em>assign </em><em>stmt</em></td>
<td colspan="2" width="68">RPAREN</td>
<td width="23"><em>body</em></td>
</tr>
<tr>
<td width="84"><em>case list</em></td>
<td width="32">→</td>
<td colspan="5" width="371"><em>case&nbsp;&nbsp;&nbsp;&nbsp; case list </em>|&nbsp;&nbsp;&nbsp;&nbsp; <em>case</em></td>
<td colspan="2" width="68"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>case</em></td>
<td width="32">→</td>
<td colspan="5" width="371">CASE NUM&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; COLON <em>body</em></td>
<td colspan="2" width="68"></td>
<td width="23"></td>
</tr>
<tr>
<td width="84"><em>default case</em></td>
<td width="32">→</td>
<td colspan="5" width="371">DEFAULT COLON <em>body</em></td>
<td colspan="2" width="68"></td>
<td width="23"></td>
</tr>
</tbody>
</table>
<strong>Some highlights of the grammar:</strong>

<ol>
<li>Expressions are greatly simplified and are not recursive.</li>
<li>There is no type declaration section.</li>
<li>Division is integer division and the result of the division of two integers is an integer.</li>
<li><em>if </em>statement is introduced. Note that <em>if stmt </em>does not have <em>else</em>.</li>
<li><em>for </em>statement is introduced. Note that <em>for </em>has a very general syntax similar to that of the C language for loop.</li>
<li>A <em>print </em>statement is introduced. Note that the <strong>print </strong>keyword is in lower case, but other keywords are all upper-case letters.</li>
<li>There is no variable declaration list. There is only one <em>id list </em>in the global scope and that contains all the variables.</li>
<li>There is no type specified for variables. All variables are int by default.</li>
</ol>
<h1>3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Execution Semantics</h1>
All statements in a statement list are executed sequentially according to the order in which they appear. Exception is made for body of <em>if stmt</em>, <em>while </em><em>stmt </em>and <em>switch </em><em>stmt </em>as explained below. In what follows, I will assume that all values are stored in locations even constants. This assumption is used by the execution procedure that we provide. This is not a restrictive assumption. For variables, you will have locations associated with them. For constants, you can reserve a location in which you store the constant (this is like having an unnamed immutable variable).

<h2>3.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Assignment Statement</h2>
To execute an assignment statement, the expression on the lefthand side of the equal sign is evaluated and the result is stored in the location associated with the righthand side of the expression.

<h2>3.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Expression</h2>
To evaluate an expression, the values in the locations associated with the two operands are obtained and the expression operator is applied to these values resulting in a value for the expression.

<h2>3.3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Boolean Condition</h2>
A boolean condition takes two operands as parameters and returns a boolean value. It is used to control the execution of <em>while </em>and <em>if </em>statements. To evaluate a condition, the values in the locations associated with the operands are obtained and the relational operator is applied to these values resulting in a true or false value. For example, if the values of the two operands a and b are 3 and 4 respectively, a &lt; b evaluates to <strong>true</strong>.

<h2>3.4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>If </em>statement</h2>
<em>if </em><em>stmt </em>has the standard semantics:

<ol>
<li>The condition is evaluated.</li>
<li>If the condition evaluates to <strong>true</strong>, the body of the <em>if </em><em>stmt </em>is executed, then the next statement following the <em>if </em>in the <em>stmt </em><em>list </em>is executed.</li>
<li>If the condition evaluates to <strong>false</strong>, the statement following the <em>if </em>in the <em>stmt </em><em>list </em>is executed These semantics apply recursively to nested <em>if </em><em>stmt</em>.</li>
</ol>
<h2>3.5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>While </em>statement</h2>
<em>while </em><em>stmt </em>has the standard semantics:

<ol>
<li>The condition is evaluated.</li>
<li>If the condition evaluates to <strong>true</strong>, the body of the <em>while stmt </em>is executed, then the condition is evaluated again and the process repeats.</li>
<li>If the condition evaluates to <strong>false</strong>, the statement following the <em>while stmt </em>in the <em>stmt </em><em>list </em>is executed.</li>
</ol>
These semantics apply recursively to nested <em>while stmt</em>. The code block:

<table width="594">
<tbody>
<tr>
<td width="594">WHILE <em>condition</em>

{ <em>stmt list</em>

}
</td>
</tr>
</tbody>
</table>
is equivalent to:

<table width="594">
<tbody>
<tr>
<td width="594"><em>label</em>: IF <em>condition</em>

{ <em>stmt list </em><strong>goto </strong><em>label</em>

}
</td>
</tr>
</tbody>
</table>
Note that <strong>goto </strong>statements do not appear in the input program, but our intermediate representation includes GotoStatement which is used in conjunction with IfStatement to represent <em>while </em>and <em>switch </em>statements.

<h2>3.6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>For </em>statement</h2>
The <em>for stmt </em>is very similar to the C language for statement. The semantics are defined by giving an equivalent construct.

<table width="594">
<tbody>
<tr>
<td width="594">FOR ( <em>assign stmt 1 condition </em>; <em>assign stmt 2 </em>)

{ <em>stmt list</em>

}
</td>
</tr>
</tbody>
</table>
is equivalent to:

<em>assign stmt 1</em>

WHILE <em>condition</em>

{

<em>stmt list assign stmt 2 </em>}

For example, the following snippet of code:

<table width="594">
<tbody>
<tr>
<td width="594">FOR ( a = 0; a &lt; 10; a = a + 1; )

{ print a;

}
</td>
</tr>
</tbody>
</table>
is equivalent to:

<table width="594">
<tbody>
<tr>
<td width="594">a = 0;

WHILE a &lt; 10

{ print a;

a = a + 1;

}
</td>
</tr>
</tbody>
</table>
<h2>3.7&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>Switch </em>statement</h2>
<em>switch stmt </em>has the following semantics<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>:

<ol>
<li>The value of the switch variable is checked against each case number in order.</li>
<li>If the value matches the number, the body of the case is executed, then the statement following the <em>switch stmt </em>in the <em>stmt list </em>is executed.</li>
<li>If the value does not match the number, next case is evaluated.</li>
<li>If a default case is provided and the value does not match any of the case numbers, then the body of the default case is executed and then the statement following the <em>switch stmt </em>in the <em>stmt </em><em>list </em>is executed.</li>
<li>If there is no default case and the value does not match any of the case numbers, then the statement following the <em>switch </em><em>stmt </em>in the <em>stmt list </em>is executed. These semantics apply recursively to nested <em>switch stmt</em>. The code block:</li>
</ol>
<table width="594">
<tbody>
<tr>
<td width="594">SWITCH <em>var </em>{

CASE <em>n</em><sub>1 </sub>: { <em>stmt list 1 </em>}

…

CASE <em>n<sub>k </sub></em>: { <em>stmt list </em><em>k </em>}

}
</td>
</tr>
</tbody>
</table>
is equivalent to:

<table width="594">
<tbody>
<tr>
<td width="594">IF <em>var </em>== <em>n</em><sub>1 </sub>{

<em>stmt list </em><em>1 </em><strong>goto </strong><em>label</em>

}

…

IF <em>var </em>== <em>n<sub>k </sub></em>{

<em>stmt list </em><em>k </em><strong>goto </strong><em>label</em>

}

<em>label</em>:
</td>
</tr>
</tbody>
</table>
And for switch statements with default case, the code block:

<table width="594">
<tbody>
<tr>
<td width="594">SWITCH <em>var </em>{

CASE <em>n</em><sub>1 </sub>: { <em>stmt list 1 </em>}

…

CASE <em>n<sub>k </sub></em>: { <em>stmt list </em><em>k </em>}

DEFAULT : { <em>stmt list default </em>}

}
</td>
</tr>
</tbody>
</table>
is equivalent to:

<table width="594">
<tbody>
<tr>
<td width="594">IF <em>var </em>== <em>n</em><sub>1 </sub>{

<em>stmt list </em><em>1 </em><strong>goto </strong><em>label</em>

}

…

IF <em>var </em>== <em>n<sub>k </sub></em>{

<em>stmt list </em><em>k </em><strong>goto </strong><em>label</em>

}

<em>stmt list default</em>

<em>label</em>:
</td>
</tr>
</tbody>
</table>
<h2>3.8&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>Print </em>statement</h2>
The statement print a; prints the value of variable a at the time of the execution of the <em>print </em>statement.

<h1>4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; How to generate the code</h1>
The intermediate code will be a data structure (a graph) that is easy to interpret and execute. I will start by describing how this graph looks for simple assignments then I will explain how to deal with <em>while </em>statements.

Note that in the explanation below I start with incomplete data structures then I explain what is missing and make them more complete. You should read the whole explanation.

<h2>4.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Handling simple assignments</h2>
A simple assignment is fully determined by: the operator (if any), the id on the left-hand side, and the operand(s). A simple assignment can be represented as a node:

struct AssignmentStatement { struct ValueNode* left_hand_side; struct ValueNode* operand1; struct ValueNode* operand2;

ArithmeticOperatorType op; // operator }

The operator of an assignment statement without an expression on the righthand side is set to OPERATOR NONE and there is only one operand. To execute an assignment, you need the values of the operand(s), apply the operator, if any, to the operands and assign the resulting value of the right-hand side to the left hand side. For literals (NUM), the value is the value of the number. For variables, the value is the last value stored in the location associated with the variable. <strong>Initially, all variables are initialized to 0</strong>.

Multiple assignments are executed one after another. So, we need to allow multiple assignment nodes to be linked to each other. This can be achieved as follows:

struct AssignmentStatement { struct ValueNode* left_hand_side; struct ValueNode* operand1; struct ValueNode* operand2;

ArithmeticOperatorType op; // operator struct AssignmentStatement* next;

}

This structure only accepts ValueNode as operands. To handle literal constants (NUM), you need to create ValueNode or them and initialize the value stored in these value nodes to the constant value. This initialization, as well as the initialization of values in locations associated with variable is done while parsing.

This will now allow us to execute a sequence of assignment statements represented in a linkedlist: we start with the head of the list, then we execute every assignment in the list one after the other.

<strong>Begin Note </strong>It is important to distinguish between compile-time initialization and runtime execution. For example, consider the program

a, b;

{

a = 3; b = 5;

}

The intermediate representation for this program will have have two assignment statements: one to copy the value in the location that contains the value 3 to the location associated with a and one to copy the value in the location that contains the value 5 to the location associated with b. The values 3 and 5 will not be copied to the locations of a and b at compile-time. <strong>End Note</strong>

This is simple enough, but does not help with executing other kinds of statements. We consider them one at a time.

<h2>4.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Handling <em>print </em>statements</h2>
The <em>print </em>statement is straightforward. It can be represented as

struct PrintStatement

{ struct ValueNode* id;

}

Now, we ask: how can we execute a sequence of statements that are either assignments or print statements (or other types of statements)? We need to put both kinds of statements in a list and not just the assignment statements as we did above. So, we introduce a new kind of node: a statement node. The statement node has a field that indicates which type of statement it is. It also has fields to accommodate the remaining types of statements. It looks like this:

struct StatementNode {

StatementType type; // NOOP_STMT, GOTO_STMT, ASSIGN_STMT, IF_STMT, PRINT_STMT

union { struct AssignmentStatement* assign_stmt; struct PrintStatement* print_stmt; struct IfStatement* if_stmt; struct GotoStatement* goto_stmt;

}; struct StatementNode* next;

}

This way we can go through a list of statements and execute one after the other. To execute a particular node, we check its type. If it is PRINT STMT, we execute the print stmt field, if it is ASSIGN STMT, we execute the assign stmt field and so on. With this modification, we do not need a next field in the AssignmentStatement structure (as we explained above), instead, we put the next field in the statement node.

This is all fine, but we do not yet know how to generate the list to execute later. The idea is to have the functions that parse non-terminals return the code for the non-terminals. For example for a statement list, we have the following pseudocode (missing many checks):

struct StatementNode* parse_stmt_list()

{ struct StatementNode* st; // statement struct StatementNode* stl; // statement list

st = parse_stmt(); if (nextToken == start of a statement list)

{ stl = parse_stmt_list();

append stl to st;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; // this is pseudocode

return st;

} else { ungetToken(); return st;

}

}

And to parse <em>body </em>we have the following pseudocode:

struct StatementNode* parse_body()

{ struct StatementNode* stl;

match LBRACE stl = parse_stmt_list(); match RBRACE

return stl;

}

<h2>4.3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Handling <em>if </em>and <em>while </em>statements</h2>
More complications occur with <em>if </em>and <em>while </em>statements. The structure for an <em>if </em>statement can be as follows:

struct IfStatement {

ConditionalOperatorType condition_op; struct ValueNode* condition_operand1; struct ValueNode* condition_operand2;

struct StatementNode* true_branch; struct StatementNode* false_branch;

}

The condition op, condition operand1 and condition operand2 fields are the operator and operands of the condition of the <em>if </em>statement. To generate the node for an <em>if </em>statement, we need to put together the <em>condition</em>, and <em>stmt list </em>that are generated in the parsing of the <em>if </em>statement.

The true branch and false branch fields are crucial to the execution of the <em>if </em>statement. If the condition evaluates to true then the statement specified in true branch is executed otherwise the one specified in false branch is executed. We need one more type of node to allow loop back for <em>while </em>statements. This is a GotoStatement.

struct GotoStatement { struct StatementNode* target;

}

To generate code for <em>while </em>and <em>if </em>statements, we need to put a few things together. The outline given above for <em>stmt </em><em>list </em>needs to be modified as follows (this is missing details and shows only the main steps).

struct StatementNode* parse_stmt()

{ …

create statement node st if next token is IF

{ st-&gt;type = IF_STMT;

create if-node;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; // note that if-node is pseudocode and is not

// a valid identifier in C, C++ or Java

st-&gt;if_stmt = if-node;

parse the condition and set if-node-&gt;condition_op, if-node-&gt;condition_operand1 and if-node-&gt;condition_operand2

if-node-&gt;true_branch = parse_body();&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; // parse_body returns a pointer to a list of statements

create no-op node&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; // this is a node that does not result

// in any action being taken

append no-op node to the body of the if&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; // this requires a loop to get to the end of

// if-node-&gt;true_branch by following the next field

// you know you reached the end when next is NULL

// it is very important that you always appropriately

// initialize fields of any data structures // do not use uninitialized pointers

set if-node-&gt;false_branch to point to no-op node set st-&gt;next to point to no-op node

…

} else …

}

The following diagram shows the desired structure for the <em>if </em>statement:

The <em>stmt list </em>code should be modified because of the extra no-op node:

struct StatementNode* parse_stmt_list()

{ struct StatementNode* st; // statement struct StatementNode* stl; // statement list

st = parse_stmt(); if (nextToken == start of a statement list)

{ stl = parse_stmt_list();

if st-&gt;type == IF_STMT

{ append stl to the no-op node that follows st

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; st

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; V

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; no-op

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; V

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; stl

} else { append stl to st;

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; st

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; V

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; stl

} return st;

} else { ungetToken(); return st;

}

}

Handling <em>while </em>statement is similar. Here is the outline for parsing a <em>while </em>statement and creating the data structure for it:

…

create statement node st if next token is WHILE

{

<table width="445">
<tbody>
<tr>
<td width="242">st-&gt;type = IF_STMT;</td>
<td width="203">// handling WHILE using if and goto nodes</td>
</tr>
<tr>
<td width="242">create if-node</td>
<td width="203">// if-node is not a valid identifier see

// corresponding comment above
</td>
</tr>
</tbody>
</table>
st-&gt;if_stmt = if-node parse the condition and set if-node-&gt;condition_op, if-node-&gt;condition_operand1 and if-node-&gt;condition_operand2 if-node-&gt;true_branch = parse_body();

<table width="450">
<tbody>
<tr>
<td width="242">create a new statement node gt gt-&gt;type = GOTO_STMT;</td>
<td width="207">// This is of type StatementNode</td>
</tr>
<tr>
<td width="242">create goto-node gt-&gt;goto_stmt = goto-node;</td>
<td width="207">// This is of type GotoStatement</td>
</tr>
<tr>
<td width="242">goto-node-&gt;target = st;</td>
<td width="207">// to jump to the if statement after

// executing the body
</td>
</tr>
<tr>
<td width="242">append gt to the body of the while</td>
<td width="207">// append gt to the body of the while // this requires a loop. check the comment // for the if above.</td>
</tr>
</tbody>
</table>
create no-op node set if-node-&gt;false_branch to point to no-op node set st-&gt;next to point to no-op node

} …

The following diagram shows the desired structure for the <em>while </em>statement:

<h2>4.4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Handling <em>switch </em>statement</h2>
You can handle the <em>switch </em>statement similarly. Use a combination of IfStatement and GotoStatement to support the semantics of the <em>switch </em>statement. See section 3.7 for the semantics of the <em>switch </em>statement.

<h1>5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Executing the intermediate representation</h1>
After the graph data structure is built, it needs to be executed. Execution starts with the first node in the list. Depending on the type of the node, the next node to execute is determined. The general form for execution is illustrated in the following pseudo-code.

pc = first node while (pc != NULL)

{ switch (pc-&gt;type)

{ case ASSIGN_STMT: // code to execute pc-&gt;assign_stmt …

pc = pc-&gt;next

case IF_STMT:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; // code to evaluate condition …

// depending on the result

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; pc = pc-&gt;if_stmt-&gt;true_branch

// or

//&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; pc = pc-&gt;if_stmt-&gt;false_branch

case NOOP_STMT: pc = pc-&gt;next

case GOTO_STMT: pc = pc-&gt;goto_stmt-&gt;target

case PRINT_STMT: // code to execute pc-&gt;print_stmt …

pc = pc-&gt;next

}

}

<strong>JAVA Implementation: Executing the graph should be done non-recursively and without</strong>

<strong>any function calls.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Even helper functions are not allowed for the execution of the</strong>

<strong>graph. This is a requirement that will be checked by inspecting your code. Little credit will be assigned if this requirement is not met.</strong>

<strong>C/C++ implementations&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>If you are developing in C/C++, we have provided you with the data

structures and the code to execute the graph and <strong>you must use it</strong>. There are two files compiler.h and compiler.cc. You need to write your code in separate file(s) and #includecompiler.h. The

entry point of your code is a function declared in compiler.h: struct StatementNode* parse_generate_intermediate_representation();

You need to implement this function. The main() function is provided in compiler.cc:

int main()

{ struct StatementNode * program;

program = parse_generate_intermediate_representation(); execute_program(program); return 0;

}

It calls the function that you will implement which is supposed to parse the program and generate the intermediate representation, then it calls the execute program function to execute the program. You should not modify any of the given code. In fact if you write your program in C/C++, you should only submit the file(s) that contain your own code and we will add the given part and compile the code before testing. If you write your program in Java, you should strictly follow the guidelines for executing the intermediate representation.

<h1>6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Requirements</h1>
<ol>
<li>Write a compiler that generates intermediate representation for the code and write an interpreter to execute the intermediate representation. The interpreter is provided for C/C++ implementations.</li>
<li><strong>Language: </strong>You can use Java, C, or C++ for this assignment.</li>
<li><strong>Any language other than Java, C or C++ is not allowed for this project</strong>.</li>
<li>If you use C/C++ for this project, you should use the provided code and only implement the required functions.</li>
<li>If you use Java, you will need to write everything yourself. The requirements on how to execute the intermediate representation will be checked manually when grading.</li>
<li><strong>Platform: </strong>As in previous projects, the reference platform is CentOS 7</li>
<li><strong>You can assume that there are no syntax or semantic errors in the input program.</strong></li>
</ol>
&nbsp;

<h1>8&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Bonus Project</h1>
<h2>8.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Bonus Project Options</h2>
You have three options for the bonus project:

<ol>
<li>Resubmit project 2. For this option you are given another chance to submit project 2. The grade you obtain will be reduced by 30% and replaces the grade you already obtained on project 2. So, if your grade for project 2 was 20 and your grade for the replacement is 90, the grade for project 2 will be changed from 20 to 63 (63 = 90 reduced by 30%)</li>
<li>Resubmit project 3. For this option you are given another chance to submit project 3. The grade you obtain will be reduced by 30% and replaces the grade you already obtained on project 3. So, if your grade for project 3 was 20 and your grade for the replacement is 100, the grade for project 3 will be changed from 20 to 70 (70 = 100 reduced by 30%)</li>
<li>Do a new project (advanced compiler) that replaces the lowest grade between project 2 and project 3. The grade you obtain under this option will replace the lower of the two grades that you obtained on project 2 or 3 (if the grade you obtain on the bonus is lower than what you already got on projects 2 and 3, no replacement is made).</li>
</ol>
If you make multiple submissions, only the last submission will count.

<h2>8.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Advanced Compiler (option 3)</h2>
Support the following grammar:

<em>program </em>→ <em>var section body var section </em>→ VAR <em>int var decl array </em><em>var decl int var decl </em>→ <em>id list </em>SEMICOLON <em>array var decl </em>→ <em>id list </em>COLON ARRAY LBRAC NUM RBRAC SEMICOLON

<em>id list&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </em>→&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ID COMMA&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>id list </em>| ID

<table width="516">
<tbody>
<tr>
<td width="91"><em>body</em></td>
<td width="35">→</td>
<td colspan="2" width="260">LBRACE&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>stmt list </em>RBRACE</td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>stmt list</em></td>
<td width="35">→</td>
<td colspan="2" width="260"><em>stmt&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; stmt list </em>| stmt</td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>stmt assign stmt</em></td>
<td width="35">→

→
</td>
<td colspan="2" width="260"><em>assign stmt </em>| <em>print stmt </em>| <em>while stmt </em>| <em>var access </em>EQUAL <em>expr </em>SEMICOLON</td>
<td width="49"><em>if </em><em>stmt</em></td>
<td width="15">|</td>
<td colspan="2" width="66"><em>switch </em><em>stmt</em></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>var access</em></td>
<td width="35">→</td>
<td colspan="2" width="260">ID | ID LBRAC <em>expr </em>RBRAC</td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>expr</em></td>
<td width="35">→</td>
<td colspan="2" width="260"><em>term </em>PLUS <em>expr</em></td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>expr</em></td>
<td width="35">→</td>
<td colspan="2" width="260"><em>term</em></td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>term</em></td>
<td width="35">→</td>
<td colspan="2" width="260"><em>factor </em>MULT <em>term</em></td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>term</em></td>
<td width="35">→</td>
<td colspan="2" width="260"><em>factor</em></td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>factor</em></td>
<td width="35">→</td>
<td colspan="2" width="260">LPAREN <em>expr </em>RPAREN</td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>factor</em></td>
<td width="35">→</td>
<td colspan="2" width="260">NUM</td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>factor</em></td>
<td width="35">→</td>
<td colspan="2" width="260"><em>var </em><em>access</em></td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>print stmt while stmt</em></td>
<td width="35">→

→
</td>
<td colspan="2" width="260"><strong>print </strong><em>var access </em>SEMICOLON

WHILE <em>condition&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; body</em>
</td>
<td width="49"></td>
<td width="15"></td>
<td colspan="2" width="66"></td>
<td width="5"></td>
</tr>
<tr>
<td width="91"><em>if stmt</em></td>
<td width="35">→</td>
<td width="259">IF <em>condition&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; body</em></td>
<td colspan="4" width="78"></td>
<td colspan="2" width="57"></td>
</tr>
<tr>
<td width="91"><em>condition</em></td>
<td width="35">→</td>
<td width="259"><em>expr&nbsp;&nbsp;&nbsp; relop&nbsp;&nbsp; expr</em></td>
<td colspan="4" width="78"></td>
<td colspan="2" width="57"></td>
</tr>
<tr>
<td width="91"><em>relop</em></td>
<td width="35">→</td>
<td width="259">GREATER | LESS | NOTEQUAL</td>
<td colspan="4" width="78"></td>
<td colspan="2" width="57"></td>
</tr>
<tr>
<td width="91"><em>switch stmt</em></td>
<td width="35">→</td>
<td width="259">SWITCH <em>var access </em>LBRACE&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>case </em><em>list</em></td>
<td colspan="4" width="78">RBRACE</td>
<td colspan="2" width="57"></td>
</tr>
<tr>
<td width="91"><em>switch stmt</em></td>
<td width="35">→</td>
<td width="259">SWITCH <em>var access </em>LBRACE&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>case </em><em>list</em></td>
<td colspan="4" width="78"><em>default case</em></td>
<td colspan="2" width="57">RBRACE</td>
</tr>
<tr>
<td width="91"><em>case list</em></td>
<td width="35">→</td>
<td width="259"><em>case&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; case </em><em>list </em>| <em>case</em></td>
<td colspan="4" width="78"></td>
<td colspan="2" width="57"></td>
</tr>
<tr>
<td width="91"><em>case</em></td>
<td width="35">→</td>
<td width="259">CASE NUM&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; COLON <em>body</em></td>
<td colspan="4" width="78"></td>
<td colspan="2" width="57"></td>
</tr>
<tr>
<td width="91"><em>default </em><em>case</em></td>
<td width="35">→</td>
<td width="259">DEFAULT COLON&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <em>body</em></td>
<td colspan="4" width="78"></td>
<td colspan="2" width="57"></td>
</tr>
<tr>
<td width="91"></td>
<td width="35"></td>
<td width="256"></td>
<td width="1"></td>
<td width="49"></td>
<td width="15"></td>
<td width="13"></td>
<td width="53"></td>
<td width="5"></td>
</tr>
</tbody>
</table>
Note that LBRAC is “[” and LBRACE is “{“. The former is used for arrays and the latter is used for body. Assume that all arrays are integer arrays and are indexed from 0 to <em>size </em>– 1, where <em>size </em>is the size of the array specified in the <em>var </em><em>section </em>after the ARRAY keyword and between “[” and “]”.

The data structures and code that we have provided for the regular assignment will not be enough for the bonus, you will need to modify those to support arrays. Submit <em>all </em>code files for the bonus project (including the modified compiler.h and compiler.cc).

<strong>All restrictions imposed on the execution of the intermediate representation for the regular project apply to the bonus project as well. You are not allowed to call any functions while executing the intermediate representation. You are not allowed to execute the program recursively.</strong>

<a href="#_ftnref1" name="_ftn1">[1]</a> The switch statement in the C language has different syntax and semantics. It is also more dangerous!
