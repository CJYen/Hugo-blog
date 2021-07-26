---
title: "Cyclistic Bike-Share Analysis"
date: 2021-07-26T19:09:09+08:00
---

### Quick Intro

I have been working on the Google Data Analytics Professional Certificate course in Coursera for the last two months. This case study is to verify the eight steps of data clean-analyst learned in this series.

In this scenario, I'm a junior data analyst working in the marketing analyst team at Cyclistic, a fictional bike-share company based in Chicago. The marketing team is trying to design a marketing campaign that can convert casual riders to annual members. The goal is to find out their usage behavior to increase the conversion rate of their members.

Before starting the task, I need to check the leader's problem first:

1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?

Based on the above problems, we can have the following plan and behavior.

### Ask

Before starting the task, I need to check the leader's problem first:

1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?

Based on the above problems, we can have the following plan and behavior.

### Prepare

First, how to find out member behavior? The data shows the date and time of the user's use, the site, and the type of vehicle used.

To determine the difference between dates they use, site difference, and the length distinction between users. You can infer the peak riding period from the dates they use to facilitate marketing follow-up promotions.

Which stations have high traffic? This allows marketing to follow up to understand whether there is a need to adjust and promote.

And, is there any difference in membership usage for their weekly usage? Also, is there any difference in the length they use?

Finally, what is their habit of using models? Maybe it can provide follow-up adjustment and distribution.

With this information, it may be possible to develop a suitable plan to help convert members.

表格
 No | Column             | Description
 ---|--------------------|------------
 1  | ride_id            | Unique identifier of each ride
 2  | rideable_type      | Type of bike (classic, electric)
 3  | started_at         | Timestamp of when a ride started
 4  | ended_at           | Timestamp of when a ride ended
 5  | start_station_name | Name of docking station where a ride started
 6  | start_station_id   | ID of docking station where a ride started
 7  | end_station_name   | Name of docking station where a ride ended
 8  | end_station_id     | ID of docking station where a ride ended
 9  | start_lat          | Latitude at the start of a ride
 10 | start_lng          | Longitude at the start of a ride
 11 | end_lat            | Latitude at the end of a ride
 12 | end_lng            | Longitude at the end of a ride
 13 | member_casual      | Whether user is a member or a casual rider

_Ps. We download the data according to the data license agreement._

### Process

In the data clean phase, I use the R language to process the data with null and error values and then transfer it to clean data. Because of the limitation of my computer, I choose to export the data first for subsequent use; if there is no such limitation, this step is unnecessary.

### Analyze

Next, for the convenience of analysis, continue to use the R language to convert the data into month and week; to convert the length of riding time.

### Share

Last year, the proportion of users was temporarily the majority of members, and the number of non-members is about more than half of the number of members. (This is still without considering repeated users)
![pic1](/posts/01_ridership.png)

Regardless of member or not, the peak month is from June to September, when it is warmer, so the campaign can be considered at this time.
![pic2](/posts/02_traffic-by-month.png)

During the week, the usage of members is more average, while casual is concentrated on holidays. Consider promoting a special time to attract members.
![pic4](/posts/04_traffic-by-ridership.png)

In terms of site usage, members use more averagely during casual users go coastal attractions as the majority. It is possible to consider this, and most of the casual users are tourists. Another campaign can be promoted, a one-day ticket or a two-day ticket, an unlimited time riding plan.

Member             |  Casual
:-------------------------:|:-------------------------:
![pic5](/posts/05_traffic-by-station.png "title-1")  |  ![pic6](/posts/06_traffic-by-station.png "title-2")


Then there is the car type. Most members ride classic, so you can deploy the site later; for non-members, the car type usage is more balanced except for holidays. Only on holidays, more classic rides, follow-up. Maybe you can make a questionnaire to help understand why they have differences in usage.
Member             |  Casual
:-------------------------:|:-------------------------:
![pic7](/posts/07_ride-type-by-week.png)  |  ![pic8](/posts/08_ride-type-by-week.png)

The last is the weekly usage rate. The average riding time of members is about 20 minutes, while the casual is approximately 40-50 minutes. Therefore, you can consider setting up a membership project to give back time to attract membership.
![img_alt_you_want_to_control](/posts/09_average-time.png)


### Act

In summary, the possible follow-up campaign suggestions are:

1. Promote according to the more popular months, and put on relevant advertising.
2. Use the holiday period to promote the two-day coupon or time-reward membership system to attract membership.
3. Follow-up questions can be planned to understand why they choose classic models in the majority.