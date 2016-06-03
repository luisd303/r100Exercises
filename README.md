# 100 R Vector and Matrix Exercises

This is the R Version of [100 numpy exercises](http://www.loria.fr/%7Erougier/teaching/numpy.100/)

##### Install and load package Magrittr (1 Star)

```{r}
# install.packages("magrittr")
library(magrittr)
```

##### Print the R version (1 Star)

```{r}
print(version)
```

##### Create a null vector of size 10 (1 Star)

```{r}
rep(NA, 10) %>% print
```

##### How to get the examples of the add (+) function from the command line ? (1 Star)

```{r}
example(`+`)
```

##### Create a null vector of size 10 but the fifth value which is 1 (1 Star)

```{r}
z <- rep(NA, 10)
z[5] <- 1
print(z)
```

##### Create a vector with values ranging from 10 to 49 (1 Star)

```{r}
10:49 %>% print
```

##### Reverse a vector (first element becomes last) (1 Star)

```{r}
1:10 %>% rev %>% print
```

##### Create a 3x3 matrix with values ranging from 0 to 8 (1 Star)

```{r}
matrix(0:8, ncol = 3, nrow = 3) %>% print
```

##### Find indices of non-zero elements from [1,2,0,0,4,0] (1 Star)

```{r}
c(1,2,0,0,4,0) %>% as.logical %>% which %>% print
```

##### Create a 3x3 identity matrix (1 Star)

```{r}
diag(3) %>% print
```

##### Create a 3x3x3 array with random values (1 Star)

```{r}
runif(3^3) %>% array(c(3, 3, 3)) %>% print
```

##### Create a 10x10 array with random values and find the minimum and maximum values (1 Star)

```{r}
z <- array(runif(10^2), c(10,10))
min(z) %>% print
max(z) %>% print
```

##### Create a random vector of size 30 and find the mean value (1 Star)

```{r}
runif(30) %>% mean %>% print
```

##### Create a 2d array with 1 on the border and 0 inside (1 Star)

```{r}
z <- array(1, c(8, 10))
z[2:(nrow(z) - 1), 2:(ncol(z) - 1)] <- 0
print(z)
```

##### What is the result of the following expression ? (1 Star)

```{r}
0 * NaN
NA == NA
NA == NaN
Inf > NA
NaN - NaN
0.3 == 3 * 0.1
```

##### Create a 5x5 matrix with values 1,2,3,4 just below the diagonal (1 Star)

```{r}
z <- diag(0, ncol = 5, nrow = 5)
z[row(z) - 1 == col(z)] <- 1:4
print(z)
```

##### Create a 8x8 matrix and fill it with a checkerboard pattern (1 Star)

```{r}
odd <- rep(0:1, 4)
evn <- rep(1:0, 4)
z <- array(c(odd, evn), c(8, 8))
```
