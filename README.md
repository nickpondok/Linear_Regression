### Abstract
The goal of this project was to create a linear regression model that attempted to predict an NBA player's salary based on their performance statistics. Data was pulled from 3 different sources. Basketball-reference provided the statistical data, ESPN provided the yearly salary data, and Spotrac provided the contract data. All data was combined and cleaned to start the model. A cross validation with 5 kfolds was performed, and a test group was held out as well. A Ridge Regression model was used which resulted in an average r^2 of .58622 and a RMSE of ~35 million. Experience proved to be the biggest factor when determining salary. 

### Design
Our client Klutch Sports is asking us to perform this analysis in order for them to include it in their training material for new agents. The idea being it will help them understand the trends of current salaries and what factors into a big contract. Additionally it will be information they could pass along to clients (NBA Players) to let them know what areas they need to improve on if they want to increase their pay. 

### Data
Data was pulled from three different websites. All sites were web scraped using beautiful soup. Spotrac.com provided the contract data. This included the length of the contract (i.e 3 years) as well as the year it expired. With this information we were able to determine what year the contract was signed. Since prior performance statistics are what lead to a new contract, I only took into account performance statistics prior to the year their contract was signed. For example, if a player signed their contract in 2018, then performance statistics from 2019-2020 were not added into the data. We used beautiful soup to webscrape basketball-reference for performance statistics. Lastly the yearly salaries were pulled from the ESPN website. After some additional cleaning and adjustments for outliers, the final data set came out to 1,276 pieces of data. 

### Algorithms 
A simple ridge regression was used with cross-validation. The hope here was to highlight the coefficients that had the most significance. Additionally their was worry for colinearity, so I wanted to account for that as well. The metrics I used to asses my model were R-Squared and Root Mean Squared Error. 

Final random ridge 5-fold CV 

Average R-Squared - 0.6056402841022513

Holdout

R-Squared - 0.586228925728601
RMSE = 3.5969711e+7

### Tools 
Beaitiful Soup for webscraping
Pandas and Numpy for data manipulation
Scikit-learn for modeling 
Matplotlib and Seaborn for plotting
    
