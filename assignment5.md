# Assignment 5

## What data did I clean?

For assignment 5 I wanted to take the opportunity to get a jump start on gathering some of the data for my final project. Accordingly, I collected and cleaned the 2019 FEC filings of WinRed, the Republican small-dollar donations platform.

## How did I do it?

Overall, the data cleaning was not that complex. After downloading the data from the FEC website, I did the following: 

1. I started by installing the tidyverse, readr, dplyr and lubridate libraries. In hindsight, I didn't need all of these for what I was doing, but they might come in handy as I carry on with my data analysis.
```
library(tidyverse)
library(readr)
library(dplyr)
library(lubridate)
```
