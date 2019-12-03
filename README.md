# Dashboard R Shiny

Dataset gathering all the projects from Kickstarter crowdfunding platform since 2009  
378661 projects, each with 15 variables such as country, project name, amount requested, amount raised, etc.   


## Packages installation
 
Everything is in the notebook but here's all the packages needed :  

package_install = c("shiny", "leaflet","lubridate","tidyverse","countrycode",'treemap',"devtools","geojsonio","ggthemes")  
install.packages(package_install)  

library("devtools")  
install_github("timelyportfolio/d3treeR")  
library("d3treeR")  

library("tidyverse")  
library("lubridate")  
library("tidyr")  
library("dplyr")  
library("shiny")  
library("leaflet")  
library("countrycode")  
library("treemap")  
library("ggthemes")  
library("geojsonio")  
library("rgdal")  


## Script

Description of the required operations to run the notebook in R Studio.

Open kickstarter.Rproj in R studio.  
Once the project is open, open kickstarter_notebook.Rmd, ui.R and server.R in Files if they are not already open.  
Then "Run all" (Ctrl+Alt+R) kickstarter_notebook.Rmd.  
Wait for everything to load (a little long because of the download of the csv and packages).  

If there is an error with "cntryname <- countrycode(unique(ksprojects1$country), "iso2c", "country.name.fr")""  
change the "country.name.fr" to "un.name.fr". I don't why there is this error.

Once finished go to ui.R and "Run App".  
Wait a little while for the different graphs to load.  

If there is a need to reload the csv, uncomment the line "#ksprojects <- read.csv("ks-projects-201801.csv",encoding="UTF-8")" and 
execute it.  
This allows the csv to be loaded locally (which goes much faster).  
