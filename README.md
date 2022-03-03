# :star2:Iris Dataset : Unsupervised Learning:star2:

This work contains Unsupervised Learning of Iris dataset, which is carried out by using PCA and Kmeans and done in R (Rstudio). 

![ide](https://img.shields.io/badge/RStudio-75AADB?style=for-the-badge&logo=RStudio&logoColor=white)
![kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)

Just in case you didn't know. The codes are contained in the .Rmd (Rmarkdown) file, whereas the results and codes are neatly combined in the .html file (knitted version of Rmarkdown). Feel free to download and open it [here](https://indrayantom.github.io/BostonHousingPrices_RegularizedRegression/)😃😉.

## Objectives
The data is about clustering the species of samples within the Iris dataset, based on Sepal length, Sepal width, Petal length, and Petal width. The result then will be compared to the actual species labels which have been deleted before. To determine the best number of clusters, The elbow method (Inertia) and Silhouette method are used.

## Libraries
This work was mainly done using tidyverse environment and glmnet to build the ML model. However, i also used another libraries to make plots and do certain calculations such as:

- [tidyverse](https://www.tidyverse.org/)
- [factoextra](https://cran.r-project.org/web/packages/factoextra/index.html)
- [patchwork](https://cran.r-project.org/web/packages/patchwork/index.html)

## Result preview
This data has 506 rows, and that number of samples is actually considered small, making Regularization is a good fit. In this work, it is found that Ridge regression performs better than Lasso and ordinary Linear Regression, with hyperparameter lambda is set to be 0.01 . Consecutively, the RMSE on the validation and test dataset are 4.346 and 6.82, with MAPE for the test dataset equals 17% approximately.
![preview](https://user-images.githubusercontent.com/92590596/156525572-1a979e4e-345f-458a-acd5-becafa5fd656.jpg)
Those metrics show that the model's performance is quite decent even though no feature engineering was done. That step however, is included in the future works section along with better outliers treatment, proposed to improve the accuracy of the model's prediction. By Residual plot figure, it is evident that except for extreme maximum predicted values (upper outlier), the residual plot already fits some of classic linear regression assumptions, such as linearity, homoskesdascity, and no autocorrelation. Furthermore, with VIF calculation and Q-Q plot of Standardized Residual, it is also found that the result also fits No multicollinearity and normality assumption.

## References
Regularization is a method in which a penalty called lambda is added in the Loss Function in order to introduce a bias thus overfitting will not happen. The method also can be divided into 2 methods, Ridge (quadratic lambda) and Lasso (absolute lambda). Meanwhile Lasso method is able to reduce the coefficients of certain variables to be completely zero, the Ridge regression can't. To grasp more comprehensive explanation about this topic, I would recommend some great youtube videos made by StatQuest. Here is the link:

- https://www.youtube.com/watch?v=Q81RR3yKn30&t=458s
- https://www.youtube.com/watch?v=NGf0voTMlcs

