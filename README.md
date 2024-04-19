# Youtube_project
link to the powerpoint: https://www.canva.com/design/DAGCh0RurZU/BuKYAyPxaHtSFtJa68C3Eg/edit?utm_content=DAGCh0RurZU&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton
An analysis of Youtube trending videos across three different nations, the United States, England, and Canada. 
The questions we sought to answer were 'How trends very across different regions or categories?' and 'What is he average engagement for trending Youtube videos?'

Link to our presentation: https://www.canva.com/design/DAGCh0RurZU/BuKYAyPxaHtSFtJa68C3Eg/edit?utm_content=DAGCh0RurZU&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

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

## Trending Topics Across the Regions
Our second hypothesis: Audiences engage more with the Entertainment, Music, and Autos & Vehicles categories of YouTube videos than any other category of videos across different regions. From the data we pulled and stored into a CSV file, we created pie charts of the breakdown of the video categories for all three regions. The images below show the breakdown for each region.

![UK_pie](https://github.com/sophiagemanuel/Youtube_project/assets/161385170/0d559ed6-32fe-4bc8-8dd1-c15138d8e946)

![CA_pie](https://github.com/sophiagemanuel/Youtube_project/assets/161385170/9b3142e1-9f7c-4714-a31a-313af1fdbdd7)

![US_pie](https://github.com/sophiagemanuel/Youtube_project/assets/161385170/a8480717-29d0-4ca4-bc05-c7b5b110e1d3)

Users in the UK and the US have more interest in Sports and in Science & Technology, while users in Canada are more interested in Music and vlogs as those categories take up almost half of what is trending. It also tells us that the users in UK have a more diverse interest as their trending videos span across 13 different categories, while the US's and Canada's only has 10 and 11 different categories respectively.

Here is a grouped bar chart showing the number of videos of different categories in trending for each region. The pink, blue, and green represents UK, Canada, and the US respectively.

![grouped_bar](https://github.com/sophiagemanuel/Youtube_project/assets/161385170/4a5d7eb5-761e-4b9e-af8f-49c55ce104fc)

From this chart, it seems that there's a lot more Entertainment videos in trending for UK, while Canada prefers Gaming and Music videos, and the US prefers Sports.

## Video Length and Views
Additionally, we were interested to see if the video length affected user interest, leading it to result to being on the Trending page. We made several scatterplots comparing the Video lengths and View counts overall and in each region.

![video_length_vs_views](https://github.com/sophiagemanuel/Youtube_project/assets/161385170/64a28475-53ca-4e66-b2df-20df35e4e50d)

The correlation coefficient between video length and views overall is -0.16. Thus, there is a weak negative correlation between video length and views.
That means there is a slight tendency for views to decrease as video length increases. Similarly for each region.

![UK_scatter](https://github.com/sophiagemanuel/Youtube_project/assets/161385170/477fb84d-8838-4905-864e-2b12bcbde57a)

![CA_scatter](https://github.com/sophiagemanuel/Youtube_project/assets/161385170/961fe7de-337f-4ef9-be0f-b859c6f90bf3)

![US_scatter](https://github.com/sophiagemanuel/Youtube_project/assets/161385170/ccf3147b-2835-4824-a894-b96b1f7ed60c)

## Statistical Anomalies and Outliers

In the date range that we pulled the data from, there were many live, current events being broadcast that were Trending on YouTube such as Coachella, where view count and comment count information was unavailable for certain videos.

Therefore, we concluded that this information might have affected the view count and engagement values that we collected from the United States region.

Additionally, we examined the data further to identify if any outliers might help prove or disprove our hypothesis.

We then conducted further analysis to find if there are any significant outliers that we have to consider that may impact our conclusions.

Although we were able to find outliers in all three regions, these outliers did not provide any significant information that would lead us to reject the conclusions we arrived at previously.

![download](https://github.com/sophiagemanuel/Youtube_project/assets/161780046/6dbb251f-0baa-4e0d-b0ca-b14816dbdb8c)

## Final Analysis

Our first hypothesis was disproved because we were unable to find a significant statistical difference between the views and engagements of US trending videos when compared with UK and Canada.

There was enough statistical evidence to suggest that we fail to reject our null hypothesis, as p-values were greater than 0.05 for all our statistical comparisons.

In our second hypothesis, we were able to collect data that provided significant evidence that proved the YouTube trending audience had higher engagements and views with Entertainment and Music categories.

Music and Entertainment accounted for approximately 38% of the total viewership of the Canadian YouTube trending audience and approcimately accounted for 20% of viewership in the US region,
but we could not find enough evidence to suggest that the audience engaged with the Automobiles category of videos on YouTube.

Therefore, some arguments in our second hypothesis had to be rejected or were unproven

We were also able to identify the unique preferences of the YouTube audience when we examined engagements/views of UK, US, and Canada individually.

In our analysis, we were able to identify that the US audience engaged more with Science/Technology (18.4%), Comedy (24.5%), and Sports (14.3%),

UK audience engaged with Science/Technology (16%), Sports (24%), and People/Blogs (16%),

Canadian audiences engaged with Music (24%), People/Blogs (24%), and Entertainment (14%).

We were able to identify similar and different interests of the English-speaking YouTube audience:

US and UK audience is highly engaged with Science/Technology and Sports content and Canada and UK audience is engaged with People & Blogs. 

We also tried to identify any correlation trends in viewer engagement and video length, but statistical analysis did not find a significant correlation between video length and viewer engagement.
We did find that as the video length increases, views decreased

We were able to identify the following trends and come to these conclusions
1. There is no significant statistical difference between viewership and engagement of UK, US, and Canadian YouTube trending audiences.
2. Entertainment and Music, Science and Technology, and People and Blogs are the most popular categories on YouTube trending across the UK, the US and Canada.
3. Canadian and UK audience has higher engagements with the People & Blogs category of videos.
4. UK and US audiences engage more with Sports, Science and Technology.
5. As video length increases, there is a higher probability that the views decrease.






