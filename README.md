14_pre_commit_hook
===================

After cloning this repository, pre-commit file must be placed into .git/hooks. 

Then pre-commit file must be given execute permission. 

Usage
-----
**Before fixing the bug**
```
~/14_pre_commit_hook$ git commit -m "random commit"
.E..
======================================================================
ERROR: test_returns_none_for_complex_solution (__main__.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 22, in test_returns_none_for_complex_solution
    root1, root2 = get_roots(1, 2, 3)
  File "/home/kajoj/14_pre_commit_hook/quadratic_equation.py", line 6, in get_roots
    root1 = (-b - sqrt(discriminant)) / (2 * a)
ValueError: math domain error

----------------------------------------------------------------------
Ran 4 tests in 0.001s

FAILED (errors=1)
         
```
**After fixing the bug**
```
~/14_pre_commit_hook$ git commit -m "random commit"
....
----------------------------------------------------------------------
Ran 4 tests in 0.000s

OK
[master de2ce83] random commit
 1 file changed, 2 insertions(+), 2 deletions(-)

```
