# Import the data source https://ourworldindata.org/covid-deaths

covid.data <- read.csv("C:/Users/natha/Downloads/owid-covid-data (1).csv")
View(covid.data)

# Select columns for analysis using %%


selected_data <- covid.data %>% select("continent","location", "date", "population" ,"total_cases", "total_deaths", "
                                       people_fully_vaccinated","female_smokers","male_smokers", "population_density")
                                       
View(selected_data)

# Manipulate the data using piping 

library(tidyverse)

new_selected <- selected_data %>% 
  mutate(total_smokers = female_smokers + male_smokers, percentage_deaths = (total_deaths/total_cases)*100, 
          percentage_population_death = (total_deaths/population)*100  )
View(new_selected)
write.csv(new_selected, "Covid.csv", row.names=FALSE)
getwd()
