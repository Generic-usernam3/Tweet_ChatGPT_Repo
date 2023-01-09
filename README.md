## Background
On April 14th of 2022, Elon Musk announced to the world via his social media that he was initiating the process to acquire the social media giant, Twitter. One of the main concerns raised by Musk, the now CEO of Twitter, was the percentage and number of bots present in Twitter’s platform. Since then, the internet began debating the actual percentage of Twitter's mDAU, monetizable daily active users, who are bots. The percentage is estimated to be betwee 5% and 20%. A research study conducted by SimilarWeb determined that 20.8% and 29.2% of the content posted on Twitter was generated by bots, meaning that bots post x1.57 more content than a regular user.

Bots are defined as automated Twitter accounts that are programmed to behave like real Twitter users to achieve specific goals at a larger scale. Social media experts divide bots into two major categories: (a) “good” bots that provide useful content to users such as daily weather forecasts and stock prices, and (b) “bad” bots that spread misinformation, scams, span and devalue Twitter’s platform. The goal of this project is to detect a Twitter bot regardless of their activity on the platform. 

## Dataset
The main dataset in the Twitter Bot Detection Repository is the *Tweet_Repo.csv*, which contains approximately 7,000 data samples. The dataset is composed of real, original tweets written by verified Twitter users and bot-like Tweets generated by OpenAI's ChatGPT. It additionally indicates which label do each Tweet belongs to. The designed purpose of this dataset is to be used as training data for a model to detect original Tweets from bot-generated Tweets. These data samples were collected by our team through two data sources:
- Twitter - We used Twitter API to scrap off data from verified user and their tweets.
- ChatGPT - We asked ChatGPT to generate us a couple thousand tweets.

| Column Name | Description                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Text]      | Contains the text of the Tweets generated by both bots and real Twitter users. The text is not yet clean.                                                                   |
| [Type]      | Labels the source of the [Text] column as "Not a bot" if it was written by a real, verified Twitter user or "bot" if it was generated by ChatGPT assimilated a Twitter bot. |
We fine-tuned a bert model- the code is included in Final_Project.ipynb


Our fine-tuned model is available on the huggingface hub as : Generic-usernam3/Tweet_Chatgpt
