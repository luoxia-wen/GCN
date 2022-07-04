# 图的基本知识



## 1.图（Graph）

​	图用G=(V, E)表示，V中元素为顶点（vertex），E中元素为边（edge）。图中边为无序对时为无向图，为有序对时为有向图。以下为一个无向图的例子。

![img](https://img-blog.csdnimg.cn/20200307173059947.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2x1emFpamlhb3hpYTA2MTg=,size_16,color_FFFFFF,t_70#pic_center)



## 2.邻居（Neighborhood）

​	顶点$V_i$的邻居
$$
\{v_j \in V | v_iv_j \in E\}
$$
​	无向图中，如果顶点$v_i$是$v_j$的邻居，那么反过来也一样。



## 3.度矩阵（Degree）

​	度矩阵是对角阵，对角上的元素为各个顶点的度。==顶点vi的度表示和该顶点相关联的边的数量。==

​	无向图中顶点$v_i$的度$d(v_i)=N(i)$。
$$
\bigtriangleup(G)= \left(
	\begin{matrix}
	d(v_1) & 0 & \dots & 0 \\
	0 & d(v_2) & \dots & 0 \\
	\vdots & \vdots & \ddots & \vdots \\
	0 & 0 & \dots & d(v_n)
	\end{matrix}
\right).
$$
​	有向图中，顶点vi的度分为顶点vi的出度和入度，即从顶点vi出去的有向边的数量和进入顶点vi的有向边的数量。



## 4.邻接矩阵（Adjacency）

​	邻接矩阵表示顶点间关系，是n阶方阵（n为顶点数量）。

​	邻接矩阵分为有向图邻接矩阵和无向图邻接矩阵。无向图邻接矩阵是对称矩阵，而有向图的邻接矩阵不一定对称。
$$
[\mathbf A(G)]_{ij} = \begin{cases}
1 & if v_iv_j \in E,\\
0 & otherwise.
\end{cases}
$$
​	==对于有向图，$v_iv_j$是有方向的，即$v_i -> v_j$==

​	

## 5.例子

​	对于1中的Figure.
$$
\bigtriangleup(G) = \left(
\begin{matrix}
1 & 0 & 0 & 0 & 0 \\
0 & 3 & 0 & 0 & 0 \\
0 & 0 & 3 & 0 & 0 \\
0 & 0 & 0 & 2 & 0 \\
0 & 0 & 0 & 0 & 3
\end{matrix}
\right) \\

\mathbf{A}(G) = \left( 
\begin{matrix}
0 & 1 & 0 & 0 & 0 \\
1 & 0 & 1 & 0 & 1 \\
0 & 1 & 0 & 1 & 1 \\
0 & 0 & 1 & 0 & 1 \\
0 & 1 & 1 & 1 & 0
\end{matrix}
\right)
$$
