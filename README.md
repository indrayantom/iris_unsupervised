# :star2:Iris Dataset : Unsupervised Learning:star2:

This work contains Unsupervised Learning of Iris dataset, which is carried out by using PCA and Kmeans and done in R (Rstudio). 

![ide](https://img.shields.io/badge/RStudio-75AADB?style=for-the-badge&logo=RStudio&logoColor=white)
![kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)

Just in case you didn't know. The codes are contained in the .Rmd (Rmarkdown) file, whereas the results and codes are neatly combined in the .html file (knitted version of Rmarkdown). Feel free to download and open it [here](https://indrayantom.github.io/iris_unsupervised/)😃😉.

## Objectives
The data is about clustering the species of samples within the Iris dataset, based on Sepal length, Sepal width, Petal length, and Petal width. The result then will be compared to the actual species labels which have been deleted before. To determine the best number of clusters, The elbow method (Inertia) and Silhouette method are used.

## Libraries
This work was mainly done using tidyverse environment and glmnet to build the ML model. However, i also used another libraries to make plots and do certain calculations such as:

- [tidyverse](https://www.tidyverse.org/)
- [factoextra](https://cran.r-project.org/web/packages/factoextra/index.html)
- [patchwork](https://cran.r-project.org/web/packages/patchwork/index.html)

## Result preview
To determine the best number of clusters, the Total Within Sum of Square of each amount cluster iteration must be calculated, and the result is shown as follow:
![numclusters](https://user-images.githubusercontent.com/92590596/156587456-817640ac-2de1-40fe-9373-d4d85ad35f10.jpg)
The best number of cluster is usually found using elbow method, a method to find a point where  sum squares start decreasing slowly in a linear fashion (many literatures/sources say this, e.g https://www.geeksforgeeks.org/elbow-method-for-optimal-value-of-k-in-kmeans/). Based on this characteristic, it is concluded that the optimal number of clusters for this dataset is 3.

From the Petal.Length vs Petal.Width plot, one can see that the model is able to perfectly identify the setosa species among all observations. Unfortunately, when attempting to identify the versicolor and virginica species, the model begins to make 'mistakes'. This errors may comes from the fact that there are several Virginica and versicolor samples with quite similar characteristics to each other.
![cluster3](https://user-images.githubusercontent.com/92590596/156587499-c6612980-160f-429d-b50f-c24d818ff77c.jpg)

