**202410052249**
**Status:** #ReinforcementLearning  
**Tags:** 
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

# MDPs, Exact Solution Methods, Max-ent RL
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

### Key note
- Draw simple framework of RL 
- How to define MDP
- What is H
- Prove of the convergence of value iteration:
	- Cách chính tắc
	- Cách contraction
>[!question]- What is the definition of max-norm
>$||U||=max_{s}|U(s)|$

- Definition: An update operation is a $\gamma$-contraction in max-norm if and only if for all $U_{i}, V_{i}$
$$
||U_{{i+1}} - V_{i+1}|| \le \gamma||U_{i} - V_{i}||
$$
- Theorem: A contraction converges to a unique fixed point, no matter initialization
- Fact: the value iteration update is a $\gamma$-contraction in max-norm
- You can bound the error
- Different between Q-values and V

#### Policy Iteration
>[!question]- What is entropy
>Measure of uncertainty over random variable X
>Number of bits required to encode X (on average)
>$H(X) = \sum_{i}p(x_{i})\log_{2} \frac{1}{p(x_{i})}$

- How "soft" is softmax
- Hệ thống truyền thông Shannon là gì ?
- 
### Exercise


### References

