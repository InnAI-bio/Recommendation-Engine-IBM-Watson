# IBM Recommendation Engine

## Dataset

We have 2 datasets here as user-item-interactions and article_community. The first dataset represents a user-article interaction, where we have the article_id, title of the article and the email associated with the event. For the privacy reason, the real email is replaced with the random generator. However, the event is still form the actual dataset. We have 45993 interactions from the dataset.

The second dataset contains information about the article's content. This includes document body, document description and its article id. We have 1051 article ids in the dataset. 


## Summary of Findings

In the exploration, I found that most users interact with less than 5 articles. Distribution follows the poisson distribution. From the data, the median of user-article interaction was 3. However, the maximum of user-article interactions could go up to 364. For the rank-based recommendations, since we did not have ratings associated with the interactions, the articles with most interactions were chosen as the top articles to recommend. For the user-user based collaborative filtering method, the similar users were found and the recommended articles are ordered by users with more engagement then articles with more interactions. Last, we implemented matrix factorization method to make articles recommendations to the users. We found there were many difficulties in using machine learning to predict the result since the class were unbalanced (interactions were mostly 0's) and the number of users we can predict in the test set were limited. We managed to obtain the accuracy score of 99.4 % with latent features of approximately 45.More interaction needed to be collected then we would be able to use cross-validation method to better access the model. We could also later perform hypothesis testing to assess whether the users with recommendation articles resulted in more interactions than the control group or not. 



## Key Insights & Acknowledgement


Since the user-article interaction only contains 0's and 1's it is difficult to assess the recommendation engine. We also have many users with 0's. This could indicate that these users are new or not engaing. The number of latent features were picked at the higest test and train score. We wanted to pick the model with the highest accuracy score but still able to account for dataset variance according to bias-tradeoff variance principles.Throughout this project, I want to acknowledge IBM Watson for providing the dataset and Udacity providing additional resources for the recommendation engine algorithms.
