**202409130215**
**Status:** #LinearAlgebra  
**Tags:** [[Reference notes/Mathematics for machine learning]]
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

# Linear Algebra (MML, Ex)
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

### Exercise
2.1) We consider $(\mathbb{R} \backslash \{-1\}, \star)$, where 
$$
a \star b := ab + a + b, \qquad a,b \in \mathbb{R} \backslash \{ -1 \} 
$$
a. Show that $(\mathbb{R}\backslash \{ -1 \}, \star)$ is an Abelian group.
b. Solve
$$
3\star x\star x = 15
$$
in the Abelian group $(\mathbb{R} \backslash \{ -1 \}, \star)$
**Solve:**
a. 
*Closure:* $\forall a, b \in (\mathbb{R} \backslash \{ -1 \})$, we have
$$a \star b := ab + a + b = (a+1)(b+1) - 1$$
Because $(a+1), (b+1) \in \mathbb{R}\backslash \{ 0 \}$, thus $a \star b \in (\mathbb{R} \backslash \{ -1 \})$ 

*Associtivity:* Assume that we have $a, b, c \in \mathbb{R} \backslash \{ -1 \}$ then we have
$$
\begin{align*}
(a \star b) \star c &= ((a+1)(b+1) - 1) \star z = ((a+1)(b+1) - 1)z + (a+1)(b+1) - 1 + z \\
&= (a+1)(b+1)(z+1) - 1\\
\end{align*} \qquad(1)
$$
$$
\begin{align*}
a \star (b \star c) &= a \star ((b+1)(c+1) - 1) = a((b+1)(c+1) - 1) + a + (b+1)(c+1) - 1 \\
&= (a+1)(b+1)(c+1) - 1
\end{align*} \qquad(2)
$$
$(1) == (2) \implies q.e.d$

*Neutral element:* If $e = 0$ then we have $x \star e = xe + x + e = x$, same for $e \star x$
*Inverse element:* If $x \star y = e =0$ then we have 
$$
\begin{array}{rcl}  \\
\Leftrightarrow & (x + 1)(y + 1) - 1 &= 0 \\
\Leftrightarrow & y &= \frac{-x}{x+1} 
\end{array}
$$
*Commutative:* 
$$
\begin{align*}
x\star y = (x+1)(y+1) - 1 = (y+1)(x+1) - 1 = y\star x

\end{align*}
$$
Because the set $(\mathbb{R}\backslash\{ -1 \})$ and operation $\star$ has ***Closure***, ***Associativity***, ***Neutral element***, ***Inverse element*** and ***Commutative***, this this is an Abelian group

b. 
$$
\begin{align*}
3 \star x\star x &= 15 \\
\Leftrightarrow 3 \star(x\star x) &= 15 \\
\Leftrightarrow 3 \star (x(x+2)) &=15 \\
\Leftrightarrow 3x(x+2) + 3+x(x+2) &=15 \\
\Leftrightarrow 4x^2 + 8x -12 &= 0 \\
\Leftrightarrow x &= \begin{cases}
1 \\
-3
\end{cases}
\end{align*}
$$

2.2) Let $n$ in $\mathbb{N} \backslash \{ 0 \}$. Let $k, x$ be in $\mathbb{Z}$. We define the congruence class $\bar{k}$ of the integer $k$ as the set
$$
\begin{align*}
\bar{k}&=\{ k\in \mathbb{Z} | x - k = 0 \quad(\text{mod n}) \} \\
&= \{  k\in \mathbb{Z} | \exists a \in \mathbb{Z} : (x-k = n \cdot a)\}
\end{align*}
$$
We now define 

### References

