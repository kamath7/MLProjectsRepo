Two types of filtering

User Based Collaborative Filtering
Item based collaborative filtering


### User Based Collaborative Filtering


User-based collaborative filtering is a recommendation technique that predicts a user's preferences by finding similar users and recommending items that these similar users have liked or rated highly. The idea behind this approach is that users who have similar preferences in the past are likely to have similar preferences in the future.

To implement user-based collaborative filtering, the system first gathers information about users' preferences, such as ratings they have given to various items or products. Then, it uses this information to build a similarity matrix that identifies how similar each pair of users is based on their preferences. This similarity matrix can be computed using different techniques, such as cosine similarity or Pearson correlation.

Once the similarity matrix is built, the system can use it to make recommendations for a given user. To do this, the system identifies users who are most similar to the target user, based on their preferences, and recommends items that these similar users have liked or rated highly, but that the target user has not yet seen or interacted with.

One challenge of user-based collaborative filtering is that it requires a significant amount of data about users' preferences to be effective. This means that the system may not work well for new users or users with sparse data. Additionally, the system may suffer from the "cold start" problem, where it is difficult to make recommendations for new items or products that have not yet been rated or liked by any users.


Simple Explanation - User-based collaborative filtering is like when you ask your friends what their favorite toys are and then pick toys that your friends like to play with that you haven't seen before. It's like making new friends who like the same things as you and asking them what they like, so you can find new things you might enjoy too!

### Item Based Collaborative filtering



Item-based collaborative filtering is a recommendation technique that suggests items or products to a user based on similarities between the items themselves. This means that the system looks at the items a user has already liked or rated highly and recommends other items that are similar to those the user has already shown interest in.

To implement item-based collaborative filtering, the system first gathers information about how users have rated or interacted with different items. Then, it uses this information to create a similarity matrix that identifies how similar each pair of items is based on how users have interacted with them. This similarity matrix can be computed using different techniques, such as cosine similarity or Jaccard similarity.

Once the similarity matrix is built, the system can use it to make recommendations for a given user. To do this, the system identifies items that are most similar to the ones the user has already liked or rated highly and recommends those items to the user. This means that the system can suggest items that the user may not have discovered on their own but are likely to be of interest to them based on their past behavior.

One advantage of item-based collaborative filtering is that it can work well even when there is limited data about individual users, as it relies on similarities between items rather than similarities between users. However, it may still suffer from the "cold start" problem when there is limited data available about new items or products that have not yet been rated or interacted with by users.

Simple Notes - Item-based collaborative filtering is like when you have a favorite toy, and your parents suggest other toys that are similar to your favorite one. They know that you like your favorite toy, so they suggest other toys that are like it that you might also like. It's like having a friend who knows what you like and helps you find other things that you might enjoy!