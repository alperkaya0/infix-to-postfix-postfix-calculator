# infix-to-postfix-postfix-calculator
Converts Infix to Postfix and then solves it by using postfix.
Uses a stack to convert, uses 2 stacks to solve it by using postfix.
<br><br><br>
Example Output:<br>
Infix is: 1+2*1/((2-1))+((3-1)/1-(2+(2*1)))<br>
[]<br>
1<br>
[+]<br>
1<br>
[+]<br>
12<br>
[+, *]<br>      
12<br>
[+, *]<br>      
121<br>
[+, /]<br>      
121*<br>        
[+, /, (]<br>   
121*<br>        
[+, /, (, (]<br>
121*<br>        
[+, /, (, (]<br>
121*2<br>
[+, /, (, (, -]<br>
121*2<br>
[+, /, (, (, -]<br>
121*21<br>
[+, /, (]<br>
121*21-<br>
[+, /]<br>
121*21-<br>
[+]<br>
121*21-/+<br>
[+, (]<br>
121*21-/+<br>
[+, (, (]<br>
121*21-/+<br>
[+, (, (]<br>
121*21-/+3<br>
[+, (, (, -]<br>
121*21-/+3<br>
[+, (, (, -]<br>
121*21-/+31<br>
[+, (]<br>
121*21-/+31-<br>
[+, (, /]<br>
121*21-/+31-<br>
[+, (, /]<br>
121*21-/+31-1<br>
[+, (, -]<br>
121*21-/+31-1/<br>
[+, (, -, (]<br>
121*21-/+31-1/<br>
[+, (, -, (]<br>
121*21-/+31-1/2<br>
[+, (, -, (, +]<br>
121*21-/+31-1/2<br>
[+, (, -, (, +, (]<br>
121*21-/+31-1/2<br>
[+, (, -, (, +, (]<br>
121*21-/+31-1/22<br>
[+, (, -, (, +, (, *]<br>
121*21-/+31-1/22<br>
[+, (, -, (, +, (, *]<br>
121*21-/+31-1/221<br>
[+, (, -, (, +]<br>
121*21-/+31-1/221*<br>
[+, (, -]<br>
121*21-/+31-1/221*+<br>
[+]<br>
121*21-/+31-1/221*+-<br>
Postfix: 121*21-/+31-1/221*+-+<br>
[+, -, +, *, 1, 2, 2, /, 1, -, 1, 3, +, /, -, 1, 2, *, 1, 2, 1]   :   [1, 2, 1, *]<br>
[+, -, +, *, 1, 2, 2, /, 1, -, 1, 3, +, /, -, 1, 2, 2, 1]   :   [1, 2, 2, 1, -]<br>
[+, -, +, *, 1, 2, 2, /, 1, -, 1, 3, +, /, 1, 2, 1]   :   [1, 2, 1, /]<br>
[+, -, +, *, 1, 2, 2, /, 1, -, 1, 3, +, 2, 1]   :   [1, 2, +]<br>
[+, -, +, *, 1, 2, 2, /, 1, -, 1, 3, 3]   :   [3, 3, 1, -]<br>
[+, -, +, *, 1, 2, 2, /, 1, 2, 3]   :   [3, 2, 1, /]<br>
[+, -, +, *, 1, 2, 2, 2, 3]   :   [3, 2, 2, 2, 1, *]<br>
[+, -, +, 2, 2, 2, 3]   :   [3, 2, 2, 2, +]<br>
[+, -, 4, 2, 3]   :   [3, 2, 4, -]<br>
[+, ., 3]   :   [3, ., +]<br>
Answer: 1<br>
