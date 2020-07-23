---
title: The Stack behind CovidKashmir
# images: /images/ck-blog1.jpg
date: 2020-07-23T08:33:53.264Z
description: "Blog Post describing the stack and technologies behind CovidKashmir.org. "
author: haideralipunjabi
---
We had decided that the first blog post would be about how we run our daily operations but while writing that, I realised that I can’t write it properly without explaining the technological sides of the website.

When we started this website in March, the website was divided into two parts, a static frontend, and Google Sheets as the backend. Over the months, other small parts have been added to support the features that we created.

**The Frontend / Website**

Even though the website has grown a lot, it has seen minimal changes from a technical perspective. The frontend is made using HTML/CSS & Javascript and is hosted on Netlify. You can find the entire code in our Github Repository. We preferred using simple technologies instead of popular frameworks (like React, etc) due to two reasons.

1. To encourage contributions to the website from other people
2. To make development easier on 2G

The website, although static, fetches a lot of data from our backends. We use Netlify Functions to do a lot of data processing on the server, so that the website uses less data.

**The Backend**

We never made a proper backend since it’s costs would increase with the traffic our website was generating. We started storing our data on Google Sheets, and used to calculate the statistics from that. Later on, we moved the live statistics to Github Gists, as Google Sheets takes a few minutes to make the changes live.

Overall, the backend is divided into two parts:

1. Live Statistics Github Gist: A Github Gists which has a JSON of the following structure

```json
{
"Total": 15711,
"Active": 6825,
"Recovered": 8607,
"Deceased": 279,
"TotalYesterday": 15711,
"ActiveYesterday": 6829,
"RecoveredYesterday": 8607,
"DeceasedYesterday": 275,
"Updated": "23/07/2020 12:00pm"
}
```

2. Google Sheets: One workbook with multiple sheets for variety of data: Patient Details, District Level Data, Media Bulletin Data, Zone Classification, etc

**Python Scripts**

I am responsible for making daily visualisations and entering the data from the daily media bulletin to our Sheets backend. To make my job easier, I have multiple Python Scripts that automates a lot of my tasks. I am planning to write a seperate blog post about the various scripts I am using, but I will still list those here:

1. Scripts to delete old visualisations & create new ones.
2. Script to resize the visualisations for Instagram
3. Script to upload the visualisations to Twitter
4. Script that generates patients details based on input

I have been trying to create an OCR Script for the daily bulletin but the accuracy of my attempts hasn’t been that great.