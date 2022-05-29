> **Good Health and Well Being: Screening for Depression on Twitter
> Using a Sentiment Analysis Neural Network**

Emmett Bicker

> Many of my friends displayed symptoms of depression after the COVID-19
> pandemicbegan and schools switched to remote learning. I am unaware if
> any of them received help, but I noticed my friends were also
> displaying depressive symptoms on social media platforms such as
> Discord, Reddit, and Twitter. Only ⅓ of those with depression ever
> seek out help while ⅔ of the depressed population suﬀer
> undiagnosed.1Studies have shown remote learning to increase students'
> anxiety and depression.2Depression, most prevalent in adolescents, has
> become more widespread due to COVID-19. A late 2020 national survey
> reported that 17.0% of all U.S. children aged 12-17 have had a major
> depressive episode, 12.0% have seriously considered suicide, and 2.5%
> attempted suicide in the past year. If depression is detected early,
> complications such as substance abuse, self-harm, and suicide can be
> prevented.3\
> The change I noticed in my friends\' social media behavior and the
> rise in depressioninspired me to make a depression detector for social
> media. The project I made was a sentiment analysis depression
> screener, in which my program would analyze a tweet and output if the
> tweet showed signs of depression. My program, *Are You Sad?*, then
> does this for up to the last 2500 tweets a user has posted and graphs
> the change in their mental health over the past few years. The product
> will be free as I want everyone to have the ability to screen their
> loved ones for mental health issues. While I made the project with
> high schoolers aﬀected by COVID-19 in mind, the ﬁnal product can be
> used to graph anyone\'s emotional state over time. Twitter is a good
> social media to screen for depression because 85% of Twitter users are
> under the age of 50,4and 83% of people who suﬀer from depression are
> under 50.5It can also be used by community volunteers and non
> medically trained staﬀ to detect depression in areas that are often
> overlooked in developing countries, such as postpartum depression,
> which can be treated if correctly identiﬁed early on.6\
> The ethical concerns the mentors and I identiﬁed were the risks of
> wrong diagnosisand privacy. I plan to present my project as a
> screening tool and not a diagnostic test, making
>
> 1 Kate Wichmann. \"People suffering from depression not getting the
> help they need.\" Dec 3, 2014. Video Testimonial, 1:20. .
>
> 2 Suzanne Lischer, Netkey Safi, and Cheryl Dickson. Remote learning
> and students' mental health during the Covid-19 pandemic: A
> mixed-method enquiry. Nature Public Health Emergency Collection, Jan
> 5, 2021.
>
> 3 "Depression (Major Depressive Disorder)," Mayo Clinic (Mayo
> Foundation for Medical Education and Research, February 3, 2018), .
>
> 4"Top Twitter Demographics That Matter to Social Media Marketers,"
> Hootsuite (Hootsuite Inc., July 14, 2020), .
>
> 5 "Major Depression," National Institute of Mental Health (U.S.
> Department of Health and Human Services, 2021), .
>
> 6Baranov, Victoria. \"The power of treating mothers\' depression in
> developing countries.\" Mar 5, 2020. Video Testimonial, 1:51. .

+----------------------+----------------------+----------------------+
| ![](vertopal_61a95e8 | ![](vertopal         | > it explicit in the |
| 0f36844dcb98d3c1e2c5 | _61a95e80f36844dcb98 | > distribution that  |
| 4c8b9/media/image1.p | d3c1e2c54c8b9/media/ | > this is the ﬁrst   |
| ng){width="1.4375in" | image2.png){width="1 |                      |
| height="1.           | .4361100174978128in" |                      |
| 4263877952755906in"} | height="1.           |                      |
|                      | 4055555555555554in"} |                      |
+======================+======================+======================+
|                      |                      | > step in a          |
|                      |                      | > depression         |
|                      |                      | > diagnosis, not a   |
|                      |                      | > deﬁnitive          |
+----------------------+----------------------+----------------------+
|                      |                      | > verdict. In order  |
|                      |                      | > to mitigate the    |
|                      |                      | > privacy            |
+----------------------+----------------------+----------------------+
|                      |                      | > concerns, I will   |
|                      |                      | > continue to only   |
|                      |                      | > analyze tweets     |
+----------------------+----------------------+----------------------+
|                      |                      | > users choose to    |
|                      |                      | > post on their      |
|                      |                      | > accounts and will  |
+----------------------+----------------------+----------------------+
|                      |                      | > not record         |
|                      |                      | > habitual           |
|                      |                      | > information and    |
|                      |                      | > data. When         |
+----------------------+----------------------+----------------------+
|                      |                      | > analyzing private  |
|                      |                      | > accounts, I plan   |
|                      |                      | > to have the        |
+----------------------+----------------------+----------------------+
| > ![](vertopal       | > screener use the   |                      |
| _61a95e80f36844dcb98 | > Twitter API        |                      |
| d3c1e2c54c8b9/media/ | > functionality to   |                      |
| image3.png){width="3 | > log                |                      |
| .0305555555555554in" |                      |                      |
| > height="0.         |                      |                      |
| 3236111111111111in"} |                      |                      |
+----------------------+----------------------+----------------------+
|                      | > in with their own  |                      |
|                      | > Twitter account;   |                      |
|                      | > the screener       |                      |
+----------------------+----------------------+----------------------+

> can only screen private accounts they have been given access to.
> Finally, in order to minimize the chance of missing cases, I plan to
> maximize recall in the project's future.
>
> When programming the tweet screening, I ﬁrst began by determining
> which features toextract from each tweet. I created four word clouds
> from the most common words and the most common hashtags found in
> healthy tweets and depressed tweets (ﬁg 1). I used these word clouds
> to create features of the occurrences of the 354 most common keywords
> and hashtags found in healthy and depressive tweets. Afterward, I
> added features such as character and word length for longer sentences,
> links, and punctuation which are indicators of a healthy or depressive
> tweet. Once I had the features I wrote a function to extract all the
> features from a tweet and perform feature normalization.
>
> I used a feed-forward neural network to train my data because its
> simplicity ﬁt atwo-day hackathon and also because this is my ﬁrst
> python machine learning project. Another reason I used a neural
> network was because of its ability to map correlation between
> features; because of the diﬀerent meanings of diﬀerent words in
> diﬀerent contexts, all the features are highly correlated so a neural
> network would be good to use. Once I'd trained the network I achieved
> a 92.75% accuracy on the test set!
>
> My algorithm is diﬀerent from standard depression sentiment analysis
> because it takesadvantage of Twitter's ways of expressing sentiment
> such as hashtags which aren't able to be taken into consideration with
> standard sentiment analysis.
>
> Looking forward, I plan to develop a web app UI for my project which
> will make myapplication more accessible to the global population. I'll
> also develop proﬁle picture and image post analysis as that has been
> proven to be able to detect depression.7I'd like to expand into
> diﬀerent social media, like Instagram, Snapchat, and TikTok, and add
> languages, and I would like to collect my own data for this. The
> dataset I'm currently using only has messages that clearly indicate
> depression and I would like to collect new data that considers
> disguised depressed speech. I would also like to get a grant to hire
> researchers to identify more features indicative of depressed tweets
> and to hire people to collect data.
>
> Depression is a rampant issue globally which has only been made worse
> by theCOVID-19 pandemic. My screener will be a useful tool to get
> people the help they need.
>
> 7 Andrew G Reece, Christopher M Danforth. Instagram photos reveal
> predictive markers of depression. EPJ Data Science, Aug 8, 2017.

Bibliography

> Baranov, Victoria. \"The power of treating mothers\' depression in
> developing countries.\" Mar 5,
>
> 2020\. Video Testimonial, 1:51. .
>
> "Depression (Major Depressive Disorder)," Mayo Clinic (Mayo Foundation
> for Medical
>
> Education and Research, February 3, 2018),
>
> .
>
> Garg, Manas. Sentimental Analysis for Tweets. May 29, 2021.
>
> .
>
> Lischer, Suzanne, Netkey Saﬁ, and Cheryl Dickson. Remote learning and
> students' mental
>
> health during the Covid-19 pandemic: A mixed-method enquiry. Nature
> Public Health
>
> Emergency Collection, Jan 5, 2021.
>
> "Major Depression," National Institute of Mental Health (U.S.
> Department of Health and
>
> Human Services, 2021), .
>
> Reece, Andrew, and Christopher M Danforth. Instagram photos reveal
> predictive markers of
>
> depression. EPJ Data Science, Aug 8, 2017.
>
> "Top Twitter Demographics That Matter to Social Media Marketers,"
> Hootsuite (Hootsuite Inc.,
>
> July 14, 2020), .
>
> Wichmann, Kate. \"People suﬀering from depression not getting the help
> they need.\" Dec 3,

2014\. Video Testimonial, 1:20. .
