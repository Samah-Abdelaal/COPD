library(tidyverse)

copd <- read_csv("Data/COPD_student_dataset.csv")

str(copd)

copd %>%
  select(FEV1, SGRQ) %>%
  summary()

shapiro.test(copd$FEV1)
shapiro.test(copd$SGRQ)

copd %>%
  ggplot(aes(x= FEV1))+
  geom_histogram(binwidth = 0.2)

copd %>%
  ggplot(aes(x= SGRQ))+
  geom_histogram(binwidth = 4)

copd %>%
  ggplot(aes(x = FEV1, y= SGRQ))+
  geom_point()+
  geom_abline()

cor(copd$FEV1, copd$SGRQ, method = "pearson")
cor(copd$FEV1, copd$SGRQ, method = "spearman")
