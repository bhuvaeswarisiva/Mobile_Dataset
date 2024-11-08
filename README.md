# User-Behaviour-Dataset Analysis:

## Objective: 

This is the dataset, which is downloaded from Kaggle website. The main purpose of the dataset is to Analyse what type of device model or operating system consumed more by the user.

## About Data: 

This dataset contains 12 columns and less than 1000 rows of data. It has the details about gender, operating system, device model, data usage, number of apps installed, battery drain, screen time and etc.

## Analysis List: 
To ensure data should be cleaned which is checking duplicate, null values, irrelevant data before processing the analysis.

 #### Conducting the Exploratory Data analysis is understanding the data better by listed questions,
    
1.How many operating systems are used by Males and Females?
    
    =COUNTIFS(Mobile[Gender],user_behavior_dataset!J3,Mobile[Operating System],user_behavior_dataset!C3)
    
2.What type of mobile using by gender?
  
    =UNIQUE(Mobile[Device Model])
    =COUNTIFS(Mobile[Gender],user_behavior_dataset!J4,Mobile[Device Model],user_behavior_dataset!B3)

    
3.Total data usage by Gender in different age category 
   
    =SUMIFS(Mobile[Data Usage (MB/day)],Mobile[Gender],user_behavior_dataset!$J$4,Mobile[Age],">=18", Mobile[Age], "<=30")
    
4.Total screen time by gender?

    =SUMIFS(Mobile[Screen On Time (hours/day)],Mobile[Gender],user_behavior_dataset!J4) 
    
5.Which 5 device model drained the battery quickly?

    =SMALL(Mobile[Battery Drain (mAh/day)],1)
    =XLOOKUP(C36,Mobile[Battery Drain (mAh/day)],Mobile[Device Model])

6.Calculating most app installed by Gender?

    =SUMIFS(Mobile[Number of Apps Installed],Mobile[Gender],user_behavior_dataset!J4)
   
7.Total screen time (hours/day) by different age group of people?

    =SUMIFS(Mobile[Screen On Time (hours/day)],Mobile[Gender], user_behavior_dataset!$J$4, Mobile[Age], ">=18", Mobile[Age], "<=20")

     
