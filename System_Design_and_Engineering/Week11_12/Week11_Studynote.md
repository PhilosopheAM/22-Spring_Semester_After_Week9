# Integer linear programming 整数优化
Programming 是运筹学的说法，Optimizing 是计算机、统计学那边的叫法。
求解整数优化问题(ILP)的两种基本办法是：
+ Cutting plane methods
+ Enumerative methods

## Cutting Plane Methods 切割平面法

**The gerneral intent of cutting plane methods for solving ILP**

Let's talk about the oldest cutting plane method, it has **several principles**:
+ A cut never excludes any integer solution from the new feasible region.
+ Each cut will reduce the feasible region of the original LP problem.
+ Each cut passes through at least one integer point.
+ In a finte number of steps, the ILP problem is solved(can be solved) as an LP problem.

