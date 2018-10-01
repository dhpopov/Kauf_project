# Kauf_project
# This project is about optimizing business processes inside the company
#
library(dplyr)
a <-subset(km, sensor_type == "drive_wheel_V_eff")
View(a)
hist(a$mean_realvalue)
b <-subset(km, sensor_type == "drive_wheel_a_max")
install.packages("ggplot2")
library(ggplot2)
frame_data(a) %>%
  ggplot(aes(x=a$date_measurement, y=a$mean_realvalue))+
  geom_point(alpha=0.5)
plot(a$mean_realvalue)
qplot(
