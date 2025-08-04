# Political Science Summer Research

This project is the output of the research I completed for Dr. Chris Chapp in the summer of 2023. Dr. Chapp had a manuscript which would become his book _Moral Issues: How Public Opinion on Abortion and Gay Rights Affects American Religion and Politics_ (cowritten with Paul Goren), but his election data extended only to the 2018 midterm elections. My task was to replicate these tables, with data updated from the 2020 and 2022 elections. 

The first task I had was to analyze news article, categorized by keywords into one of three categories: Taxes, Health, and Moral (Abortion and LGBT). To do this, I scraped data from online archives of the New York Times, Washington Post, and Associated Press. I combined this with similar data from Colin Harris, and successfully provided updated counts to Dr. Chapp. 

Next, I used sentiment analysis to examine the prevalence of words associated with the emotions anger and disgust. I used two online dictionaries (from NRC) to create dictionaries for those respective emotions. Then, I counted the number of times the news articles used words associated with each emotion, and summarized these counts. 

Finally, I examined text files scraped from the websites of 2022 major party nominees for the US House of Representatives. I computed the proportion of candidates with at least one section of their website discussing abortion or LGBT issues. A web page is determined to be focused on "moral issues" if more than 0.25% of its words are within Dr. Chapp's "moral" dictionary.

## Deliverables

I created four CSVs with the desired data: article counts over time from AP, NYT, and Washington Post, for each category; and summaries of the proportions of "anger" and "disgust"-coded words in articles in the Moral, Health, and Tax categories. 
These data can be found in _Article_Counts_2018_2023.csv_. 
For the Campaigns dataset, I calculated the proportions, for each party, of candidates with at least one "moral-focused" website section. For Democrats, 70.26316% of candidates had at least one webpage focused on a "moral" issue; however, only 44.11028% of GOP candidates had any section focused on a "moral issue". 

## Documents and CSVs Summary

For this project, I created five RMD files: _AP-Poli_Sci_Project.Rmd_, _NYTimes-Poli_Sci-Project.Rmd_, _WaPo-Poli_Sci_Project.Rmd_, _Sentiment Analysis.Rmd_, and _Campaigns.Rmd_. The first three RMD files process the news article data from their respective sources. _Sentiment Analysis.Rmd_ computes the proportion of "disgust"- and "anger"-coded words in these news articles. _Campaigns.Rmd_ computes these statistics for text documents of the webpages of 2022 congressional candidates, and additionally the proportions of candidates with "moral issue"-focused website pages. 

The NRC dictionaries _anger-NRC-Emotion-Lexicon.txt_ and _disgust-NRC-Emotion-Lexicon.txt_ were used for the sentiment analysis. 

The CSVs _Health_Articles.csv_, _Moral_Articles.csv_, and _Taxes_Articles.csv_ contain the cleaned and filtered text files for articles in the respective categories, from 2018 to 2023, from all three of the sources (Associated Press, Washington Post, and New York Times). 
_Full_Campaign_Dataframe.csv_ contains the scraped web pages from the 2022 US House major party nominees. 

## Packages

This research was performed in the ROAR server, on RStudio. We used the packages _rmarkdown_, _knitr_, _readtext_, _tidyverse_, _lubridate_, _data.table_, _rvest_, _tidytext_, _tm_, and _pdftools_.

## AI and Reproduction

© 2025 Matthew Blake, Christopher Chapp. All rights reserved.

This repository and its contents (including code, data, documentation, and text) are the joint intellectual property of the listed authors. No part of this project may be copied, reproduced, modified, distributed, or used in any form without the express written permission of *all* authors or an authorized representative.

This project is not open source. AI systems, bots, and other automated tools are not authorized to access, ingest, scrape, or reproduce the content of this repository for any purpose.
