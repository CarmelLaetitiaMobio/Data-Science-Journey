## Data-Science-Journey
Working on building my portfolio


**Project 1: Cyclistic_CaseStudy**

I completed the Google Data Analytics Professional Certificate. I will be working on one of the case study we have available on the website. 

[Cyclsitic](https://www.coursera.org/learn/google-data-analytics-capstone/supplement/7PGIT/case-study-1-how-does-a-bike-share-navigate-speedy-success)

A bike-share program that features more than 5,800 bicycles and 600 docking stations. Cyclistic sets itself apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with
disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about
8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day

> **Scenario**

I am a junior data analyst working in the marketing analyst team for the past six(6) months at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members.
But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

The following derivables for this project.

- A clear statement of the business task
- A description of all data sources used
- Documentation of any cleaning or manipulation of data
- A summary of your analysis
- Supporting visualizations and key findings
- three recommendations based on analysis

> **Ask**

The main goal is to design marketing strategies aimed at converting casual riders into annual members.


> **Prepare** 

#Data: 
The data has been made available by Motivate International Inc. under this [license](https://ride.divvybikes.com/data-license-agreement). 
 Due to data-privacy, any personally-identifiable information has been removed/encrypted.


The past 12 months of Cyclistic trip data will be used to explore how different customer types are
using Cyclistic bikes. The data is organized by month from January 2021 to December 2021. 
The data included information about the Ride_id, type of ride , start date and time and location,
type of members, trip length, and locations.



#R-Code

```R
##Install packages

install.packages("tidyverse")
install.packages("leaflet")
install.packages("mapview")
install.packages("janitor")

##run library

library(tidyverse) #data
library(lubridate) #data attributes
library(ggplot2) #visualize data
library(data.table)#add columns/large data
library(janitor)#cleaning dirty table
library(lealflet)#mapping

##upload all .csv files on R

m1<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202101-divvy-tripdata.csv")
m2<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202102-divvy-tripdata.csv")
m3<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202103-divvy-tripdata.csv")
m4<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202104-divvy-tripdata.csv")
m5<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202105-divvy-tripdata.csv")
m6<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202106-divvy-tripdata.csv")
m7<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202107-divvy-tripdata.csv")
m8<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202108-divvy-tripdata.csv")
m9<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202109-divvy-tripdata.csv")
m10<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202110-divvy-tripdata.csv")
m11<-read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202111-divvy-tripdata.csv")
m12<- read.csv("C:\Users\carme\OneDrive\Documents\R work\p1\datacyc\Project1\divvy-trip data\202112-divvy-tripdata.csv")

##Clean the data 
##Removed columns start_station_id	end_station_name	end_station_id(empty rows) 

m1_2021=select(m1, -start_station_id,-end_station_name,-end_station_id)
m2_2021=select(m2, -start_station_id,-end_station_name,-end_station_id)
m3_2021=select(m3, -start_station_id,-end_station_name,-end_station_id)
m4_2021=select(m4, -start_station_id,-end_station_name,-end_station_id)
m5_2021=select(m5, -start_station_id,-end_station_name,-end_station_id)
m6_2021=select(m6, -start_station_id,-end_station_name,-end_station_id)
m7_2021=select(m7, -start_station_id,-end_station_name,-end_station_id)
m8_2021=select(m8, -start_station_id,-end_station_name,-end_station_id)
m9_2021=select(m9, -start_station_id,-end_station_name,-end_station_id)
m10_2021=select(m10, -start_station_id,-end_station_name,-end_station_id)
m11_2021=select(m11, -start_station_id,-end_station_name,-end_station_id)
m12_2021=select(m12, -start_station_id,-end_station_name,-end_station_id)

##Combine the files together in one database

all_trips<-bind_rows(m1_2021,m2_2021,m3_2021,m4_2021,m5_2021,m6_2021,m7_2021,m8_2021,m9_2021,m10_2021,m11_2021,m12_2021)

##descriptive analysis


# mean,median,25th and 75th quartiles,min,max
summary(biketrip_2021)







```


> **Process**


> **Analyze**



