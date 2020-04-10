# introtocars

---
title: "cars niyati"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
#Introduction to cars dataset. Data gives speed of cars and distances. Data recorded in 1920s. It has 50 observations and 2 variables.

```{r}
cars.data<-cars
dim(cars.data)
```

#We also see variables are speed and distance. both of them are numbers

```{r}
str(cars.data)
```

#Plotting
#Histogram
#Top speeds are 20km

```{r}
hist(cars.data$speed, 30, col="red")
```

```{r}
hist(cars.data$dist, 40, col="yellow")
```

#Boxplot
#Variation / which has most variation
#Speed has lower variation than distance

```{r}
boxplot(cars.data, main="Box Plot",
        xlab="variable", ylab="value", col="red", pch=19)
```


```{r}
plot(x=cars.data$speed, y=cars.data$dist, main="cars data scatter plot", xlab="speed", ylab = "dist", pch=19, col="orange")
```

#lin.mod <- lm(cars$dist~cars.data$speed)
#pr.lm <- predict(lin.mod)
#lines(pr.lm~cars$speed, col="blue", lwd=0.7)
