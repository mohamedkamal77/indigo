---
title: "Breast Cancer Classification with ML"
layout: post
date: 2019-12-3 15:44
image: /assets/images/markdown.jpg
headerImage: false
tag:
- markdown
- elements
star: true
category: blog
author: johndoe
description: Markdown summary with different options
---

## Introduction

I studied a biostatistics course within my third year in the college,
 including the **probabilitiy** concept and I have to apply what I studied;
 so we had to choose a topic and represent a **Machine Learning** model.
 That was my first experience with ML, I and my team have to read about 
 different ML algorithms to apply it on our set of data.
 I found later that ML track is very interisting I enjoyed this experience alot.


---

## Purpose

For our society, breast cancer became a severe problem causing many deaths so  expecting the survival status of patients who will undertake breast cancer surgery is highly vital,
 as it speciﬁes whether conducting a surgery is the best solution for the patient or not. 
 To achieve an acurate prediction , we have to do alot of work in our data to represent the best model,
 We would like to explain the various data analysis operation that we would do on this data set and how to conclude or predict 
 survival status of patients who undergone this surgery.

---
## Data 
### features 
  * ***Age*** of patient at time of operation (numerical)
  * ***year*** of operation (year-1900, numerical)
  * number of positive auxiliary ***nodes*** detected (numerical)
  * survival status ***class*** attribute
---
## visualization & EDA
  ![Markdowm Image][3]
  <figcaption class="caption">Visualization</figcaption>
  ![Markdowm Image][1]
  <figcaption class="caption">Visualization</figcaption>
  ![Markdowm Image][2]
  <figcaption class="caption">Visualization</figcaption>
  ![Markdowm Image][4]
  <figcaption class="caption">Visualization</figcaption>
  ![Markdowm Image][5]
  <figcaption class="caption">Visualization</figcaption> 
---

## Features

### Age
   * integar
   * no misisng data
   * no zeros
   * 49  unique values
   * mean = 52.46
   * sd = 12.37
   * min = 30
   * max = 12.37

---	 
### Nodes
   * integar
   * no misisng data
   * 136 zeros - p_zeros= 44.44
   * 31 unique values
   * mean = 4.026
   * sd = 6.03
   * min = 0
   * max = 52
---
### Year
   * integar
   * no misisng data
   * no zeros
   * 12 unique values
   * mean = 62.85
   * sd = 3.738
   * min = 58
   * max = 69
---	 
### output class
   * 2 classes
   * 0 represent who survived 5 years after the operation (225 example)
   * 1 represent who died in 5 years after the operation (81 examples)
   * unbalanced
	 
	 
---

## Preprocessing
 *corrilation matrix
![Markdowm Image][6]
 <figcaption class="caption">Visualization</figcaption>
 we notice that feature of year of operation has zero correlation with our output class and high P_value
 *Bias Vs Variance
![Markdowm Image][7]
  <figcaption class="caption">Visualization</figcaption>
 *High bias no normalization
 *No imputation ; no missing data
 *feature scaling : We are going to use standarization  
 *feature selecting : year feature does not have high impact so we will not use it

---
## Methodology
we are going to use 5 models:
1. Logistic regression
2. Knn
3. Naive Bayes
4. Decision tree
5. Kernal SVM

---

## Models
 1.  ### Logistic Regression
  * simple model
    ![Markdowm Image][8]
	<figcaption class="caption">Visualization</figcaption>
    1. accuarcy = 0.748
    2. sensitivity = 0.234
	3. specifity = 0.6
	4. f = 0.336
	
---		 
   *Polynomial_featured model
    ![Markdowm Image][9]
	<figcaption class="caption">Visualization</figcaption>
    1. accuarcy = 0.758
    2. sensitivity = 0.26
    3. specifity = 0.63
	4. f = 0.3672
	
	After many analysis and processing, we found that our data is biased. We found that logistics regression is the most method that suffered from this problem. As we showed above, we found if we added polynomial features, the accuracy would be increased.  
---		 
 2. ### Naive Bayes
    ![Markdowm Image][10]
    <figcaption class="caption">Visualization</figcaption>
    1. accuarcy = 0.745
    2. sensitivity = 0.1986
	3. specifity = 0.576
	4. f = 0.295
	
	It employs a very simple hypothesis function. It suffers from high bias, resulting from inaccuracies in its hypothesis class, because its hypothesis function is so simple. It cannot accurately represent many complex situations.
---		 
 3. ### Knn
    #### K = 9
    ![Markdowm Image][11]
	<figcaption class="caption">Visualization</figcaption>
	1. accuarcy = 0.795
    2. sensitivity = 0.33
	3. specifity = 0.8
	4. f =0.47
 
	We found it is the best model. As it's the highest in sensitivity and accuracy.
---		 
 4. ### Kernel SVM
    ![Markdowm Image][12]
    <figcaption class="caption">Visualization</figcaption>
	1. accuarcy = 0.75
    2. sensitivity = 0.26
	3. specifity = .53
	4. f = 0.35
	
---
 5. ### Decision Tree
    ![Markdowm Image][13]
    1. accuarcy = 0.754
    2. sensitivity = 0.368
	3. specifity = .554
	4. f = 0.442
   
---		 
## summary
 
	After a lot of analysis and processing, We discovered that the feature "nodes" is the most significant one. And the feature "year of operation" has no observable effect. We were facing a challenge which was a case of life or death. Cataloguing of Haberman’s survival information was beneﬁcial to realize the patients’ survival probability after a breast cancer surgery. We depended on a collected dataset from a standard benchmark UCI machine learning repository. We were trying to get through data imputation, categorical datatype, data processing and exploratory data analysis using different methodologies to detect the performance evaluation of classiﬁers and to compare between them to find the most suitable one.


---





[1]: https://mohamedkamal77.github.io/assets/images/EDA_FREQ.png
[2]: https://mohamedkamal77.github.io/assets/images/EDA_OUT_freq.png
[3]: https://mohamedkamal77.github.io/assets/images/vis.png
[4]: https://mohamedkamal77.github.io/assets/images/sunflower.png
[5]: https://mohamedkamal77.github.io/assets/images/boxplot.png
[6]: https://mohamedkamal77.github.io/assets/images/Bias_Vs_Variance.jpg
[7]: https://mohamedkamal77.github.io/assets/images/bias_vs_variance.png
[8]: https://mohamedkamal77.github.io/assets/images/simple_Logistic.jpg
[9]: https://mohamedkamal77.github.io/assets/images/FINAL_LOGISTIC.jpg
[10]: https://mohamedkamal77.github.io/assets/images/NB.jpg
[11]: https://mohamedkamal77.github.io/assets/images/KNN.jpg
[12]: https://mohamedkamal77.github.io/assets/images/KERNEL.jpg
[13]: https://mohamedkamal77.github.io/assets/images/Decision_Tree.jpg
