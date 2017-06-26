
## Motivation
This project poses a pervasive social concern in a data science framework and provide insight using data science.  

## Tools used


|Stage|Tool|
|--|:--|
|Data collection| python: selenium (Firefox, phantomJS), boto3. AWS: EC2, S3|
|Data processing|python: BeautifulSoup, MongoDB|
|Data analysis|python: pandas, numpy, scikit-learn, nltk, networkx.  Gephi|
|Modeling | python: scikit-learn.  Latent Dirichlet Allocation, Non-negative matrix factorizatoin|



## Problem definition
 <img align="left" src="notes/resources/Screen%20Shot%202017-06-23%20at%205.14.46%20PM.png" width="300"> Mortality is inevitable and it befalls us all, but a third of all deaths are deemed premature.  The majority of premature deaths is preventable, arising from voluntary lifestyle choices.  The World Health Organization has estimated that if the major risk factors for chronic disease were eliminated, at least 80% of all heart disease, stroke, and type 2 diabetes would be prevented, and more than 40% of cancer cases would be prevented ([ref](http://www.who.int/chp/chronic_disease_report/full_report.pdf)).  In particular, about half of all American adults have one or more preventable, diet-related chronic diseases, including cardiovascular disease, type 2 diabetes, and overweight and obesity ([ref](https://health.gov/dietaryguidelines/2015/guidelines/executive-summary/). Among the statistics of lifestyle factors related to chronic disease, early deaths due to diet and physical activity patterns stands out in the fact that has actually increased in recent years (from 14% to 18% of all early deaths, 1990 to 2010). Poor diet and activity patterns is now the leading cause of early deaths, and the direct and indirect cost of their consequences are staggering.  
<p>
The digital age proffers all kinds of products built around data, yet it is apparent that the implicit value proposition of technology-- that it serves to improve our lives-- is not fully realized when it comes to issues of health.  As a population, we make voluntary choices that make us less healthy.  Numerous, complex reasons may exist for this epidemic, but to the extent that this is a data science problem, more data science tools are necessary to address the problem.  

The USDA and DHHS have conducted surveys on "What We Eat in America (WWEIA surveys) as well as analyses on nutrient compositions of foods consumed.  These bodies of knowledge form the basis for the dietary guidelines set forth every five years ([ref](https://health.gov/dietaryguidelines/2015/guidelines/executive-summary/)).  Their current recommendations are grounded on principles that guide healthy eating patterns over time ([ref](https://health.gov/dietaryguidelines/2015/guidelines/executive-summary/#figure-es-1-2015-2020-dietary-guidelines-for-americans-at-a-glan)).  

Current data What can be done to empower individuals to adopt healthier eating habits?  

## Using data oriented methods to generate actionable insight  
<img align="right" src="notes/resources/doing_data_science_fig.png" width="300">Fundamentally, data science is about doing science with data (statistics) that serves as the basis for delivering value in measurable form.  The cross industry standard process for data mining ([CRISP-DM](https://en.wikipedia.org/wiki/Cross_Industry_Standard_Process_for_Data_Mining)) is a widely adopted framework.  This diagram is an illustration of the steps involved.  

In this project, I set out to use data science tools to make real world observations in dietary behavior and explore ways to empower healthy living.  

## Data collection

The main choice for data source was allrecipes.com, a website repository of recipes that is also effectively a social platform for people who cook.  It is an unpolished grass-roots website for the everyday cooker ([ref](http://www.slate.com/articles/life/food/2016/05/allrecipes_reveals_the_enormous_gap_between_foodie_culture_and_what_americans.html))-- or at least it used to be; they have recently undergone a major commercial overhaul.  

The website is a trove of multidimensional data.  In addition to recipe pages that contain user-generated ingredients lists, directions, pictures, metrics (cooking time, servings, nutrition information, etc.), it also contains ratings and reviews linked to members who have made and evaluated the recipe.  Each member has a personal site with sections detailing recipes that they have made or enjoyed.  Also included are list of people that they follow or are followed by.  

- [Scraping the allrecipes.com website](https://github.com/q0j0p/food/wiki/Scraping-the-allrecipes.com-website)

The USDA maintains a database for "standard reference" foods and branded food items sold in the US.  These have nutrition information and the SR list is categorized.  

Allrecipes data was scraped from the website, while the USDA database was accessed via its API.  

## Data processing and storage
Scraped pages were parsed and stored as documents in a nosql database.  

## Exploratory data analysis
### Graph analysis of a member subset
<img src="notes/resources/graph1.png" width="650">


## Modeling
