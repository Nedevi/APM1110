1.  A geospatial analysis system has four sensors supplying images. The
    percentage of images supplied by each sensor and the percentage of
    images relevant to a query are shown in the following table:

<!-- -->

    sensor_data <- data.frame(
      Sensor = c(1, 2, 3, 4),
      Percentage_Images_Supplied = c(15, 20, 25, 40),
      Percentage_Relevant_Images = c(50, 60, 80, 85)
    )
    sensor_data

    ##   Sensor Percentage_Images_Supplied Percentage_Relevant_Images
    ## 1      1                         15                         50
    ## 2      2                         20                         60
    ## 3      3                         25                         80
    ## 4      4                         40                         85

What is the overall percentage of relevant images?

    relevant_img_percentage <- sum(sensor_data$Percentage_Relevant_Images * sensor_data$Percentage_Images_Supplied)/sum(sensor_data$Percentage_Images_Supplied)
    relevant_img_percentage

    ## [1] 73.5

1.  A fair coin is tossed twice. Let E\_1 be the event that both tosses
    have the same outcome, that is, E\_1 = {HH, TT}

Let E\_2 be the event that the first toss is a head, that is, E\_2 =
{HH, HT}

Let E\_3 be the event that the second toss is a head, that is, E\_3 =
{TH, HH}

Show that E\_1, E\_2, and E\_3 are pairwise independent but not mutually
independent.

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

    ## E_1, E_2 Pairwise independent =  TRUE

    cat("E_2, E_3 Pairwise independent = ", pair_ind_check(E_2, E_3),"\n")

    ## E_2, E_3 Pairwise independent =  TRUE

    cat("E_1, E_3 Pairwise independent = ", pair_ind_check(E_1, E_3),"\n")

    ## E_1, E_3 Pairwise independent =  TRUE

    mutual_ind <- prob(intersect(intersect(E_1, E_2), E_3)) == prob(E_1) * prob(E_2) * prob(E_3)

    cat("E_1, E_2, E_3 Mutually independent = ", mutual_ind)

    ## E_1, E_2, E_3 Mutually independent =  FALSE
