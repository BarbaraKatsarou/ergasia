# Example of Read.md
##Κώδικας mtcars
?mtcars
dat=mtcars
pmatrix=scale(dat)
d=dist(pmatrix)
c=hclust(d,method="ward.D2")
plot(c)
*Παρατηρούμε ότι ξεχωρίζουν τέσσερις μεγάλες ομάδες*
rect.hclust(c,k=4)
groups<-cutree(c,k=4)
table(mtcars$mpg,groups)
