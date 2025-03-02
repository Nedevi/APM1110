---
title: "SEC 1 GROUP 8-COBARRUBIAS, I-FA4"
output: md_document
date: "2025-02-28"
---
5. A geospatial analysis system has four sensors supplying images. The percentage of images supplied by each sensor and the percentage of images relevant to a query are shown in the following table:
```{r}
sensor_data <- data.frame(
  Sensor = c(1, 2, 3, 4),
  Percentage_Images_Supplied = c(15, 20, 25, 40),
  Percentage_Relevant_Images = c(50, 60, 80, 85)
)
sensor_data
```
What is the overall percentage of relevant images?

```{r}
relevant_img_percentage <- sum(sensor_data$Percentage_Relevant_Images * sensor_data$Percentage_Images_Supplied)/sum(sensor_data$Percentage_Images_Supplied)
relevant_img_percentage
```
6. A fair coin is tossed twice.
Let E_1 be the event that both tosses have the same outcome, that is,
E_1 = {HH, TT}

Let  E_2 be the event that the first toss is a head, that is,
E_2 = {HH, HT}


Let E_3 be the event that the second toss is a head, that is,
E_3 = {TH, HH}

Show that E_1, E_2, and E_3 are pairwise independent but not mutually independent.
```{r}

S <- c("HH", "HT", "TH", "TT")

E_1 <- c("HH", "TT")
E_2 <- c("HH", "HT")
E_3 <- c("HH", "TH")

prob <- function(event) {
  return(length(event) / length(S))
}
pair_ind_check <- function(event1, event2){
  intersection <- prob(intersect(event1, event2))
  check <- intersection == prob(event1) * prob(event2)
  return(check)
}

cat("E_1, E_2 Pairwise independent = ", pair_ind_check(E_1, E_2),"\n")
cat("E_2, E_3 Pairwise independent = ", pair_ind_check(E_2, E_3),"\n")
cat("E_1, E_3 Pairwise independent = ", pair_ind_check(E_1, E_3),"\n")

mutual_ind <- prob(intersect(intersect(E_1, E_2), E_3)) == prob(E_1) * prob(E_2) * prob(E_3)

cat("E_1, E_2, E_3 Mutually independent = ", mutual_ind)


```