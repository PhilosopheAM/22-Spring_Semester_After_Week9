# 单纯形法及应用练习
````
DOCTYPE - md & Katex. 使用基于Pandoc的渲染器输出PDF文档
Copyright is reserved by Harry Chen. If you have any problem, please contact the author through 11911421@mail.sustech.edu.cn
````

单纯形法的知识前提：图片从右向左看
![](source/img/Basic%20Feasible%20solution%20基本可行解%20说明.png '图源来自：SDM223_第10周课件_王振坤_20220420')
当解出$\vec x = \left(\vec B\mathop{{}}\nolimits^{{-1}}b,0\right)^T$得到基本解(Basic solution).
当满足$\vec B\mathop{{}}\nolimits^{{-1}}b\ge0$，称$x$为一个基本可行解(Basic feasible solution).
![](source/img/什么是基本可行解.png '图源来自：https://youtu.be/0P5OAcXdUec')

![](source/img/什么是基本可行解(Basic%20feasible%20solution).png)

## 什么是“凸 Convex”和“凹 Concave” ？
参考资料：
+ [什么是凸组合(Convex combination)？](https://zh.wikipedia.org/wiki/%E5%87%B8%E7%BB%84%E5%90%88)
+ [Convex combination的一个特殊情况：两个向量的convex combination](https://www.youtube.com/watch?v=qy9jB5ydxGo)
+ [Operation Research Course 这个的课程蛮好](https://www.youtube.com/watch?v=a_gRfwHUlhQ)，口音清晰，讲解清楚，比......

**凸组合 Convex Combination**的定义是：
$$
\begin{cases}
x = \lambda_1x_1+\lambda_2x_2+...+\lambda_kx_k\\
\lambda_1,\lambda_2,...\lambda_k\in\left[0,1\right]\\
\lambda_1+\lambda_2+...+\lambda_k=1\quad or\quad \sum\limits^{^N}_{i=1} \lambda_i = 1
\end{cases}
$$  

这里还有一个严格凸组合(Strict convex combination)的定义，仅仅需要将 Convex combination's definition约束到：
$$\lambda_1,\lambda_2,...\lambda_k\in\left(0,1\right)$$

**什么是凸集 Convex Set** - 

![](source/img/凸集的定义.png '图源来自：https://youtu.be/a_gRfwHUlhQ')

上排为Convex Set, 下排为 Non-Convex Set:
![](source/img/Convex%20Set%20示意.png '图源来自：https://youtu.be/a_gRfwHUlhQ')
**补充** -
+ Given a convex set $S$ and $x\in S, x_1\in S, x_2\in S, x_1\ne x_2$, for any $ \lambda \in \left(0,1\right), x\ne \lambda x_1+\left(1-\lambda\right)x_2$, **then $S$ is a vertex of $S$**
![](source/img/图示凸集合.png '图源来自：SDM223_第10周课件_王振坤_20220420')

**Two special cases:**
+ A empty set is a convex set.
+ A single point set is a convex set.

## Basic Theories of LP
![](source/img/Basic%20theories%20of%20LP.png '图源来自：SDM223_第10周课件_王振坤_20220420')
**Theorem - The feasible region of a LP problem is a convex set**  
**证明**也很简单: 
> Every linear constraint will split the space in half. In each half space, it is a convex set. It is easy to proof that the intersection of convex sets is still a convex set.

**


## 什么是 凸函数Convex Function 和 凹函数Concave Funtion

![](source/img/Definition%20of%20Convex%20Function.png '图源来自：https://youtu.be/a_gRfwHUlhQ')

![](source/img/Definition%20of%20Concave%20Function.png '图源来自：https://youtu.be/a_gRfwHUlhQ')





