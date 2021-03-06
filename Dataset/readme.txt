2000 tweets per person.

Dataset:
link: https://drive.google.com/file/d/1FJiIl7QDe1K6U2gqZ_jdO3_8edHnO6TD/view?usp=sharing

About Dataset: 
FinalDataset.csv is the our final dataset which we have used in this project for training and testing our model. 
We obtained it after manually anotating and cleaning of the data. We used the Twitter API to collect the tweets corre- sponding to the hashtags which are trending. 
For that, we had to apply for a Twitter’s developer account which usu- ally takes weeks to be approved. We were asked about the project and about how we were going 
to use the collected data, once we replied to them about the details of our work, we got access to the public tweets. The tweets obtained had a lot of information 
along with the text, such as username of uploader, his/her followers and friends count, tweet time of
uploading, retweet information, location of tweet if available and many more. These tweets were used to create the data- set. Another challenge we faced was that 
there could only be 100 tweets extracted through the API. The tweets were manually annotated into categories of whether the tweet is hijacked or not. Our initial 
goal was to collect 10,000 tweets and annotate them to create out dataset. Since tweets can be subjective and it depends on the person whether he/she considers it 
to be hijacked or not, we followed a majority voting approach. Each of the tweet has been manually read and classified by each and every team member. Out of 5, if 
more than 2 members need to agree to classify a tweet hi- jacked. This way we removed opinionated bias. Moreover, there were numerous hashtags and their respective 
popular- ity’s were very dynamic. Ultimately we were able to create a dataset of 9470 samples.

The tweets were collected using Twitter API as men- tioned above and the tweets were retrieved as JSON objects and stored as .csv file. As some tweets had a few 
columns values as NaN or missing values, when these tweets were stored into a csv file, their column orders were skewed. For example: the User column entry actually 
got shifted to Geo coordinates columns. This had to be resolved by running a script to iterate over all the columns of the tweet to find the corresponding shifted 
values. Moreover, since the tweets were collected in batches over a duration of 4-5 days be- cause of the rate limit of twitter API, their format differed a bit. So 
the script for filtering out the relevant attributes for each batch of tweets varied a little. In the final dataset, we had just the columns named label, full-text, 
created at, screen name, followers count, friends count, retweets count, favorites count. The rest of the features were not relevant to our goal.
