Answer Exercises 7.1 items 2 and 7.

1.  A binary communication channel carries data as one of two sets of
    signals denoted by 0 and 1. Owing to noise, a transmitted 0 is
    sometimes received as a 1, and a transmitted 1 is sometimes received
    as a 0. For a given channel, it can be assumed that a transmitted 0
    is correctly received with probability 0.95, and a transmitted 1 is
    correctly received with probability 0.75. Also, 70% of all messages
    are transmitted as a 0. If a signal is sent, determine the
    probability that:

<!-- -->

    P_0 <- 0.7
    P_1 <- 0.3
    err0 <- 0.05
    err1 <- 0.25

1.  a 1 was received;

<!-- -->

    prob1 <- (P_0*err0)+(P_1*(1-err1)) 
    prob1

    ## [1] 0.26

1.  a 1 was transmitted given than a 1 was received.

<!-- -->

    trans1 <- (1-err1)*(P_1)/prob1
    trans1

    ## [1] 0.8653846

1.  There are three employees working at an IT company: Jane, Amy, and
    Ava, doing 10%, 30%, and 60% of the programming, respectively. 8% of
    Jane’s work, 5% of Amy’s work, and just 1% of Ava‘s work is in
    error. What is the overall percentage of error? If a program is
    found with an error, who is the most likely person to have written
    it?

<!-- -->

    jane <- 0.10
    amy <- 0.30
    ava <- 0.60
    jane_err <- 0.08
    amy_err <- 0.05
    ava_err <- 0.01

Total Percent Error:

    TPE <- (jane*jane_err) + (amy*amy_err) + (ava*ava_err)
    TPE

    ## [1] 0.029

    prob_jane_err <- (jane*jane_err)/TPE
    prob_jane_err

    ## [1] 0.2758621

    prob_amy_err <- (amy*amy_err)/TPE
    prob_amy_err

    ## [1] 0.5172414

    prob_ava_err <- (ava*ava_err)/TPE
    prob_ava_err

    ## [1] 0.2068966

If an error occurs, it most likely came from Amy’s work at 0.5172
probability.
