# Matrix calculus

##### Generalization of Jacobian
>[!error] We consider numerator layout, in many research paper, scientist use denumerator layout (It's just the transpose of numerator layout)
- The shape of Jacobian matrix are in the form below (Just remember this table!)
![[Pasted image 20240707173504.png | center|600]]


##### Derivatives of vector element-wise binary operator
- We can often reduce the Jacobian matrix into this form
$$
\mathbf{J}_{\mathbf{w}} = \frac{ \partial \mathbf{y} }{ \partial \mathbf{w} } = \begin{bmatrix}
\frac{ \partial}{ \partial w_{1}}(f_{1}(w_{1})\, \bigcirc \, g_{1}(x_{1}))  &  &  &  &   \Huge{0} \\
 &  \frac{ \partial }{ \partial w_{2} } (f_{2}(w_{2})\, \bigcirc \, g_{2}(x_{2}))  \\
\Huge{0}  &  &  &  &  \frac{ \partial}{ \partial w_{n} } (f_{n}(w_{n}) \, \bigcirc \, g_{n}(x_{n}))
\end{bmatrix}  
$$

</br>
</br>

$$
\mathbf{J}_{\mathbf{x}} = \frac{ \partial \mathbf{y} }{ \partial \mathbf{x} } = \begin{bmatrix}
\frac{ \partial}{ \partial x_{1}}(f_{1}(w_{1})\, \bigcirc \, g_{1}(x_{1}))  &  &  &  &   \Huge{0} \\
 &  \frac{ \partial }{ \partial x_{2} } (f_{2}(w_{2})\, \bigcirc \, g_{2}(x_{2}))  \\
\Huge{0}  &  &  &  &  \frac{ \partial}{ \partial x_{n} } (f_{n}(w_{n}) \, \bigcirc \, g_{n}(x_{n}))
\end{bmatrix}  
$$
- More succintly, we can write:
$$
\frac{ \partial \mathbf{y} }{ \partial \mathbf{x} } = diag(
\frac{ \partial}{ \partial x_{1}}(f_{1}(w_{1})\, \bigcirc \, g_{1}(x_{1})) \,,\
\frac{ \partial }{ \partial x_{2} } (f_{2}(w_{2})\, \bigcirc \, g_{2}(x_{2})), \, \dots ,\
\frac{ \partial}{ \partial x_{n} } (f_{n}(w_{n}) \, \bigcirc \, g_{n}(x_{n}))
)
$$

##### Derivatives involving scalar expression 
- Threre are 4 formulas that you should try to prove
	- $\frac{ \partial  }{ \partial \mathbf{x} } (\mathbf{x}+z) = diag(\vec{1}) = I$
	- $\frac{ \partial  }{ \partial z } (\mathbf{x} + z) = \vec{1}$
	- $\frac{ \partial  }{ \partial \mathbf{x} }(\mathbf{x}z)=Iz$
	- $\frac{ \partial }{ \partial z }(\mathbf{x}z) =\mathbf{x}$

##### Vector sum reduction 
Let $y=\text{sum}(\mathbf{f(x)}) = \sum_{i=1}^nf_{i}\mathbf{(x)}$. Notice we were careful here to leave the parameter as a vector $\mathbf{x}$ because each function $f_{i}$ could use all values in the vector, not just $x_{i}$. The sum is over the **results** of the function and not the parameter. The gradient (1 x $n$ Jacobian) of vector summation is
$$
\begin{flalign*}
\frac{ \partial y }{ \partial \mathbf{x} } &= \begin{bmatrix}
\frac{ \partial y }{ \partial x_{1} } , \frac{ \partial y }{ \partial x_{2}}, \dots, \frac{ \partial y }{ \partial x_{n} }  
\end{bmatrix} && \\ &= 
\begin{bmatrix}
\frac{ \partial  }{ \partial x_{1} }\sum_{i}f_{i}(\mathbf{x}) , \frac{ \partial  }{ \partial x_{2}}\sum_{i}f_{i}(\mathbf{x}), \dots, \frac{ \partial  }{ \partial x_{n} }\sum_{i}f_{i}(\mathbf{x})  
\end{bmatrix}&& \\ &=
\begin{bmatrix}
\sum_{i} \frac{ \partial f_{i}(\mathbf{x}) }{ \partial x_{1} } , \sum_{i} \frac{ \partial f_{i}(\mathbf{x}) }{ \partial x_{2} }, \, \dots, \sum_{i} \frac{ \partial f_{i}(\mathbf{x}) }{ \partial x_{n} }  
\end{bmatrix}
\end{flalign*}
$$

Because $\frac{ \partial }{ \partial x_{j} }x_{i} = 0$ for $j \neq i$, we can simplify to:
$$
\nabla y = \begin{bmatrix}
\frac{ \partial x_{1} }{ \partial x_{1} }, \frac{ \partial x_{2} }{ \partial x_{2} }, \, \dots, \frac{ \partial x_{n} }{ \partial x_{n} } \end{bmatrix} = \begin{bmatrix}
1, 1, \, \dots,1   
\end{bmatrix} = \vec{1}^T
$$

##### Chain rules
- **Single-variable rule:** $\frac{df}{dx} = \frac{df}{du} \frac{du}{dx}$
- **Single-variable total-derivative rule:** $\frac{ \partial f(u_{1}, \dots,u_{n}) }{ \partial x } = \frac{ \partial f }{ \partial \mathbf{u} } \frac{ \partial \mathbf{u} }{ \partial x }$
- **Vector rule:** $\frac{ \partial  }{ \partial \mathbf{x}}\mathbf{f(g(x)) = \frac{ \partial \mathbf{f} }{ \partial \mathbf{g} } \frac{ \partial \mathbf{g} }{ \partial \mathbf{x} }}$

##### Exercise
- Go to [[Matrix Calculus (ex)]] 
