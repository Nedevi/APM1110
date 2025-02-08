---
title: "SEC 1 GROUP 8-COBARRUBIAS, I-FA2"
output: md_document
date: "2025-02-08"
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

##2. An experiment consists of tossing two fair coins. Use R to simulate this experiment 100 times and obtain the relative frequency of each possible outcome. Hence, estimate the probability of getting one head and one tail in any order.
```{r}
toss <- replicate(100, sample(c(1, 0), size = 2, replace = TRUE))
toss
```
####Results of the tosses
The experiment assigns heads as 1 and tails as 0.

```{r}
x <- sum((toss[1, ] == 1 & toss[2, ] == 0) | (toss[1, ] == 0 & toss[2, ] == 1))
x/100
```
####Experimental probability of 1 heads and 1 tails calculated from the simulated 100 tosses.
Out of the 100 tosses, 51% yielded a result of having exactly 1 heads and 1 tails in any order.

##3. An experiment consists of rolling a die. Use R to simulate this experiment 600 times and obtain the relative frequency of each possible outcome. Hence, estimate the probability of getting each of 1, 2, 3, 4, 5, and 6.
```{r}
dice <- replicate(600, sample(c(1, 2, 3, 4, 5, 6), size = 2, replace = TRUE))
dice
```
#### Results of the 600 dice rolls

```{r}
probresult_1 <- sum(dice[1,] == 1)/600
probresult_2 <- sum(dice[1,] == 2)/600
probresult_3 <- sum(dice[1,] == 3)/600
probresult_4 <- sum(dice[1,] == 4)/600
probresult_5 <- sum(dice[1,] == 5)/600
probresult_6 <- sum(dice[1,] == 6)/600

probresult_1
probresult_2
probresult_3
probresult_4
probresult_5
probresult_6
```
####Calculated experimental probability of all the possible outcomes
