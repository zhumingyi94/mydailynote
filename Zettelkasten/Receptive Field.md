**202408061133**
**Status:** #flashcards #ComputerVision #deeplearning 
**Tags: ** 
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

# Receptive Field
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

### Key note
![[Pasted image 20240806113651.png]]
Each layers of CNN focus on small section of the image, as we add more layer, this area expand => allow network capture broader pattern in details
*We can use specific formula to precisely calculate this area that we call* **<u>Theoretical Receptive Field</u>**
$$
r_{0} = \sum_{l=1}^L\left( (k_{l}-1)\prod_{i=1}^{l-1}s_{i} \right)
$$
>[!danger] this is not always fully exploited by the network

**<u>Effective Receptive Field</u>**

**Add gate:** routed gradient for both inputs, equally and unchanged
**Max gate:** Distributed the gradient (unchanged) to exactly one of its inputs (the input that had the highest value during the forward pass )
**Multiply gate:** Local gradients are inputs value

TRY TO INTERPRET THIS !
![[Pasted image 20240806152520.png]]
### Exercise


### References

