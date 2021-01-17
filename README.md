# Hello-world
none
data <- cpi_ppi
data
install.packages('plotrix')
library(plotrix)
Date <- seq.Date(from=as.Date("2010-01-01"),to=as.Date("2020-11-01"),by="month")
df1<- data.frame(Date=Date,cpi=cpi,ppi=ppi)
df1
twoord.plot(lx=df1$Date,ly=df1$ppi,
            rx=df1$Date,ry=df1$cpi,
            xlim=c(0,133),lylim=c(94,107),rylim=c(99,107),
            main="CPI和PPI序列的时序图",
            lcol="blue",rcol="red",
            xlab="time",ylab="PPI",rylab="CPI",type=c("l","l"),
            lytickpos = c(94,107),
            xtickpos = df1$Date,
            xticklab = df1$Date)
