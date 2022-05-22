
````
DOCTYPE - md & Katex. 使用基于Pandoc的渲染器输出PDF文档
Copyright is reserved by Harry Chen. If you have any problem, please contact the author through 11911421@mail.sustech.edu.cn
````

# Intro to Metaheuristics
> Reference : Boyed的Intro. Charpter 14.


### Def of heuristic method- 

A heuristic method is a procedure that is likely to discover a very good feasible solution but not necessarily an optimal solution(for the specific problem being considered)... can provide a silution that is at least nearly optimal(or conclude that no such solutions exist).

### The drawbacks of heuristic method- 

Heuristic method often are based on relatively simple common-sense ideas for how to search for a good solution.

*Comment: 比方说“仿生启发式算法”就是从自然界中的组织方式与行为方式得到“直觉的”灵感*

这些simple common-sense的ideas需要被carefully tailored来适应特定的问题。因此这些heuristics的方法 is designed to fit a specific problem type rather than a variety of applications.(启发式算法的针对性)

### Def of Meta-heuristics methods-

A metaheuristics is a general solution method that provides both a general structure and strategy guidelines for developing a specific heristic method to fit a paticular kind of problem.
简单来说就是：元启发式算法并不需要针对具体问题的情况设计特例的结构。元启发式算法式一大类问题的通解——基于启发式算法的特性，但是适用范围更广、约束更少。

### The nature of meta-heuristics
我们首先参考一个问题：
![](source/img/Reference-Chapter14-figure14.1.png)
用一个简单的gradient search procedure做，假设从$x=0$开始作为inistial trial silution,那么会在$x=5$的时候停下来（因为达到了一个local optima.
或者以另一种方法 the bisection method 二分法来做，取 lower bound $x=0$ 和 upper bound $x=6$可以看到 sequence of trial solutions obtained 是 $x=3, x=4.5, x=4.825$即不断地逼近local optima $x=5$. 这是一个更加明显、典型的local improvement procedure.
