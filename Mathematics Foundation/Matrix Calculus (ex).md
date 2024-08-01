# Matrix Calculus (ex)

>[!question]- Write *gradient* of a function of 2 variables
$\nabla f(x, y) = \begin{bmatrix}
\frac{ \partial f(x, y) }{ \partial x }, \frac{ \partial f(x, y) }{ \partial y } 
\end{bmatrix}
$


$\nabla f(x, y) = ?$

>[!question]- Write the Jacobian
$
J_{x} = \frac{ \partial \mathbf{y} }{ \partial \mathbf{x} } = \begin{bmatrix}
\frac{ \partial f_{1}(x) }{ \partial x_{1} }  & \frac{ \partial f_{1}(x) }{ \partial x_{2} }   & \dots  & \frac{ \partial f_{1}(x) }{ \partial x_{n} } \\
\frac{ \partial f_{2}(x) }{ \partial x_{1} }  & \frac{ \partial f_{2}(x) }{ \partial x_{2} }   & \dots  & \frac{ \partial f_{2}(x) }{ \partial x_{n} } \\
  \dots   & \dots  & \dots & \dots
\\
\frac{ \partial f_{m}(x) }{ \partial x_{1} }  & \frac{ \partial f_{m}(x) }{ \partial x_{2} }  &  \dots  & \frac{ \partial f_{m}(x) }{ \partial x_{n} }
\end{bmatrix} 
$

$J_{x} = ?$
>[!question]- The element-wise operations on vector $\mathbf{w}$ and $\mathbf{x}$ using $\bigcirc$
$\frac{ \partial (\mathbf{w+x}) }{ \partial \mathbf{w} } =I$
$\frac{ \partial (\mathbf{w-x}) }{ \partial \mathbf{w} } = I$
$\frac{ \partial (\mathbf{w \bigotimes x}) }{ \partial \mathbf{w} } = diag(\mathbf{x})$
$\frac{ \partial (\mathbf{w \oslash x}) }{ \partial \mathbf{w} } = diag\left( \dots\, \frac{1}{x_{i}} \dots\right)$

$\frac{ \partial (\mathbf{w+x}) }{ \partial \mathbf{w} } = ?$
$\frac{ \partial (\mathbf{w-x}) }{ \partial \mathbf{w} } = ?$
$\frac{ \partial (\mathbf{w \bigotimes x}) }{ \partial \mathbf{w} } = ?$
$\frac{ \partial (\mathbf{w \oslash x}) }{ \partial \mathbf{w} } = ?$

>[!question]- Write the scalar expansion
>$\frac{ \partial}{ \partial \mathbf{x} }(\mathbf{x} + z) = I$
>$\frac{ \partial}{ \partial z }(\mathbf{x} + z) = \vec{1}$
>$\frac{ \partial  }{ \partial \mathbf{x} }(\mathbf{x}z) = Iz$
>$\frac{ \partial  }{ \partial z}(\mathbf{x}z) =\mathbf{x}$

$\frac{ \partial}{ \partial \mathbf{x} }(\mathbf{x} + z) = ?$
$\frac{ \partial}{ \partial z }(\mathbf{x} + z) = ?$
$\frac{ \partial  }{ \partial \mathbf{x} }(\mathbf{x}z) = ?$
$\frac{ \partial  }{ \partial z}(\mathbf{x}z) = ?$

>[!question]- Write the chain rules
>**Single-variable rule: **$\frac{dy}{dx} = \frac{dy}{du} \frac{du}{dx}$
>**Single-variable total-derivative rule:** $\frac{ \partial f(u_{1}, u_{2}\dots,u_{n}) }{ \partial x } = \frac{ \partial y }{ \partial \mathbf{u} } \frac{ \partial \mathbf{u} }{ \partial x }$
>**Vector rule: ** $\frac{ \partial \mathbf{y} }{ \partial \mathbf{x} } = \frac{ \partial \mathbf{y} }{ \partial \mathbf{g} } \frac{ \partial \mathbf{g} }{ \partial \mathbf{x} }$

**Single-variable rule: **:
**Single-variable total-derivative rule:**
**Vector rule: **

>[!question]- Calculate the gradient of neuron activation $activation(\mathbf{x}) = max(0, \mathbf{w \cdot x} + b)$
> $\frac{ \partial activation(x) }{ \partial \mathbf{w} } =  \begin{equation}
\begin{cases}
\vec0^T \qquad \mathbf{w} \cdot \mathbf{x} + b \le 0 \\
\mathbf{x}^T \qquad \mathbf{w} \cdot \mathbf{x} + b > 0 
\end{cases}
\end{equation}$
> $\frac{ \partial activation(\mathbf{x}) }{ \partial b } = \begin{equation}
\begin{cases}
0 \qquad \mathbf{w} \cdot \mathbf{x} + b \le 0 \\
1 \qquad \mathbf{w} \cdot \mathbf{x} + b > 0 
\end{cases}
\end{equation}$

$\frac{ \partial activation(x) }{ \partial \mathbf{w} } = ?$
$\frac{ \partial activation(\mathbf{x}) }{ \partial b } = ?$


>[!question]- Calculate the gradient of the neural network loss function
> $C(\mathbf{w}, b, X, \mathbf{y}) =\frac{1}{N}\sum_{i=1}^N(y_{i} - max(0, \mathbf{w \cdot \mathbf{x}_{i}+b}))^2$
> $\frac{ \partial C }{ \partial \mathbf{w} } = \begin{equation}
\begin{cases}
\vec{0}^T & \mathbf{w \cdot x_{i} +b \le 0} \\ \\
\frac{2}{N}\sum_{i=1}^{N} (\mathbf{w}\cdot x_{i}+b-y_{i})\mathbf{x}_{i}^T  &  \mathbf{w} \cdot x_{i} + b > 0
\end{cases}
\end{equation}$
>$e_{i} = \mathbf{w} \cdot x_{i} +b -y_{i} \implies \frac{ \partial C }{ \partial \mathbf{w} } = \frac{2}{N}\sum_{i=1}^{N}e_{i}\mathbf{x}_{i}^T$
> $\frac{ \partial C }{ \partial b } = \begin{equation}
\begin{cases}
0 & \mathbf{w \cdot x_{i} +b \le 0} \\ \\
\frac{2}{N}\sum_{i=1}^{N}e_i&  \mathbf{w} \cdot x_{i} + b > 0
\end{cases}
\end{equation}$

$C(\mathbf{w}, b, X, \mathbf{y}) =\frac{1}{N}\sum_{i=1}^N(y_{i} - max(0, \mathbf{w \cdot \mathbf{x}_{i}+b}))^2= ?$


>[!question]- Calculate this $\frac{ \partial  }{ \partial x }(A \cdot ((A \cdot x + b) \odot (A \cdot x + b)) + b) = 2A \,diag(Ax+b)\,A$

 