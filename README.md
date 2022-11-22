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
(![mtcars](https://user-images.githubusercontent.com/118823882/203342135-6b4b3a03-0ff5-4e22-a9f7-ec22562d04ae.png)
