**202408060601**
**Status:** #flashcards 
**Tags: ** 
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

# Automatic Differentiation
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

### Key note
Yang Zhang Medium's post
Move some calculations outside of the recorded computational graph $z = x * y$ and $y=x*x$ but we want to focus on the *direct* influence of $x$ on $z$ rather than the influence conveyed via $y$
contrived
(i) attach gradients to those variables with respect to which we desire derivatives
(ii) record the computation of the target value 
(iii) execute backpropagation function 
(iv) access the resulting gradient
### Exercise
>[!question]- What x.grad.zero_() do ?

>[!question]- What happens if we forget to reset gradient ?

>[!question]- What is the mechanics in Pytorch that help to avoid wrong interpretation of non-scalar tensors taking gradient


### References

