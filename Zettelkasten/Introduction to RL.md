**202408020120**
**Status:** #ReinforcementLearning
**Tags:** 

<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

# Introduction to RL
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

### Reinforcement Learning Framework

- Elements of RL:
	- Policy: a mapping from perceived states of the environment to actions to be taken when in those states
	- Reward signal: 
	- Value function: of a state is the total amount of reward an agent can expect to accumulate over the future, starting from that state.
	- Model: mimics the behavior of the environment, allows inferences to be made about how the environment will behave
MDP
Observation Space
Action Space 
Rewards & discounting 

$$
\begin{align*}
R(\tau) &= r_{t+1} + \gamma r_{t+2} + \gamma^2r_{t+3} + \gamma^3r_{t+4}+\dots \\
R(\tau) &= \sum_{k=0}^{\infty}\gamma^kr_{t+k+1}
\end{align*}
$$

### Type of tasks
*Episodic* task
*Continuing* task
![[Pasted image 20240801152516.png | center|675]]

### Exploration/Exploitation tradeoff
![[Pasted image 20240801154539.png]]

### 2 approach for solving RL problem
**Policy-Based Methods** - learn action to take 
**Value-Based Methods** - learn which state is more valuable 

$$
v_{\pi}(s) = \mathbb{E}_{\pi}[R_{t+1}+\gamma R_{t+2}+\gamma^2_{t+3}+\dots|S_{t} = s]
$$

## References