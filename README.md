# Title

**Author**: Maria Kuzmin
## Overview

The goal of this study is to better understand how Microsoft can enter into the movie industry with maximum potential to succeed in profitability based on real world data.
The data is sourced from five major websites that give relevant monetary and release information concerning thousands of movies.
The data demonstrates that five specific genres are more profitable.
Also, the data showed that specific months of the year to release the movies is critical.

## Business Problem

To enter into the movie industry, Microsoft would need to have a clear path of entry that takes into account a series of factors based on the evidence of previous movies that proved to be successful and profitable. After researching about the most profitable movies, it became clear that certain genres tend to be more profitable than others, and therefore it was key to investigate if this was true or not based on real data. The key questions that need to be answered to effectively have a business plan are:

- What movie genres have the highest gross income?
- Which ones have the lowest budgets?
- Which movies provide the highest retun on investment?

And once the top genres are clear:
- What makes a movie profitable?
- What are the parameters that we can choose to try to increase our ROI?

And finally: 
- How much can Microsoft expect to produce as an income on average, and how much would it need to invest in the production budget per movie on average?

## Data

The data that was provided for this study consists of some tabular files (csv and tsv formats) that were taken by a few websites. Most of them have informations about the movie budget, gross income (domestic and worldwide), number of reviews and average reviews, movie genre and so on.
Another set of data we have is contained in a database (format SQL) that we can extract information from.
Beside the basic information that also the other websites provide, this database contains also the names of directors and writers for the movies, and a list of the people that each movie is known for.

Preparing the data was key prior to reaching any conclusions. 
First, I had to convert the type of some of the data, that represented numbers but was in the format of strings. 

Second, in order to identify the genre of the movies I had to split the string that describes the genre and convert that into a list, to be able to use the .explode() method to separate the movies that have multiple genres.

Third, I deleted the missing values that were present since there were only a few movies without a genre and compared to the number of entries I have the NaN values seemed negligible.

Fourth, I decided not to remove the outliers yet, since there is something that we can learn from the movie with the highest income or lowest budget.

However, I did decide to remove them for the last step of the analysis, when calculating the averages of budget and gross.

## Methods

With the DataFrame of movies divided by genre I grouped the movies by genre and calculated the average of the numerical values per genre.

In this way I was able to study what on average is the gross income (both worldwide and domestic) per genre. This also allowed me to see what is the budget per genre and some other similar calculations.

Then I selected what I found to be the five genres with highest gross income and highest ROI.

Starting from these five genres, I calculated how many people each movie was known for, and calculated to see if there is a correlation between the number of famous people in a movie and the gross income and production budget.

I also divided the movies by release date to study which are the release months that tend to have the highest gross.

Finally going back to the main database I calculated what is the gross income and budget on average, both considering only movies from the five top genres, and all the movies from all the other genres.

## Results

ROI, return on investment, is a performance measure to evaluate the efficiency or profitability of an investment. It is calculated as net income versus investment and it's expressed at a percentage. This is the most relevant of the figures since it keeps into account the budget and it is normalized so it can give us a more objective idea of how much a movie or a genre is actually profitable, all things considered. Let us calculate it:

Here is an example of how to embed images from your sub-folder:

### Visual 1
![graph1](./images/Graphs/ROI per genre.png)

## Conclusions

Provide your conclusions about the work you've done, including any limitations or next steps.

***
Questions to consider:
* What would you recommend the business do as a result of this work?
* What are some reasons why your analysis might not fully solve the business problem?
* What else could you do in the future to improve this project?
***

## For More Information

Please review our full analysis in [our Jupyter Notebook](./dsc-phase1-project-template.ipynb) or our [presentation](./DS_Project_Presentation.pdf).

For any additional questions, please contact **name & email, name & email**

## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── dsc-phase1-project-template.ipynb   <- Narrative documentation of analysis in Jupyter notebook
├── DS_Project_Presentation.pdf         <- PDF version of project presentation
├── data                                <- Both sourced externally and generated from code
└── images                              <- Both sourced externally and generated from code
```