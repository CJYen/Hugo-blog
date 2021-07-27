---
title: "Cyclistic Bike-Share Analysis"
date: 2021-07-26T19:09:09+08:00
---

### Quick Intro

This case study is to verify my learning steps for the last two months of studying in the [Data Analyst course](https://coursera.org/share/0ad6ead310ccce190847c121ebaea8ee).

### Scenario

I'm a junior data analyst working in the marketing analyst team at Cyclistic, a fictional bike-share company based in Chicago. The marketing team is trying to design a marketing campaign that can convert casual riders to annual members. The goal is to find out user behavior and develop our membership strategy of converting casual users become members.

### Ask

Before starting, to find a way, I need to ask the leader these questions. 
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?

### Prepare

To find out user behavior between these two types of casual users and members. It needs to identify the time they use, their site, and the kinds of bikes they ride in the data.
Gain insight into user behaviors' patterns; the marketing can follow up to make suitable promotions and marketing campaigns.

With download the data of information as following:
1. Unique id for each ride
2. Type of bikes (classic, electric)
3. When the ride started
4. When the ride ended
5. Where the ride started
6. Where the ride ended
7. Whether is a member or a casual user

_Ps. With download the data according to the data [license agreement](https://www.divvybikes.com/data-license-agreement)._

### Process

In the data clean phase, I use the [R language](https://github.com/CJYen/Google-Data-Analytics-Capstone) to clean up the null values and unnecessary data. Since the limitation of my computer, I decided to export the clean data sets for further inspection. But this is not a necessary step for everyone.

### Analyze

It would be much convenient to identify data when converting the raw data into months, weeks, and riding length for further analysis. I use the [R language](https://github.com/CJYen/Google-Data-Analytics-Capstone) to do so. Again, export the final data is an option that benefits those who lack of Memory(RAM), just like me.

### Share

The proportion of users in the last year, the majority are members. Casual users are approximately half of the number of members.
![pic1](/posts/01_ridership.png)

_The riding time between the casual users and members; members highly use than casual users._

Regardless of members or not, the peak months starting from June to October can be considered a reasonable time for the campaign.
![pic2](/posts/02_traffic-by-month.png)

It is more average of members' riding during the week. Casual users are preferred riding on holidays. It can be considered a good time to do a special promotion to attract them to sign up as members.
![pic3](/posts/03_traffic-by-ridership.png)

Unlike members who commute between offices, casual users are more likely located around harbors in terms of sites usage. Another campaign can be a one-day ticket or two-day ticket of promotions for them to sign up.
![pic4](/posts/04_traffic-by-station.png) 




Members are more likely to ride classic bikes, which can leverage the number of bike types as the adjustment ratio in the future needs.
![pic5](/posts/05_ride-type-by-week.png) 

_Ps. All Viz can be found on [Tableau](https://public.tableau.com/views/Cyclistic_Bike/StationTraffic?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)_



### Act

To summarize, all possible campaign suggestions are:
1. Promote according to the popular months, and put on advertising.
2. Promote the two-day ticket or time-reward membership program to attract sign-up for members during the holiday period.
3. Follow-up suggestions can be plans survey to understand their choice between classic bikes and electronic bikes.