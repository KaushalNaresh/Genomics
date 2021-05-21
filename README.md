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

Deep neural networks **(DNN)** have achieved break throughs in applications with large sample size. However, when facing high dimension, low sample size **(HDLSS)** data, such as the phenotype prediction problem using genetic data in bioinformatics, DNN suffers from overfitting and high-variance gradients. In this paper, we propose a DNN model tailored for the HDLSS data, **named Deep Neural Pursuit (DNP)**. DNP selects a subset of high dimensional features to alleviate overfitting and takes the average over multiple dropouts to calculate gradients with low variance. As the first DNN method applied on the HDLSS data, DNP enjoys the advantages of the high nonlinearity, the robustness to high dimensionality, the capability of learning from a small number of samples the stability in feature selection, and the end-to-end training. I will deploy this technique to classify breast, lung, leukemia and Prostate cancer.

</div>

>## Dataset
<div style="text-align: justify">

We chose 3 biological datasets (Prostate-GE, ALLAML and Lung) provided on this [link](https://jundongl.github.io/scikit-feature/datasets.html) and one breast cancer dataset which was provided by professor. You can find all these datasets in data folder. All these datasets suffer from HDLSS. Few details of these data sets are - Breast(4 subtypes) 574 samples and 1519 features, Lung Cancer(5 subtypes) with 203 samples and 3312 features, Prostate Cancer(2 subtypes) with 102 samples and 5966 features, Leukemia Cancer(2 subtypes) with 72 samples and 7129 features. These datasets are already preprocessed and for better prediction we normalised (mean = 0, std = 1) gene expression data. Every dataset has 2 tables one for gene expression values and other for subtype information.
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
  
You can find the source code in src folder.

**end while**  

</div>

>## References
<div style="text-align: justify">

1. Deep Neural Networks for High Dimension, Low Sample Size Data **Bo Liu, Ying Wei, Yu Zhang, Qiang Yang**  Hong Kong University of Science and Technology, Hong Kong. [Research Paper](https://www.ijcai.org/proceedings/2017/0318.pdf)
2. Google Slides to understand DNP algorithm in a better way [Google Slides](https://docs.google.com/presentation/d/1TM9R9-ctBZwkCwkmvR_qXwbsOIOoTVuO7WbD0fMLGBU/edit?usp=sharing)
3. Google Slides for final presentation [Google Slides](https://docs.google.com/presentation/d/1Sg9wsu9srHGv6439LHxZjKM4oylqa92W6llFNRs-0Mw/edit?usp=sharing)

</div>

>## Further Queries

For further queries please contact <naresh.kaushal.17003@iitgoa.ac.in>  
**Happy coding !!**



