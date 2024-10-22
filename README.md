## Project One: Ironhack DA

<img width="400" alt="image" src="https://github.com/Paula0923/project-1/blob/main/picture_adler-project1.png">

## Introduction:

In this project data from the German parliament (Bundestag) was used to analyze questions like party distribution, the distribution of first names and the occurence of academical grade.

## Data Extraction:

Two sources of data were combined to create the final dataframe:

- Through the API of the German Bundestag, data concerning names of the members, date of their first election to be members of the parliament, their titles and their party belonging were gathered from the endpoint "/person":
    - https://search.dip.bundestag.de/api/v1/swagger-ui/#/
- As this showed not to be sufficient to get comprehensive data, I also used webscraping (with Selenium) on the website of the German Bundestag to gather a dataframe containing names and party belongings of all members of the German Bundestag (on 21.10.2024):
    - https://www.bundestag.de/abgeordnete

## Hypotheses:

1. Certain first names will be found significantly more often.
   1a) In the parties CDU/CSU, FDP and AfD there will be a higher concentration and more male first names.
   1b) In the parties Die Grünen, Gruppe Die Linke/Gruppe BSW and SPD there will be a lower concentration and more female names.
2. The distribution of party belonging will be like shown on a different subpage of the German Bundestag (current data): https://www.bundestag.de/parlament/plenum/sitzverteilung_20wp.
3. Academical grade: the occurance of the academical grade "Dr." in the German Bundestag is higher than in the represented population (2019: 1.2%, https://www.academics.de/ratgeber/promotion-statistik)

## Findings:

The hypotheses have largely proved to be true, but not in their entirety:
- While there is a higher concentration of first names among the parties from the "right" wing of the parliament and a lower on the "left" side, male names dominate throughout. All the top five first names are male. This only changes once the analysis goes down to particular parties: Die Grünen and Die Linke/BSW stand out and, to a lesser degree, also the SPD.
    - The most common names among all parties are Michael, Thomas, Stefan, Christian and Andreas.
- The rate of persons with the academical grade doctorate is much higher than in the German population (15.8% vs. 1.2%)
- The analysis of the seat distribution is almost exactely like the numbers on an overview by the German Bundestag (https://www.bundestag.de/parlament/plenum/sitzverteilung_20wp).
    - There is one person less in the fraction "AfD" and one more without fraction ("fraktionslos"), there must have been one change recently and either one of the different subpages is not updated.

## Further information:

In the repo, you can find my presentation in which the main findings and obstacles are shown.
Also, you will find three different Jupyter Notebooks here:
1. for the main process of creating, merging and cleaning the dataframe: creating-and-cleaning-df_bt_project1.ipynb
2. for webscraping the website of the German Bundestag using Selenium: webscrap-selenium_bt_project1.ipynb
3. for the following basic EDA with some charts: EDA_bt_project1.ipynb

