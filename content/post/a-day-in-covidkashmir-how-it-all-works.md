---
title: A Day in CovidKashmir - How it all works?
images: 
 - /images/ck-blog2.jpg
date: 2020-07-29T11:03:45.308Z
description: To update our website, we rely on two sources only, Daily Media
  Bulletins and News Reports in various newspapers. The media bulletin comes out
  only once a day (or sometimes twice) and contains a lot of data that we have
  to update. On the other hand, news reports can come out at any time during the
  day but usually, we have to update the live statistics only with that data.
  The two sources trigger different workflows, and I will divide this article
  into two sections, each detailing a workflow.
author: haideralipunjabi
---
To update our website, we rely on two sources only, Daily Media Bulletins and News Reports in various newspapers. The media bulletin comes out only once a day (or sometimes twice) and contains a lot of data that we have to update. On the other hand, news reports can come out at any time during the day but usually, we have to update the live statistics only with that data. The two sources trigger different workflows, and I will divide this article into two sections, each detailing a workflow.

**News Reports**

I read the news reports published in newspapers every morning as they contain the most detailed account of cases announced / deaths occurred during the previous day. This data mostly adds to the data we have in the Patient Details sheet on Google Sheets. I look for details like age, gender, locality, etc that aren’t available in the daily bulletin. Sometimes, information about deaths which occur during the night is also present, which I add to the Live Statistics data on Github Gists.

During the rest of the day, news reports about deaths, recoveries and new cases are published which I add to the Live Statistics. A lot of news reports about new cases and recoveries used to be published in March - April but they stopped when the cases began increasing much faster. Nowadays (July), news reports are mostly about deaths that occur due to the pandemic.

After adding the data to the Live Statistics, I take a screenshot of the Live Statistics section on our website. I share this screenshot with the details of the update to our Whatsapp Group. From there, it is shared to our pages on various social media. Also, I send out Push Notifications to everyone who has subscribed to it.

**\
Daily Media Bulletin**

The Bulletin is published on [DIPRJK’s Twitter Account](https://twitter.com/diprjk) once (or sometimes twice) a day. This bulletin contains various statistics and district level details about the pandemic in J&K. I first update the main statistics in our Media Bulletin Sheet and then send a message in our group that the bulletin update is done. These statistics are shown on the Sample Statistics section of our website and are used by Vikas to create the Daily Overall Statistics Graphic. Vikas shares the graphic image to the group when he is done, and we share it to various social media sites. I also update the District Data and Patient Details sheets. After the update to Google Sheets is done and published, I compare the district table on our website (which uses the District Data Sheet) to the Media Bulletin so that errors can be removed. I then use a collection of scripts (Python & Bash) that I have made to make 12 (I started with 9, and they might increase in the future) different visualisations based on the District Data Sheet. The visualisations include Total, Active, Recovered and Deceased Cases map along with their “per million” variants. Along with those, New Cases, Recoveries, and Deaths that were added. The last visualisation contains line charts of all the districts visualising the change in Total, Active, Recovered and Deceased Cases since April 11. Due to the size of the images, I upload the visualisations myself to every social media site.

**Future**

The workflow has been the same ever since we started, and I don’t see it changing anytime in the future. The only thing that has changed and might change is the amount of automation I am using. The amount of data entry I had to do daily has reduced a lot, and I am hoping to automate a bit more. I will be writing one or more articles regarding the scripts I have made to make the visualisations and help me in data entry.