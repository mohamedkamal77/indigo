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



{% highlight html %}
This note **demonstrates** some of what [Markdown][some/link] is *capable of doing*.
{% endhighlight %}

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
  # output
    * survival status (class attribute)
---
## visualization & EDA
   we got 306 examples
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

##features
 1. #Age
   *integar
   *no misisng data
   *no zeros
   *49  unique values
   *mean = 52.46
   *sd = 12.37
   *min = 30
   * max = 12.37

---	 
 2. #Nodes
   * integar
   * no misisng data
   * 136 zeros - p_zeros= 44.44
   * 31 unique values
   * mean = 4.026
   * sd = 6.03
   * min = 0
   * max = 52
---
 3. #Year
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

##Preprocessing
 *corrilation matrix
![Markdowm Image][6]
 <figcaption class="caption">Visualization</figcaption>
####we notice that feature of year of operation has zero correlation with our output class and high P_value
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

##Models
 1. ###Logistic Regression
  * simple model
    ![Markdowm Image][8]
	<figcaption class="caption">Visualization</figcaption>
    1. accuarcy =
    2. sensitivity =
	3. specifity =  
	4. F =
---		 
   *Polynomial_featured model
    ![Markdowm Image][9]
	<figcaption class="caption">Visualization</figcaption>
    1. accuarcy =
    2. sensitivity =
    3. specifity = 
	4. F =
---		 
 2. ###Naive Bayes
    ![Markdowm Image][10]
    <figcaption class="caption">Visualization</figcaption>
    1. accuarcy =
    2. sensitivity =
	3. specifity = 
	4. F =
---		 
 3. ###Knn
    ![Markdowm Image][11]
	<figcaption class="caption">Visualization</figcaption>
	1. accuarcy =
    2. sensitivity =
	3. specifity = 
	4. F =
---		 
 4. ### Kernel SVM
    ![Markdowm Image][12]
    <figcaption class="caption">Visualization</figcaption>
	1. accuarcy =
    2. sensitivity =
	3. specifity = 
	4. F =
---		 
## summary

A horizontal rule is a line that goes across the middle of the page.
It's sometimes handy for breaking things up.


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
[12]: https://mohamedkamal77.github.io/assets/images/Kernel.jpg
