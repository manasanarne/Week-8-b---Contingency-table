# Week-8-b---Contingency-table
m<-as.table(rbind(c(190,243,197),c(82,44,44),c(23,78,34),c(5,12,8)))
dimnames(m)=list(Empcategory=c("Labour","Clerks","Technicians","Executives"), BonusSchemes=c("Type1","Type2","Type3"))
print(m)
csum<-colSums (m)
rsum<-rowSums (m)
mytable<-(rbind(m,csum))
print(mytable)
mytable<-(cbind(m,rsum))
print(mytable)
test<-chisq.test(m)
print(test)
print(test$expected,3)

OUTPUT:-
BonusSchemes
Empcategory    Type1  Type2  Type3
  Labour      196.88 247.41 185.72
  Clerks       53.12  66.76  50.11
  Technicians  42.19  53.02  39.80
  Executives    7.81   9.82   7.37
