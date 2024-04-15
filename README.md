# Youtube_project
An analysis of Youtube trending videos across three different nations, the United States, England, and Canada. 
The questions we sought to answer were 'How trends very across different regions or categories?' and 'What is he average engagement for trending Youtube videos?'

We found our information by using the Youtube api (https://developers.google.com/youtube/v3/getting-started) and generating the information regarding audience engagement with the top trending 50 videos of each region.We collected the information on the video's title, id, category, views, likes, comments, and duration. From this, we stored the information of each video into a CSV file for each region. 
First we tested the hypothesis of: The United States has higher viewership and engagement (likes/comments) on average when compared with Canada and United Kingdom, comparing it to the null hypothesis of: There is no significant differences between viewership and engagement (likes/comments) across each nation. To do this, we found the statistic measures of views and comments accross the United States (US), England (GB), and Canada (CA). We then stored these into a dataframe for each country. 

We found our information by using the Youtube api (https://developers.google.com/youtube/v3/getting-started) and generating the information regarding audience engagement with the top trending 50 videos of each region. We collected the information on the video's title, id, category, views, likes, comments, and duration. From this, we stored the information of each video into a CSV file for each region. 

First we tested the hypothesis of: The United States has higher viewership and engagement (likes/comments) on average when compared with Canada and United Kingdom, comparing it to the null hypothesis of: There is no significant differences between viewership and engagement (likes/comments) across each nation. To do this, we found the statistic measures of views and comments accross the United States (US), United Kingdom (GB), and Canada (CA). We then stored these into a dataframe for each country. 
Then we created our first chart: Comparing the Mean Value of Views Across Regions. This chart shows the views in milions on the x-axis, and the country on the y-axis. By looking at this chart, the United Kingdom had a higher mean of views per video, then Canada, then the United States.

![image](https://github.com/sophiagemanuel/Youtube_project/assets/157437098/45175710-f283-43c6-bd05-90d54b3bf636)

Then we created our second chart: Comparing the Mean Value of Commentss Across Regions. This chart shows the comments in the thousands on the x-axis, and the country on the y-axis. By looking at this chart, Canada had a higher mean of comments per video, then United Kingdom, then the United States.

![image](https://github.com/sophiagemanuel/Youtube_project/assets/157437098/d5d16369-7c87-494b-92f9-34f201e9fa7d)

Although by looking at the charts, it seems like there was a significant difference, we needed to check by preforming an independent T-test comparing the views and comments United States to Canada and the United Kingdom.
From this we gained the results:

T-test Results for CA and US Viewership:
T-statistic: -1.169017780466276
P-value: 0.24710003583582768

------------------------------
T-test Results for CA and US Comments:
T-statistic: -0.9545805792677698
P-value: 0.34329817086704695

------------------------------
T-test Results for GB and US Viewership:
T-statistic: -1.6835531897024303
P-value: 0.09764031281841963

------------------------------
T-test Results for GB and US Comments:
T-statistic: -0.8199059877464244
P-value: 0.4152082658263955

------------------------------

When looking at the P-value of all the results, all of them are greater than 0.05. Thus we fail to reject the null hypothesis. This means that there is no significant difference between viewership engagement.
