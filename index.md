## Chi Lu

I am a junior undergradute majoring in Econometrics at the University of Illinois at Champaign and Urbana, and I will apply for the master school after the graduation. I want to contribute in the area of finance in the future. 
![689_quadruple-grand-champion-apollo-peace-coon-loretta](https://user-images.githubusercontent.com/35546324/75815377-ecd35700-5d58-11ea-836a-e76166baa040.jpg)

[Resume](https://github.com/chilu981021/chilu981021.github.io/files/4283574/Resume.docx.pdf)

[Linked](https://www.linkedin.com/in/chi-lu-b434721a3/).

[Github Profile](https://chilu981021.github.io/).


## Blog

This semester, I am taking the courses focusing on the areas of Public Sector(Public Finance), Industrial Comp and Monopoly, International Trading. Please feel free to discuss any of these topics with me. 

So far, I have learnt the basic R code through Stat385 including: data type&structure, basic plotting skills, and using github page or RMarkdown to create a personal page. 

##Homework3 Excercise one R code: 
(a)

specific_sum_vec <- function(m,pos){
  my_sum <- sum(m[1:nrow(m),pos])
  my_sum
}
m <- matrix(data = c(114:133), nrow = 4, byrow = TRUE)
pos <- c(1, 4, 2)
specific_sum_vec(m,pos)



(b)

long_names_vec <- function(names){
  name <- names[nchar(names) >= 8]
  name
}
my_names <- c("alexander", "david", "sebastian", "johnathan", "christopher", "ha",
              "washington", "lincoln", "maximo", "mason", "luca", "anthony", "kevin")

long_names_vec(names = my_names)



(c)

roulette_vec <- function(many_bets){
  win_lose_random <- sample(x = c(TRUE, FALSE), size = length(many_bets), replace = TRUE)

  many_bets[many_bets == "low"] <- 10
  many_bets[many_bets == "high"] <- 10
  many_bets[many_bets == "red"] <- 20
  many_bets[many_bets == "black"] <- 20
  many_bets[many_bets == "odd"] <- 15
  many_bets[many_bets == "even"] <- 15
  many_bets[many_bets == "first"] <- 50
  many_bets[many_bets == "second"] <- 50
  many_bets[many_bets == "third"] <- 50

  as.numeric(many_bets)*win_lose_random
}

set.seed(385)
roulette_vec(many_bets = c("red"))

roulette_vec(many_bets = c("red", "black", "low", "high"))

long_vec <- rep(c("red", "black", "low", "high", "second", "first", "third",
                  "odd", "even"), 10000)
system.time(roulette_vec(many_bets = long_vec))
roulette_vec(many_bets = c("red", "black", "low", "high"))
