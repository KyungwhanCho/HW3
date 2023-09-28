# HW3

Lab 3
​
library(dplyr)
library(plotly)
library(tidyverse)
​
load("Household_Pulse_data_w57.RData")
summary(Household_Pulse_data)
​
summary(RECVDVACC == 'yes got vax')
summary(RECVDVACC == 'no did not get vaxx')
summary(RECVDVACC == 'NA')
​
summary(RECVDVACC == "yes got vax")
summary(RECVDVACC)
​
restrict1 <- (Household_Pulse_data$RECVDVACC == 'NA') & (Household_Pulse_data$ANYWORK == "no employment in last 7 days")
data_new <- subset(Household_Pulse_data,restrict1)
​
view(restrict2)
summary(restrict2)
​
​
restrict2 <- (Household_Pulse_data$RECVDVACC == 'no did not get vaxx') & (Household_Pulse_data$ANYWORK == "yes employment in last 7 days")
data_new <- subset(Household_Pulse_data,restrict2)
​
restrict3 <- (Household_Pulse_data$RECVDVACC == 'yes got vaxx') & (Household_Pulse_data$ANYWORK == "yes employment in last 7 days")
data_new <- subset(Household_Pulse_data,restrict3)
summary(restrict3)
​
​
restrict4 <- (Household_Pulse_data$RECVDVACC == 'NA') & (Household_Pulse_data$ANYWORK == "yes employment in last 7 days")
data_new <- subset(Household_Pulse_data,restrict4)
summary(restrict4)
​
