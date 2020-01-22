## Part a

### Describe what the code in `z3-test.py` is doing in a paragraph or two.

z3-test.py first seems to define two boolean variables ("a" and "b") and two integer variables ("x" and "y"). It then finds assignments for these variables which satisfy a set of logical conditions. For the boolean variables, it simply chose the only pair of boolean states (False and True) which satisfied the requirements of having 

(NOT a) AND b

Interestingly, for the integer variables it chose the largest possible value of x and the smallest possible value of y given that value of x.

It then printed these assignments to show that these logical conditions could be satisfied. Finally, it attempted to satisfy these logical conditions (as one giant AND clause) as well as a SEPARATE a new logical condition (that y < 1), which was now impossible (since for integers if y < 1, y <= 0, and so x < y requires x < 0, but x > 0), and so it told us that this new string of logical conditions was unsatisfiable.

I will add that it is unclear if the program attempted to reassign values or if it simply checked if the value we get for y (which we know to be 100) in (possibly re-)doing this first set of AND clauses was less than 1.