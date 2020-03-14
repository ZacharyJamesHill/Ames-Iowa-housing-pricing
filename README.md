# Applications of Modeling Housing Prices

## Summary 
Ames Iowa is seeking to create a $900,000 low income housing development on 10 acres of land. Investment in housing is generaly more succesful long term is said housing is of reasonably high value. By modeling the pricing of houses using the Ames data set I was able to find housing features that provide high value for low cost.

## Modeling Methodology

### Data Cleaning
The train and test datasets were read into Pandas dataframes and combined. Dummy values were created using pd.get_dummies. Null values were imputed using sklearn.impute.IterativeImputer.  
![msno](https://git.generalassemb.ly/ZacharyJamesHill/dsi_assignments/blob/master/project_2/saved_figures/msno.png)
### EDA
The correlation between features and sale price was evaluated using pairplots and heatmaps.
![pairplot](https://git.generalassemb.ly/ZacharyJamesHill/dsi_assignments/blob/master/project_2/saved_figures/pairplot.png)
### Feature Selection
I attempted several feature selection techniques including selecting manualy and by correlation with price. Ultimately I dropped features with p values over .05, refitted the model and dropped high p values again.
### Modeling Techniques
Beyond submitting predictions to the leaderboard a train test split of the train data was used to evaluate the accuracy of the model. Taking the log of y aided the model by normalising the pricing values. Ridge and Lasso regression models were tested in an effort to reduce the effects of multicolinearity. Unfortunately Ridge and Lasso failed to increase test accuracy.
## Insights

### Visualization
A bar chart showing what amount the predicted price is accounted for by each feature in the model.
![contribs](https://git.generalassemb.ly/ZacharyJamesHill/dsi_assignments/blob/master/project_2/saved_figures/contribs.png)
### Supplimentary Data
Various pricing statisics were used to evaluate the value for cost each feature provides.
  
# Sources
Ames Development Budget  
https://www.cityofames.org/home/showdocument?id=51177  
  
Ames Construction Pricing  
https://home-builders.promatcher.com/cost/ames-ia-home-builders-costs-prices.aspx  
  
Ames Development Articles  
https://www.iowastatedaily.com/news/politics_and_administration/city/city-of-ames-will-act-as-developer-constructing-affordable-housing/article_cabbc08c-224d-11e8-b884-93ff7258eae3.html  
  
https://www.amestrib.com/news/20180306/council-picks-city-as-state-avenue-developer 

Various House Pricing
https://www.homeadvisor.com/

