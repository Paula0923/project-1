## Project One: Ironhack DA

<img width="400" alt="image" src="https://github.com/Paula0923/project-1/blob/main/picture.png">

## Introduction:

In this project data from the German parliament (Bundestag) was used to analyze questions like party distribution, the distribution of first names and the occurence of academical grade.

## Data Extraction:

Two sources of data were combined to create the final dataframe:

- Through the API of the German Bundestag, data concerning names of the members, date of their first election to be members of the parliament, their titles and their party belonging were gathered from the endpoint "/person":
    - https://search.dip.bundestag.de/api/v1/swagger-ui/#/
- As this showed not to be sufficient to get comprehensive data, I also used webscraping (with Selenium) on the website of the German Bundestag to gather a dataframe containing names and party belongings of all members of the German Bundestag (at the day of the 2021 election):
    - https://www.bundestag.de/abgeordnete

## Hypotheses:

1. Some first names will be found significantly more often.
   1a) In the parties CDU/CSU, FDP and AfD there will be a higher concentration and more male first names.
   1b) In the parties Die Grünen, Gruppe Die Linke/Gruppe BSW and SPD there will be a lower concentration and more female names.
2. The distribution of party belonging will be like the end results of the 2021 election of parliament.
3. Academical grade: the occurance of the academical grade "Dr." in the German Bundestag is higher than in the represented population (2019: 1.2%, https://www.academics.de/ratgeber/promotion-statistik)

## Findings:

The hypotheses have largely proved to be true, but not in their entirety:
- While there is a higher concentration of first names among the parties from the "right" wing of the parliament and a lower on the "left" side, male names dominate throughout. All the top five first names are male. This only changes once the analysis goes down to particular parties: Die Grünen and Die Linke/BSW stand out and, to a lesser degree, also the SPD.
    - The most common names among all parties are Michael, Thomas, Stefan, Christian and Andreas.
- The rate of persons with the academical grade doctorate is much higher than in the German population (15.9% vs. 1.2%)
- The analysis of the seat distribution showed that my database is not entirely reliable:
    - The created df must be faulty, there are more MoPs in this df than there should be (around 30) and therefore the calculations based on numbers are not right either. In their tendency, they are not wrong but in absolute terms, they are.

## Further information:

In the repo, you can find my presentation in which the main findings and obstacles are shown.
Also, you will find three different Jupyter Notebooks here:
1. for the main process of creating, merging and cleaning the dataframe: creating-and-cleaning-df_bt_project1.ipynb
2. for webscraping the website of the German Bundestag using Selenium: webscrap-selenium_bt_project1.ipynb
3. for the following basic EDA with some charts: EDA_bt_project1.ipynb

