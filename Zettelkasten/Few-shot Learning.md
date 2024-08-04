**202408030049**
**Status:** #flashcards #ComputerVision 
**Tags:** [[reference notes/Computer Vision]]

<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

# Few-shot Learning

<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

### Key note
It's a **Machine Learning Framework** that enables a pre-trained model to generalize over new categories of data using only few labeled samples per class.
We do this by learning a similarity function using **large-scale dataset**
##### <font color="#0070c0">Core terminology</font>
**Support Set:** Data samples that we give model after training process and use this for inference
**k-way n-shot learning scheme**: The support set have **k-classes** and has **n-samples**
##### <font color="#0070c0">Training process</font>
- First, learn a similarity function from large-scale training dataset
- Then, apply similarity function for prediction by compare the **query** with every sample in **support set** (Find the sample with highest similarity score)
- We can use [[Siamese network]] to accomplish this task

### Exercise
>[!question]- What is Support Set
?
>Data samples that we give model after training process and use this for inference

>[!question]- What is k-way n-shot learning scheme
?
The support set have **k-classes** and has **n-samples**

>[!question]- Describe the training process of the few-shot learning
?
First, learn a similarity function from large-scale training dataset. Then, apply similarity function for prediction by compare the **query** with every sample in **support set** (Find the sample with highest similarity score)

### References
[Few-Shot Learning (1/3): Basic Concepts (youtube.com)](https://www.youtube.com/watch?v=hE7eGew4eeg)
