# **Readme**
>## **Deep Neural Pursuit**
> Name : Naresh Kumar Kaushal  
> Id : 170030027, Department : CSE, Term : Fourth Year  
> BTP advisor : Dr. Clint Pazhayidam George
***

>## Table of Contents
1. [Abstract](#abstract)
2. [Dataset](#dataset)
3. [Algorithm](#algorithm)
4. [References](#references)

>## Abstract 
<div style="text-align: justify">

Deep neural networks **(DNN)** have achieved break throughs in applications with large sample size. However, when facing high dimension, low sample size **(HDLSS)** data, such as the phenotype prediction problem using genetic data in bioinformatics, DNN suffers from overfitting and high-variance gradients. In this paper, we propose a DNN model tailored for the HDLSS data, **named Deep Neural Pursuit (DNP)**. DNP selects a subset of high dimensional features for the alleviation of overfitting and takes the average over multiple dropouts to calculate gradients with low variance. As the first DNN method applied on the HDLSS data, DNP enjoys the advantages of the high nonlinearity, the robustness to high dimensionality, the capability of learning from a small number of samples the stability in feature selection, and the end-to-end training. We will deploy this technique to classify breast, lung and brain cancer.

</div>

>## Dataset
<div style="text-align: justify">

**Still to be decided in next meeting**

</div>


>## Algorithm
<div style="text-align: justify">

**Input:** X ∈ R<sup>n×d</sup> , y ∈ R<sup>n</sup>, the maximum number of selected features *k*.  
**Initialize:** *S* = {bias}, C = *F* and **W**<sub>C</sub> = 0.  
**while** |S| ≤ k + 1 do  

1. Fix candidate weights **W**<sub>C</sub> = 0;  
2. Update weights of hidden layer and input **W**<sub>S</sub>;   
3. Dropout multiple times and average out **G**<sub>F<sub>c</sub></sub>;   
4. *j* = arg max<sub>c∈C</sub> ||**G**<sub>F<sub>c</sub></sub>||<sub>q</sub>;  
5. Update learning rates using Adagrad;  
6. Initialize **W**<sub>F<sub>j</sub></sub> with Xavier Initializer;  
7. *S* = *S* ∪ F<sub>j</sub> and *C* = *C* \ *F*<sub>j</sub>;      

**end while**  

</div>

>## References
<div style="text-align: justify">

1. Deep Neural Networks for High Dimension, Low Sample Size Data **Bo Liu, Ying Wei, Yu Zhang, Qiang Yang**  Hong Kong University of Science and Technology, Hong Kong. <https://www.ijcai.org/proceedings/2017/0318.pdf>

</div>

>## Further Queries

For further queries please contact <naresh.kaushal.17003@iitgoa.ac.in>  
**Happy coding !!**



