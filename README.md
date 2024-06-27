# Anti-immigrant Attitudes in Russia: Understanding Determinants and Predicting Attitudes	 	

## Project description 

While Russia remains one of the largest immigrant-receiving countries, the case has received surprisingly little attention. The existing studies in migration literature tend to privilege cases of Western liberal democracies, the results of which might not be applicable to the context of Russia's hybrid regime. Furthermore, the existing studies on migration in Russia mostly focus on the socio-legal paradigms of its migration regime but tend to ignore public opinion and how it might reinforce policies. Finally, the studies that explore public attitudes often test only one theory, so it is hard to draw the relative importance of determinants that shape anti-immigrant attitudes. For example,
while it is known that xenophobic attitudes are more pronounced towards migrants with particular backgrounds, it seems unclear how these socio- cultural concerns can be compared to concerns regarding economic vulnerability or social welfare provision. Which ones are relatively more important? I attempt to determine the most important drivers of anti-immigrant
attitudes in Russia and predict them.

## Data 

I rely on Wave 7 (2017-2020) of the World Values Survey (WVS), which aims to measure people's values, beliefs, and norms through a comparative cross-
national and over-time perspective. The Wave 7 WVS dataset on Russia ontains 1810 observations and includes a wide range of variables. Since I am interested in attitudes towards migrants, I construct my binary dependent variable through the following question (Q121): "How would you evaluate the impact of these people [migrants] on the development of this country?"; where 1 stands for negative attitude while 0 for everything else. Since the missing values are not missing at random, I impute them using the K-nearest neighbor
model. I use the data for demographic and socio-economic variables as predictors. For convenience (when it comes to "greedy" approaches) I turn my predictors into binary variables, too, subdividing some of the variables. The dataset has 53 predictors.

## Methods
Previous studies relied on survey data using regression analysis, which tested only particular separate theories. Machine learning techniques should be useful in selecting determinants, understanding their relative importance, as well as predicting attitudes. 

Unsupervised learning: I use a principal component analysis (PCA) to reduce dimensionality and see common patterns in the data. The data is centered and scaled.

Supervised learning:  I create 12 models to identify the most important predictors as well as predict the attitudes:
Parametric: Logit, Ridge, Lasso, LDA
Non-parametric: kNN, tree-based (CART, Bagging, Random Forest, Boosting), support Vector Machines(linear, polynomial, radial).
