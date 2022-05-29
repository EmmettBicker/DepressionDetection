# Good Health and Well Being: Screening for Depression on Twitter
# Using a Sentiment Analysis Neural Network

 Emmett Bicker


**Motivation**

Many of my friends displayed symptoms of depression after the COVID-19 pandemic began and schools switched to remote learning. I am unaware if any of them received help, but I noticed my friends were also displaying depressive symptoms on social media platforms such as Discord, Reddit, and Twitter. Only ⅓ of those with depression ever seek out help while ⅔ of the depressed population suffer undiagnosed.[^1] Studies have shown remote learning to increase students’ anxiety and depression.[^2] Depression, most prevalent in adolescents, has become more widespread due to COVID-19. A late 2020 national survey reported that 17.0% of all U.S. children aged 12-17 have had a major depressive episode, 12.0% have seriously considered suicide, and 2.5% attempted suicide in the past year. If depression is detected early, complications such as substance abuse, self-harm, and suicide can be prevented.[^3]

**Overview**

The change I noticed in my friends' social media behavior and the rise in depression inspired me to make a depression detector for social media. The project I made was a sentiment analysis depression screener, in which my program would analyze a tweet and output if the tweet showed signs of depression. My program, *Are You Sad?*, then does this for up to the last 2500 tweets a user has posted and graphs the change in their mental health over the past few years. The product will be free as I want everyone to have the ability to screen their loved ones for mental health issues. While I made the project with high schoolers affected by COVID-19 in mind, the final product can be used to graph anyone's emotional state over time. Twitter is a good social media to screen for depression because 85% of Twitter users are under the age of 50,[^4] and 83% of people who suffer from depression are under 50.[^5] It can also be used by community volunteers and non medically trained staff to detect depression in areas that are often overlooked in developing countries, such as postpartum depression, which can be treated if correctly identified early on.[^6]

**Ethics**

The ethical concerns the mentors and I identified were the risks of wrong diagnosis and privacy. I plan to present my project as a screening tool and not a diagnostic test, making it explicit in the distribution that this is the first step in a depression diagnosis, not a definitive verdict. In order to mitigate the privacy concerns, I will continue to only analyze tweets users choose to post on their accounts and will not record habitual information and data. When analyzing private accounts, I plan to have the screener use the Twitter API functionality to log in with their own Twitter account; the screener can only screen private accounts they have been given access to. Finally, in order to minimize the chance of missing cases, I plan to maximize recall in the project’s future.

**Program**

When programming the tweet screening, I first began by determining which features to extract from each tweet. I created four word clouds from the most common words and the most common hashtags found in healthy tweets and depressed tweets (fig 1). I used these word clouds to create features of the occurrences of the 354 most common keywords and hashtags found in healthy and depressive tweets. Afterward, I added features such as character and word length for longer sentences, links, and punctuation which are indicators of a healthy or depressive tweet. Once I had the features I wrote a function to extract all the features from a tweet and perform feature normalization.
    I used a feed-forward neural network to train my data because its simplicity fit a two-day hackathon and also because this is my first python machine learning project. Another reason I used a neural network was because of its ability to map correlation between features; because of the different meanings of different words in different contexts, all the features are highly correlated so a neural network would be good to use. Once I’d trained the network I achieved a 92.75% accuracy on the test set! After programming a depression detector for a single tweet, I then used Tweepy and a Twitter developer account to write a program to get the last couple thosuand tweets from a user and graph their emotional state over time.
  
**Future Plans**

Looking forward, I plan to develop a web app UI for my project which will make my application more accessible to the global population. I’ll also develop profile picture and image post analysis as that has been proven to be able to detect depression.[^7] I’d like to expand into different social media, like Instagram, Snapchat, and TikTok, and add languages, and I would like to collect my own data for this. The dataset I’m currently using only has messages that clearly indicate depression and I would like to collect new data that considers disguised depressed speech. I would also like to get a grant to hire researchers to identify more features indicative of depressed tweets and to hire people to collect data.

[^1]: Kate Wichmann. "People suffering from depression not getting the help they need." Dec 3, 2014. Video Testimonial, 1:20. https://www.youtube.com/watch?v=J-pgdjguTjA. 

[^2]: Suzanne Lischer, Netkey Safi, and Cheryl Dickson. Remote learning and students’ mental health during the Covid-19 pandemic: A mixed-method enquiry. Nature Public Health Emergency Collection, Jan 5, 2021.

[^3]:“Depression (Major Depressive Disorder),” Mayo Clinic (Mayo Foundation for Medical Education and Research, February 3, 2018), https://www.mayoclinic.org/diseases-conditions/depression/symptoms-causes/syc-20356007. 

[^4]: “Top Twitter Demographics That Matter to Social Media Marketers,” Hootsuite (Hootsuite Inc., July 14, 2020), https://blog.hootsuite.com/twitter-demographics/. 

[^5]: “Major Depression,” National Institute of Mental Health (U.S. Department of Health and Human Services, 2021), https://www.nimh.nih.gov/health/statistics/major-depression. 

[^6]: Baranov, Victoria. "The power of treating mothers' depression in developing countries." Mar 5, 2020. Video Testimonial, 1:51. https://www.youtube.com/watch?v=H7Y7RQko2Wg. 

[^7]: Andrew G Reece, Christopher M Danforth. Instagram photos reveal predictive markers of depression. EPJ Data Science, Aug 8, 2017.

[Dataset]: Garg, Manas. Sentimental Analysis for Tweets. May 29, 2021. https://www.kaggle.com/datasets/gargmanas/sentimental-analysis-for-tweets. 

