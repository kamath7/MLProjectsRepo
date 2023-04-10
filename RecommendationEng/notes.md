Two types of filtering

User Based Collaborative Filtering
Item based collaborative filtering


### User Based Collaborative Filtering


User-based collaborative filtering is a recommendation technique that predicts a user's preferences by finding similar users and recommending items that these similar users have liked or rated highly. The idea behind this approach is that users who have similar preferences in the past are likely to have similar preferences in the future.

To implement user-based collaborative filtering, the system first gathers information about users' preferences, such as ratings they have given to various items or products. Then, it uses this information to build a similarity matrix that identifies how similar each pair of users is based on their preferences. This similarity matrix can be computed using different techniques, such as cosine similarity or Pearson correlation.

Once the similarity matrix is built, the system can use it to make recommendations for a given user. To do this, the system identifies users who are most similar to the target user, based on their preferences, and recommends items that these similar users have liked or rated highly, but that the target user has not yet seen or interacted with.

One challenge of user-based collaborative filtering is that it requires a significant amount of data about users' preferences to be effective. This means that the system may not work well for new users or users with sparse data. Additionally, the system may suffer from the "cold start" problem, where it is difficult to make recommendations for new items or products that have not yet been rated or liked by any users.


### Item Based Collaborative filtering



