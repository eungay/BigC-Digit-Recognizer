# BigC-Digit-Recognizer
 Digit Recognizer 예제 실습
자 이제 코드를 입력해 보아요

#sample size가 2
tpt[, sample(MaxTemp, 5)]
SampleMeans <- NULL
Means <- NULL
for(i in 1:1000){
  #Means[i] <- Means
  Means <- append(Means, mean(tpt[, sample(MaxTemp, 2)], na.rm = T))
  i <- i+1
  print(i)
  if(i == 1001) break
}
SampleMeans <- data.table(SampleSize2 = Means)


#size = 5
Means <- NULL
for(i in 1:1000){
  #Means[i] <- Means
  Means <- append(Means, mean(tpt[, sample(MaxTemp, 5)], na.rm = T))
  i <- i+1
  print(i)
  if(i == 1001) break
}
SampleMeans[,SampleSize5 := Means]

#size = 25
Means <- NULL
for(i in 1:1000){
  #Means[i] <- Means
  Means <- append(Means, mean(tpt[, sample(MaxTemp, 25)], na.rm = T))
  i <- i+1
  print(i)
  if(i == 1001) break
}
SampleMeans[,SampleSize25 := Means]

#size = 49
Means <- NULL
for(i in 1:1000){
  #Means[i] <- Means
  Means <- append(Means, mean(tpt[, sample(MaxTemp, 49)], na.rm = T))
  i <- i+1
  print(i)
  if(i == 1001) break
}
SampleMeans[,SampleSize49 := Means]
tpt[MaxTemp == -999, MaxTemp]

SampleMeans[1:10, mean(SampleSize5)]
SampleMeans[1:100, mean(SampleSize5)]
SampleMeans[1:500, mean(SampleSize5)]
SampleMeans[1:1000, mean(SampleSize5)]
sapply(SampleMeans, sd)
sapply(SampleMeans, mean)
