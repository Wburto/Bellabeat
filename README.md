This is just the raw 'R' code and cleaned data sets for my Google Capstone project. To see the completed project, with the code and visualisations run correctly, please visit the following link [*link*](https://rpubs.com/Willb/Bellabeat_Capstone) 






Welcome to my Google Coursera Data Analytics Capstone project, focused on Bellabeat---a pioneering company transforming women's health and wellness. By analysing data from comparable wearable devices (FitBit), we'll extract insights and provide actionable recommendations. The comprehensive approach will follow the course guidelines of ask, prepare, process, analyse, share, and act in order to enhance Bellabeat's products and empower women with informed health decisions. Let's dive in and make a positive impact!

------------------------------------------------------------------------

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRH3psWGkqeywpsyHfP9k6Pa6fpxL7ioRjomsiDZ_s6S_zl6Fbs24k3hfSbiaiUZ61q400&usqp=CAU)

> Founded by Urška Sršen and Sandro Mur in 2014. Bellabeat is best known for its Leaf smart jewellery wearable line that is created only for women and tracks sleep, steps, menstrual cycle, mindfulness, and activity. The company aims to revolutionise women's health and wellness through fashionable wearable devices. They provide personalised solutions, monitor various health parameters, and offer valuable insights. With a focus on community support and continuous innovation, Bellabeat is leading the way in women's health technology.

There are three main stakeholders of Bellabeat to consider. 

1.  **Urška Sršen**: Bellabeat's cofounder and Chief Creative Officer

2.  **Sando Mur**: Mathematician and Bellabeat's cofounder; key member of the Bellabeat executive team

3.  **Bellabeat marketing** analytics team.\

And, as per the course guidelines, there are three main questions:

1\. What are some trends in smart device usage?

2\. How could these trends apply to Bellabeat customers?

3\. How could these trends help influence Bellabeat marketing strategy?

While all of the questions can be answered by considering the data alone, I want to first briefly consider the external research of questions 1. What are some trends in smart device usage? As a note, I think that there is an important distinction to be made about the smart devices being wearable, as there is a potential to find broader trends with less relevance. 

With the advent of 5g we're seeing more and more devices able to operate in the same area as they are no longer "[*fighting for bandwidth*](https://www.forbes.com/sites/bernardmarr/2021/03/05/the-biggest-wearable-technology-trends-in-2021)". Another effect that comes with an advancement of technology is that devices get smaller, "[*as there will be less need for them to contain powerful data-processing hardware in the devices themselves*](https://www.forbes.com/sites/bernardmarr/2021/03/05/the-biggest-wearable-technology-trends-in-202)." This technological advancement only serves to make wearable wellness technology more accessible and therefore there has been a steady increase in 'Smart Wearable Users'

> ![](https://www.insiderintelligence.com/_gatsby/image/609aa03739387bbb57a5e5ff49a1e839/c1863e55ac64feb575156148d6b2a197/Smart-Wearable-Users.png?u=https%253A%252F%252Fpublicsite-wordpress-storage-public.insiderintelligence.com%252Fwp-content%252Fuploads%252F2022%252F02%252F11160731%252FSmart-Wearable-Users.png&a=w%253D1020%2526h%253D920%2526fm%253Dpng%2526q%253D90&cd=2022-02-11T21%253A07%253A30){width="473"} [source](https://www.insiderintelligence.com/insights/wearable-technology-healthcare-medical-devices/)

Consider the following graphic which suggests that monitoring health is at 75% of adult's healthcare concerns.  So we know that not only wearable wellness technologies relevant, they are also a growing market.

> ![](https://lh4.googleusercontent.com/KE9xMq_KU6LbsTXJWMA9WBhH78J2QqMehw-ut7JzWVgYBwnH-AgXO8xuR0N0gi7fvxMsFklhDrHvipijxW7d7g6S-R8SHp9g6runjnU2678UfU0D5UzG5rb_th47CwtOBOUlIZPSN0oBeB6HV0yjjqlzSU77ci3_BHcdzxvbA40Goljc6BqTm709JgIJ){width="462"} [source](https://www.insiderintelligence.com/insights/wearable-technology-healthcare-medical-devices/)\
>
> ------------------------------------------------------------------------

# Now the data preparation stage.

The data is hosted on [Kraggle](https://www.kaggle.com/datasets/arashnic/fitbit)(CC0: Public Domain, data set made available through Mobius). It is a  in a mix of both wide and long formats detailing various bodily metrics such as weightlogs and calories spent. I have downloaded the data set to be able to backup and modify the files locally. 

In accordance with best practice, I will apply the ROCCC (Relevance, Objectivity, Currency, Coverage, and Comprehensiveness to test it's credibility. 

### *Reliable*

| The main issue with the data is the small sample size of around 30 users. With a limited number of observations, there is a higher risk of sampling errors and biases, making it challenging to generalise findings to a broader context.
| 
| There is also a problem with the lack of data on demographics of users. Drawing conclusions from anonymous data feels inadequate, especially when Bellabeat pride themselves on the personalisation of their data towards women. 
| **The Reliability Score** = LOW

### *Original*

| The data is not from the client Bellabeat, rather the data is sourced from what could be described as a competitor in FitBit. This damages the direct relevance of the data. 
| 
| Beyond this, FitBit outsourced the gathering of the data to AMT. Amazon Mechanical Turk is a crowdsourcing website with which businesses can hire remotely located 'crowdworkers' to perform discrete on-demand tasks that computers are currently unable to do as economically. It is operated under Amazon Web Services, and is owned by Amazon. So the data is not even directly sourced by the company FitBit. Again damaging the reliability of the data and making it far from the ideal primary source.
| **The Originality Score** = LOW

\

### *Comprehensive*

| There are, upon further reflection, large gaps within specific sheets of this data rendering several sets inadequate for use. However, several important sets are well populated and should be sufficient for more general analysis. 
| 
| Worth noting that the two month period through which the study was run is not quite sufficient for detailed conclusions.
| **The Originality Score** = MIDDLING

\

### *Current*

| This dataset is about seven years old rendering it much less reliable than more current data sets.
| **The Originality Score** = LOW

### *Cited*

| While AMT, as discussed before, is cited there is no more information than that. The fact that AMT is "discrete" renders the chain of responsibility obsolete. 
| 
| It is publicly hosted on Kraggle but with limited sources or information. 
| **The Citing Score** = LOW

\
As the dataset is held under a CC0 1.0 Licence it is open for public use and has no copyright concerns. Given the CC0 Licence, and it's open public nature, I have no privacy, security and accessibility concerns. For ease of accessibility and for the most efficient operations I will be downloading the data to my local drives. 

In conclusion, using the ROCCC model it is clear that the data fails to satisfy any of the necessary checks. It isn't appropriate to draw too many actionable conclusions, rather it is more appropriate for looking at more general, historic trends within the wearable wellness industry. 

With that being said, I will treat the data as both useful and relevant from here so as to display the tools and techniques learnt in the course.

------------------------------------------------------------------------

Now for the data cleaning process! I am cleaning data in R because I want to be able to utilise what I have learned but also because I want to to be able to automate most of the tasks, reducing the chance of human error.

First we install the necessary packages.

```{r}
install.packages("tidyverse") 
install.packages("lubridate") 
install.packages("dplyr")
install.packages("ggplot2")
install.packages("tidyr")
```

Then we load them.

```{r}
library(tidyverse)
library(lubridate)
library(dplyr)
library(ggplot2)
library(tidyr)
```

Next we bring in the relevant .csv files that we have already uploaded and create their corresponding data frames.

```{r}
daily_activity <- read_csv("Fitabase Data/dailyActivity_merged.csv")
hourly_calories <- read_csv("Fitabase Data/hourlyCalories_merged.csv")
sleep <- read_csv("Fitabase Data/sleepDay_merged.csv")
weightlog <- read.csv("Fitabase Data/weightLogInfo_merged.csv")
intensities <- read.csv("Fitabase Data/hourlyIntensities_merged.csv")
steps <- read.csv("Fitabase Data/hourlySteps_merged.csv")
heartrate <- read.csv("Fitabase Data/heartrate_seconds_merged.csv")
```

Now, let's check everything is in order quickly.

```{r}
View(daily_activity)
head(daily_activity)
View(hourly_calories)
head(hourly_calories)
View(intensities)
head(intensities)
View(sleep)
head(sleep)
View(weightlog)
head(weightlog)
View(steps)
head(steps)
View(heartrate)
head(heartrate)
```

------------------------------------------------------------------------

There are issues with this data set as have already been explained but I will detail my immediate observations:

### *Daily Activities:*

> I notice that there are 109 rows with a surely erroneous number of steps (0-1000), 77 rows of this data are an exact 0. It is safe to assume that there was no data entered/recorded on those days, or at the very least the data is only partial.
>
> There are only 4 rows of data that show 0 calories but there are 127 rows below the low average threshold of 1,600 calories burnt by the [lowest](https://www.everydayhealth.com/weight/how-to-achieve-one-pound-of-weight-loss.aspx#:~:text=To%20lose%20a%20pound%2C%20you,man%20expends%202%2C000%20to%203%2C000) average human.
>
> I will need to format the date to keep the data consistent.

### *Hourly Calories:*

| A good data set with consistent entries.
| 
| I will need to format the date to keep the data consistent.

### *Intensities:*

| Many records showing intensity at a 0, which is fine as intensities is [measure](https://www.verywellfit.com/why-active-minutes-mean-more-than-steps-4155747#:~:text=Fitbit%20uses%20your%20cadence%20or,exercise%20to%20track%20active%20minutes)d differently to steps. The patients could be recording no time spent above the 10 minute higher heart rate threshold.
| 
| I will need to format the date to keep the data consistent.

### *Sleep:*

| A good data set with consistent entries. While concerning it is entirely possible that many users had only an hours sleep.
| 
| I will need to format the date to keep the data consistent.

### *Steps:*

| A good data set with consistent entries however, as predicted there are many entries that haven't recorded steps. It is still useful data to keep though as it will cross reference with intensities and calories.
| 
| I will need to format the date to keep the data consistent.

### *Weightlog:*

| A good data set with consistent entries however, there are only 67 entries total. 
| 
| As such, I will have to remove the weightlog data frame.

```{r}
rm(weightlog)
```

### *Heartrate:*

| A good data set with consistent entries and even though there are some worryingly low heartrates, no one is clinically dead.
| 
| heartrate is in seconds so will need to be reformatted to minutes to align with the other data.
| 
| I will need to format the date to keep the data consistent.

------------------------------------------------------------------------

Now we check for unique values

```{r}
n_distinct(daily_activity$Id)
n_distinct(hourly_calories$Id)
n_distinct(intensities$Id)
n_distinct(sleep$Id)
n_distinct(steps$Id)
n_distinct(heartrate$Id)
```

daily_activities, hourly_calories, intensities and steps have all returned a result of 33 unique ID's.

sleep has returned 24 unique ID's.

heartrate has only returned 14 unique ID's which is too low a sample size and therefore it needs to be removed from the analysis. Frustrating but fair.

heartrate has too few values, it is removed.

```{r}
rm(heartrate)
```

------------------------------------------------------------------------

Let's check to see if there are any duplicates now.

```{r}
sum(duplicated(daily_activity))
sum(duplicated(hourly_calories))
sum(duplicated(intensities))
sum(duplicated(sleep))
sum(duplicated(steps))
```

There are 3, in sleep, they will need to be removed.

```{r}
sleep <- sleep %>%
  distinct() %>%
  drop_na()
```

let's make sure that worked.

```{r}
sum(duplicated(sleep))
```

------------------------------------------------------------------------

Next I rename the columns in each remaining data frame for consistency's sake in case there will be merging later on

```{r}
daily_activity <- daily_activity %>% 
  rename(Date= ActivityDate)
```

```{r}
sleep <- sleep %>%
  rename(ActivityDate= SleepDay)
```

```{r}
hourly_calories <- hourly_calories %>%
  rename(ActivityDate= ActivityHour)
```

```{r}
intensities <- intensities %>%
  rename(ActivityDate= ActivityHour)
```

```{r}
steps <- steps %>%
  rename(ActivityDate= ActivityHour)
```

------------------------------------------------------------------------

I want to split the ActivityDate column of the data frames into two separate "Date" and "Time" columns. Then I will format them as the correct data types.

### *steps*

```{r}
steps$ActivityDate <- as.POSIXct(steps$ActivityDate,format="%m/%d/%Y %I:%M:%S %p",tz=Sys.timezone())
steps$Date <- as.Date(steps$ActivityDate)
steps$Time <- format(as.POSIXct(steps$ActivityDate), format = "%H:%M:%S", tz=Sys.timezone())
steps <- subset(steps, select=-ActivityDate)
```

### *intensities*

```{r}
intensities$ActivityDate <- as.POSIXct(intensities$ActivityDate,format="%m/%d/%Y %I:%M:%S %p",tz=Sys.timezone())
intensities$Date <- as.Date(intensities$ActivityDate)
intensities$Time <- format(as.POSIXct(intensities$ActivityDate), format = "%H:%M:%S", tz=Sys.timezone())
intensities <- subset(intensities, select=-ActivityDate)
```

### *sleep*

```{r}
sleep$ActivityDate <- as.POSIXlt(sleep$ActivityDate, format = "%m/%d/%Y %H:%M:%S", tz = Sys.timezone())
sleep$Date <- as.Date(sleep$ActivityDate)
sleep$Time <- format(as.POSIXct(sleep$ActivityDate), format = "%H:%M:%S", tz=Sys.timezone())
sleep <- subset(sleep, select=-ActivityDate)
```

### *daily_activity*

```{r}
daily_activity <- daily_activity %>%
  mutate(Date = as_date(Date, format = "%m/%d/%Y"))
  names(daily_activity)[2] <- 'Date'
```

### *hourly_calories*

```{r}
hourly_calories$ActivityDate <- as.POSIXct(hourly_calories$ActivityDate,format="%m/%d/%Y %I:%M:%S %p",tz=Sys.timezone())
hourly_calories$Date <- as.Date(hourly_calories$ActivityDate)
hourly_calories$Time <- format(as.POSIXct(hourly_calories$ActivityDate), format = "%H:%M:%S", tz=Sys.timezone())
hourly_calories <- subset(hourly_calories, select=-ActivityDate)
```

------------------------------------------------------------------------

Let's merge the relevant files together, now that there are correct formatting. I merged the tables to focus on "Id", "Date" and "Time" in order to ensure they matched up.

```{r}
intensities <- merge(steps, intensities, by = c("Id", "Date", "Time"), all = TRUE)
```

and I also wanted to merge hourly_calories with daily_activity I chose the "Id" and "Date" options to merge as they were again the common columns.

```{r}
daily_activity <- merge(hourly_calories, daily_activity, by = c("Id", "Date"), all = TRUE)
daily_activity <- daily_activity %>%
  rename(CaloriesHour= Calories.x)
daily_activity <- daily_activity %>%
  rename(CaloriesDay= Calories.y)
```

I then renamed the appropriate calorie columns "CaloriesHour" and "CaloriesDay" to retain both sets of data.

I am now left with three columns "daily_activity", "intensities" and "sleep"

------------------------------------------------------------------------

I want to look at the newly merged data now

```{r}
install.packages("psych")
library(psych)
describe(daily_activity)
describe(intensities)
describe(sleep)
```

Now I'd like to summarise the new data frames:

### *daily_activity*

```{r}
daily_activity %>%  
  select(TotalSteps,
               TotalDistance,
               SedentaryMinutes,
               CaloriesDay) %>%
 summary()
```

### *sleep*

```{r}
sleep %>%  
  select(TotalSleepRecords,
         TotalMinutesAsleep,
         TotalTimeInBed) %>%
  summary()
```

### *intensities*

```{r}
intensities %>%  
  select(StepTotal,
               TotalIntensity,
               AverageIntensity) %>%
  summary()
```

The data looks fairly normal but I notice that many users are not reaching their [recommended](https://www.mayoclinic.org/healthy-lifestyle/fitness/in-depth/10000-steps/art-20317391#:~:text=The%20average%20American%20walks%203%2C000,a%20day%20every%20two%20weeks) 10,000 steps a day but still burning calories so I realise at this point that METs are a useful and seemingly universal tool for measuring intensity. So i add the appropriate .csv file to the project, and clean it like normal.

> A quick note on how FItBit organises it's users into activity level. It does it through MET's to measure the intensity level.:
>
> -   Earn active minutes through 10 minutes or more of continuous moderate-to-intense activity.
>
> -   Sedentary, Light, Fairly, and Very Active, minutes can be defined as the following metabolic equivalent of tasks (METs) for each level of activity: [Source](https://en.wikipedia.org/wiki/Metabolic_equivalent_of_task))
>
>     -   Sedentary: Activities less than 1.5 METs
>
>     -   Light: Activities less than 3 METs
>
>     -   Fairly/Moderate: Activities between 3 - 6 METs
>
>     -   Very: Activities greater than 6 METs
>
> From John, a FitBit Dev on the forum [here](https://community.fitbit.com/t5/Web-API-Development/Daily-Activity-Summary-Data-Definition-Questions/td-p/3087077)

> For reference, this scientific journal [here](https://pubmed.ncbi.nlm.nih.gov/14715035/#:~:text=7500%2D9999%20likely%20includes%20some,classify%20individuals%20as%20'active'.) suggests the following measurements for classifying users steps: "Based on currently available evidence, we propose the following preliminary indices be used to classify pedometer-determined physical activity in healthy adults:
>
> -   \<5000 steps/day may be used as a 'sedentary lifestyle index';
>
> -   5000-7499 steps/day is typical of daily activity excluding sports/exercise and might be considered 'low active'
>
> -   7500-9999 likely includes some volitional activities (and/or elevated occupational activity demands) and might be considered 'somewhat active'
>
> -   \>or=10000 steps/day indicates the point that should be used to classify individuals as 'active'.
>
> -   \>12500 steps/day are likely to be classified as 'highly active'."

A table with the two side by side so you can see how both metrics fit into their recommended categories.

|                  |                     |                             |
|------------------|---------------------|-----------------------------|
|                  | **Steps a day**     | **MET's (intensity level)** |
| *Sedentary*      | \< 5000             | \<1.5                       |
| *Lightly Active* | \>= 5000 - \< 7499  | \<3                         |
| *Fairly Active*  | \>= 7500 - \< 9999  | 3-6                         |
| *Very Active*    | \>= 1000 \*         | 6                           |

##### \*Note there is a separate 'highly active' (\>12500 steps) category but for the purposes of aligning it with the MET's I have chose to amalgamate the 'very' and 'highly active' categories.

```{r}
METs <- read.csv("Fitabase Data/minuteMETsNarrow_merged.csv")
```

I notice that the values of the METs are extremely high, in some cases they are well beyond even the 'Very Active' category of user. Thanks to some research by this Kaggle user [here](https://www.kaggle.com/code/marcoantonioreyes/bellabeat-a-step-by-step-analysis) I am saved, and see that FitBit doesn't record the decimal point, as per the post [here](https://community.fitbit.com/t5/Web-API-Development/Definition-of-Mets-in-Charge-HR/td-p/1240824?nobounce).

Let's address that. Then I changed the minute recording to daily and formatted the dates, column names in order to merge with daily_activity. I do this so I can compare them as daily averages compared to other daily averages.

```{r}
METs <- METs %>%
  mutate(ActivityMinute = mdy_hms(ActivityMinute))
```

```{r}
METs <- mutate(METs, METs = METs/10)
METs <- mutate(METs, date = date(ActivityMinute))
mets_daily <- aggregate(METs~Id + date, METs, FUN=sum)
mets_daily <- rename(mets_daily, Date = date)
```

Finally I merge the METs data frame into the daily_activity data frame.

```{r}
daily_activity <- merge(daily_activity, mets_daily, by = c("Id","Date"))
colnames(daily_activity)[colnames(daily_activity) == "METs"] <- "METsDay"
```

------------------------------------------------------------------------

I want to see averages now to get a better sense of the data so I create a new daily_average data frame from some of the columns in the daily_activity data frame.

```{r}
daily_average <- daily_activity %>%
  group_by(Id) %>%
  summarize (AvgDailySteps = mean(TotalSteps), AvgDailyCalories = mean(CaloriesDay), AvgSedentaryMinutes = mean(SedentaryMinutes), AvgLightlyActiveMinutes = mean(LightlyActiveMinutes), AvgFairlyActiveMinutes = mean(FairlyActiveMinutes), AvgVeryActiveMinutes = mean(VeryActiveMinutes), AvgDailyMETs = mean(METsDay) )
```

Then I would like to see the averages in the User Types as defined in the follow on document.

```{r}
user_type <- daily_average %>%
  mutate(user_type = case_when(
    AvgDailySteps < 5000 ~ "sedentary",
    AvgDailySteps >= 5000 & AvgDailySteps < 7499 ~ "lightly active", 
    AvgDailySteps >= 7500 & AvgDailySteps < 9999 ~ "fairly active", 
    AvgDailySteps >= 10000 ~ "very active"
    ))
```

Let's turn that into percentages.

```{r}
user_type_percent <- user_type %>%
  group_by(user_type) %>%
  summarise(total = n()) %>%
  mutate(totals = sum(total)) %>%
  group_by(user_type) %>%
  summarise(total_percent = total / totals) %>%
  mutate(labels = scales::percent(total_percent))

user_type_percent$user_type <- factor(user_type_percent$user_type , levels = c("very active", "fairly active", "lightly active", "sedentary"))

```

I'd like to see that as a pie chart.

```{r}
user_type_percent$user_type <- factor(user_type_percent$user_type , levels = c("very active", "fairly active", "lightly active", "sedentary"))
user_type_percent %>% 
  ggplot(aes(x="",y=total_percent, fill=user_type)) + 
  geom_bar(stat ="identity", width = 1)+ 
  coord_polar("y", start=0)+ theme_minimal()+ 
  theme(axis.title.x= element_blank(), 
        axis.title.y = element_blank(), 
        panel.border = element_blank(), 
        panel.grid = element_blank(), 
        axis.ticks = element_blank(), 
        axis.text.x = element_blank(), 
        plot.title = element_text(hjust = 0.5, size=14, face = "bold")) + scale_fill_manual(values = c("#0A7373","#B7BF99", "#EDAA25", "#C43302")) + geom_text(aes(label = labels), position = position_stack(vjust = 0.5))+ labs(title="User by Activity Level")
```

From the graph of the User Type Percent we can see that many different users enjoy this wearable wellness products. As such, Bellabeat needs to acknowledge this spectrum and not seek to alienate certain, less active groups. A fine balance is required however as Bellabeat should also not seek to do the reverse and alienate the "more active" groups as well.

------------------------------------------------------------------------

Now, with visualizations on the go, I would like to do some initial visual analysis to see what insights can be drawn Average Daily Met Score vs. Average Daily Calories.

```{r}
ggplot(data = daily_average) +
  geom_point(mapping = aes(x = AvgDailyCalories, y= AvgDailyMETs), color="darkgreen")+
  geom_smooth(mapping = aes(x = AvgDailyCalories, y= AvgDailyMETs), color="darkred") +
  labs(title = "Average Daily Met Score vs. Average Daily Calories",
             x = "Calories",
             y = "METs")
```

Here we see a direct correlation between Average Daily Met score and Average Daily Calories. The higher your intensity when working out, the more calories you will burn.

------------------------------------------------------------------------

Let's look at how steps affect calories in order to have a more detailed look at how those calories are being burnt off with the Average Daily Calories vs Average Daily Steps.

```{r}
ggplot(data = daily_average, aes(x=AvgDailySteps, y= AvgDailyCalories)) +
    geom_point(color = "steelblue") +
    geom_smooth(color = "darkred") +
    labs(title = "Average Daily Calories vs. Average Daily Steps")
```

We see a direct correlation. The dip around the 12000 mark could be related to a different exercise that requires fewer steps, such as weights for instance. This furthers the point that perhaps, if losing calories is the goal, steps aren't just the answer. 

The spread of users on the activity spectrum is enormous. There aren't enough people doing their recommended steps and there are also simultaneously lots of users going well above and beyond. 

------------------------------------------------------------------------

Let's now review Daily Calories versus User Type minutes to see if we can see where most calories are going.

Average Sedentary Minutes vs. Average Daily Calories

```{r}
ggplot(data = daily_average, aes(x=AvgSedentaryMinutes, y= AvgDailyCalories)) +
  geom_point(color = "steelblue") +
  geom_smooth(color = "darkred") +
  labs(title = "Average Sedentary Minutes vs. Average Daily Calories")
```

Average Lightly Active Minutes vs. Average Daily Calories

```{r}
ggplot(data = daily_average, aes(x=AvgLightlyActiveMinutes, y= AvgDailyCalories)) +
  geom_point(color = "steelblue") +
  geom_smooth(color = "darkred") +
  labs(title = "Average Lightly Active Minutes vs. Average Daily Calories")
```

Average Fairly Active Minutes vs. Average Daily Calories

```{r}
ggplot(data = daily_average, aes(x=AvgFairlyActiveMinutes, y= AvgDailyCalories)) +
  geom_point(color = "steelblue") +
  geom_smooth(color = "darkred") +
  labs(title = "Average Fairly Active Minutes vs. Average Daily Calories")
```

Average Very Active Minutes vs. Average Daily Calories

```{r}
ggplot(data = daily_average, aes(x=AvgVeryActiveMinutes, y= AvgDailyCalories)) +
  geom_point(color = "steelblue") +
  geom_smooth(color = "darkred") +
  labs(title = "Average Very Active Minutes vs. Average Daily Calories")
```

So all roughly as you might expect with the surprise of the Average Fairly Active minutes tapering off quite quickly. Perhaps this suggests that it is better to a longevity to your exercise if you want to burn calories, even if it isn't very intense.

------------------------------------------------------------------------

Given the data above, I wondered what comparing Step Total vs. Total Intensity would show us with regards to how intensity correlates with steps.

```{r}
ggplot(data = intensities, aes(x=StepTotal, y= TotalIntensity)) +
  geom_point(color = "steelblue") +
  geom_smooth(color = "darkred") +
  labs(title = "Step Total vs. Total Intensity")
```

It shows us again what we might predict, unless you're doing a Very Active sessions of steps, you won't get the intensity required to burn off calories.

------------------------------------------------------------------------

I decide I want to see the daily average of sleep times so I create the data frame.

```{r}
daily_average_sleep <- sleep %>%
  group_by(Id) %>%
  summarize (TotalMinutesAsleep = mean(TotalMinutesAsleep), TotalTimeInBed = mean(TotalTimeInBed) )
daily_average_sleep$TotalHoursAsleep <- format(as.POSIXct(daily_average_sleep$TotalMinutesAsleep), format = "%M:%S", tz=Sys.timezone())
```

I want to see that as a graph.

```{r}
theme_set(theme_bw())  # pre-set the bw theme.
g <- ggplot(daily_average_sleep, aes(Id, TotalHoursAsleep))
g + geom_count(col="steelblue", show.legend=F) +
  labs (y="TotalHoursAsleep", 
        x="Id", 
        title="Total Hours Asleep per Id")
```

This plot is just to illustrate the full variety of the sleep spectrum across the Id's. There are a significant number of users who are clearly below the average recommended sleep, this must be addressed.

------------------------------------------------------------------------

Finally I want to see the relationship between Total Minutes Slept and Total Time In Bed.

```{r}
ggplot(data = sleep) +
  geom_smooth(mapping = aes(x =TotalMinutesAsleep, y = TotalTimeInBed)) +
  labs(title = "The relationship between Total Minutes Slept and Total Time In Bed")
geom_smooth()` using method = 'loess' and formula = 'y ~ x'
```

The graph here shows a fairly predictable pattern between Total Time In Bed and Total Minutes Slept. This is a useful correlation and shows that users are mostly using their bed for sleep which is [healthy](https://www.theguardian.com/lifeandstyle/shortcuts/2018/may/14/only-use-your-bed-for-sex-and-sleep-and-other-tips-for-dealing-with-chronic-insomnia).

------------------------------------------------------------------------

## What conclusions can we draw?

Unfortunately, the incomplete, anonymous fitness-centric nature of the data available means most of our conclusions are limited. The areas that can be addressed with the most confidence involve calories and sleep.

For the most part the conclusions that can be drawn are predictable.:\
Users need to lose more calories so you tell them to exercise more.\
Users need to sleep more so you can send them warnings about getting enough sleep.\
\
However, I am more interested in insights beyond the obvious generalised wearable wellness market.

As we have seen, the activity level spread of users is surprisingly even across the merged daily_activity data frame. Drilling further into the data shows us that perhaps users are not exclusively interested in the cold hard metrics of steps and weight loss. Consider for instance, the weightlog data frame where very few of the sample size wanted to record and subsequently track their weight. Or the steps data in the daily_activity dataframe, as it now seems that steps are an [outdated](https://www.mayoclinic.org/healthy-lifestyle/fitness/in-depth/10000-steps/art-20317391) metric.

Bellabeat has a real and unique opportunity to re-frame how wellness is traditionally seen and encourage the exploration of a more, **personal and holistic** approach to health. As one [reviewer](https://www.theverge.com/23612567/bellabeat-ivy-review-reproductive-health-tracker-wearables) writes "*This isn't the tracker for data nerds or athletes looking to optimize performance. It's meant for people who'd like to protect their mental health while pursuing their health goals*."

-   Instead of the traditional and potentially damaging obsessions with weight data, calories, steps etc. why not add a broader "**well enough**" option. Allowing users to hit their recommended daily exercise but with less pressure attached. Exploring the data allowed us to see METs (intensity measure) as a more valuable way of expending calories then steps. So why not have intensity as the foremost metric for exercise?

-   Not all genders are the same and not all women are either, this is especially true when it comes to exercise; "*If one week you can blitz a high-intensity workout and the next you can barely make it through, it doesn't mean your fitness has gone backwards. If your motivation is suffering, it doesn't mean you are a failure. It could all simply be hormonal*" as [this](https://www.theguardian.com/lifeandstyle/2021/feb/02/the-menstrual-month-how-to-exercise-effectively-at-every-stage-of-your-cycle) article states. Bellabeat needs to customise it's exercise plans towards specific women and their specific context.

-   Prompts could be more like - [You are in your "*late follicular and the mid-luteal phases, oestrogen is higher.*[McNulty](#0)*says one of its many effects is to help build muscle mass"* so why not try one of our personalised hit work outs on the app?]{.underline}

-   Bellabeat already has a [Coach](https://bellabeat.com/coach/) program that it can leverage. These prompts are more successful than the traditional ones which can cause too much pressure; "*people aren't machines, and they don't need to be shamed for breaking streaks or losing some fitness during a recovery period.*" As [one](https://www.theverge.com/22774263/wearables-smartwatches-apple-watch-fitness-trackers-fitbit-streaks-recovery) article noted.

-   This is a deliberate move away from the gamification of health apps, which "*led to obsessive behaviour in an attempt to get the most shares or likes from their peers.*" as a study from Bath, Salford and University of Canberra [found](https://www.bbc.co.uk/news/uk-england-somerset-53420168). Instead it's leaning toward leveraging Bellbeats focus on a more caring, personalised and nurturing environment.

-   With regards to sleep we can see that the spectrum is fairly large again and some users need to be hitting their recommended amount of sleep. This can be done through the traditional means of timely reminders and encouragement. However, as we have seen, there is another way and Bellabeat's focus on holistic personalisation can come to the fore here. After all, menstruation, pregnancy and menopause all have an enormous and specific [effect](https://www.sleepfoundation.org/women-sleep/do-women-need-more-sleep-than-men) on women's sleep. "*Most women who have trouble with sleep at different parts of their menstrual cycle, have problems just before and after the start of menstruation, with 30% of women reporting disturbed sleep during menstruation and 23% reporting disturbed sleep in the week prior to menstruation."* See [here](https://sleephub.com.au/menstrual-cycle-and-sleep/#:~:text=Progesterone%20has%20sleep%20promoting%20effects,Oestrogen%20can%20also%20promote%20sleep.) for more information.

-   My insight for sleep is that Bellabeat offer a similar "**well enough**" approach as before. Bellabeat can compare other metrics such as activity minutes, cycle information, calories to offer advice on how best get the appropriate sleep that night. For instance a prompt could be - [As you start menstruating sleep can be difficult, why not try meditation before bed or perhaps a series of workouts during the day to reduce energy towards the end of the day.]{.underline}

-   I would also suggest that Bellabeat leverage it's social community for sleep and daily wellness. Not getting enough sleep and feeling run down can be isolating, so any support is valuable.

Ultimately Bellabeat's primary focus is on women's health and well-being. Their products are specifically designed to cater to the unique needs and experiences of women, offering personalised solutions and insights tailored to their health concerns. Bellabeat should go beyond traditional fitness tracking and embrace their differences to the current market. They should use their technology to educate, nurture and promote specific women with specific contexts and move away from the traditional outdated harassment of current gender-less wellness tech.

Please see a Tableau dashboard I created for this project [here](https://public.tableau.com/authoring/BellaBeatStory/Story1#1).\
\
Thank you for reading.\
Will
