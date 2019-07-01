# Analyzing Housing Prices in Ames, Iowa

## Problem Statement
  Housing in any state is generally a difficult game of figuring out how to best assess value. Within every city or town, there is a plethora of information available to inform such a decision. Figuring out what features are important, which can be overlooked, and the significance of each's on a home's value is a process of sorting through this mound of information and adding context.    
  <br>
  Whether for students seeking opportunity at Iowa University or families putting down roots, Ames seems a fine choice.
With a 2010 population of almost 60,000 (almost half of which are college students) and an unemployment rate of just 1.5% people are moving.
Real estate agents and developers must figure out what attributes of a home make it most desirable to a potential future owner.    
<br>
My goal is to filter out those features that make the most difference, in context with the city, to identify where people want to live - and why.    

## Relevant Files
* [Datasets](https://git.generalassemb.ly/Rose-TesorieroMontoya/project_2/tree/master/datasets)
* [Code Notebook](https://git.generalassemb.ly/Rose-TesorieroMontoya/project_2/tree/master/code)
* [Slides](https://docs.google.com/presentation/d/1MM3tVLN0oCN3TYF456SoIycP0dxYaI6Xppbsx8q8hGM/edit?usp=sharing)    

## Executive Summary
  Given such an extensive dataset, my first step was to make sense of all the columns. Using the data description, I was able to determine what each feature was and how the imput values translated to real life homes.<br>
  With so many null features, determining how to deal with missing values was a somewhat extensive process of sifting through and understanding where the creator of the dataset had used "NA" to denote a nonexistent feature, and where there had either been a mistake or a lack of information.<br>
  Using my own judgement, I identified correlated features and combined those necessary into one. Outliers were another issue. While we do not want to place too much significance on a single occurence - which would lead our model greatly askew - so too do we not want to completely misperform on homes with unique features.    
  By transforming all categorical data into numerical, I created a standardized dataset, imputing many values on a ranking system, or simply creating dummy columns.    
  What I found to be the most interesting - if not most significant - variable was the neighborhood in which a home is located. A home's location in certain neighborhoods could bring up the price by quite a bit - or decrease it. However, I discovered that just because the selling price of homes in more desirable neighborhoods were above average for the city, it did not mean more homes were sold. <br> 
  E.g. - Green Hills has some of the priciest homes, but the data is inconspicuously sparse - or missing - after 2007. Recall: the housing recession hit in 2008.    
  This lead me to question what about these neighborhoods changed the value of a home that had similar features to another home in a different neighborhood?<br>
  I was drawn to question something that does not immediately come to mind when looking at the Midwestern United States but in this case appeared to be a factor: crime rate.<br>
  Using data from US census, Ames' website, and an interactive crime report map of the city, I was able to identify that those neighborhoods seen as most desirable had far fewer reported crimes than those neighborhoods that appeared to have a negative correlation to home value.     
  
  ## Conclusions/Recommendation
    Despite my interest in the effect of crime rate on neighborhood desirability and therefore on home value, my model showed other variables of much more significance:    
    
* Newer properties (later “Year Built” dates) will have greater value
* Homes designated “Higher Quality” will also have greater value
* Home size, on the ground floor is, related to higher value
* However, when a basement’s finished square footage is greater than half its overall square footage, home value decreases
* Neighborhoods in which homes are sold for higher prices tend to be in lower crime areas
* Neighborhoods that negatively affected sale price are those with slightly more crime    

## Source Documentation

* ["In This Town, You Apply for a Job and You Get It", NPR] (https://www.npr.org/2019/05/23/721086615/in-this-town-you-apply-for-a-job-and-you-get-it)
* [Residential Map of Ames] (http://jse.amstat.org/v19n3/decock/AmesResidential.pdf)
* [Neighborhood Scout - Crime Rates in Ames, Iowa] (https://www.neighborhoodscout.com/ia/ames/crime)
* [Spot Crime - Recent Crime in Ames, Iowa - Interactive Map] (https://spotcrime.com/ia/ames)

  
 

