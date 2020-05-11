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

2. Next, I had R read the CSV file I downloaded from the FEC and created a data frame based on the CSV.
```
read.csv("raw_winred_data.csv")

raw_winred_data <- read.csv("raw_winred_data.csv")
```

3. Third, I filtered the raw FEC data to include only the columns I wanted. I saved this data to a new data frame: filtered_winred_data
```
filtered_winred_data <- raw_winred_data %>% 
  select(committee_name, recipient_state, candidate_office_district, recipient_name, candidate_first_name, candidate_last_name, disbursement_date, disbursement_amount, disbursement_description)
```

4. After filtering the raw data, I wanted to clean it up a little more. More specifically, I wanted to combine "candidate_first_name" and "candidate_last_name" into one column. To do this, I did the following"
```
mydata$fullname<-paste(mydata$first_name, mydata$last_name, sep=" ")
```

5. Then I filtered the data again to remove the "candidate_first_name" and "candidate_last_name" columns and reorganize the order of the columns.
```
filtered_winred_data <- filtered_winred_data %>%
  select(committee_name, recipient_state, candidate_office_district, recipient_name, fullname, disbursement_date, disbursement_amount, disbursement_description)
```

6. Finally, I turned the data frame containing the filtered data into a CSV and saved it to my computer.
```
write.csv(filtered_winred_data,"filtered_winred_data.csv", row.names = FALSE) 
```
