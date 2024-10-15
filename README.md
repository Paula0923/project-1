## Shark Quest: Team Coral Reefs

<img width="700" alt="image" src="https://github.com/user-attachments/assets/9367e333-b8ba-48ce-bdf1-8f8b4c710521">

## Introduction:

Business case: We are a travel agency and are specialized on customers who like water sports of all kinds but are aware of the danger of shark attacks.

For this, we need to look at data of shark attacks to find out where people are more or less likely to be (fatally) attacked and what kind of activity attacked people were doing so that we can inform our customers accurately what they should not be doing.

## Hypotheses:

These are our HYPOTHESES, we created them from the first impression of the dataset and also from common assumptions on shark attacks:

- H1: WHERE Geography has influence: It is more likely to be attacked by a Shark in   Australia or in the US than in other countries
- H2: WHO Demographic factors have an influence:
    - H2a Males are more likely to be attacked by a shark
    - H2b Young people (under 35) are more likely to be attacked by a shark
- H3: WHAT Endangering activity: It is more likely to be fatally attacked while surfing than while swimming

## Data cleaning

- There were lot of quality issues in the data: some examples: almost half the age values were NaNs; there were empty columns with almost no data; unnamed columns; there was a lot of string in what should be numerical values (age, date) and a lot of additional text in what should be categorical data (fatal, activity)
- techniques we used to solve this: handling null values in different ways (using median, ffill, assigning them to a value category), dropping columns, manipulating strings (i.e. filtering, erasing), categorizing data, handling duplicates
- for interested readers cleaning on specific columns can be found in the Jupyter Notebook in our repo

## Findings:

- COUNTRY: Most shark attacks happen in the USA, followed by Australia.
- FATALITY: The fatality rate varies from country to country: i.e. in Australia 10% of the attacks ended deadly, whereas only 2.3% in the US and even 16% in South Africa  
- ACITIVITY/ FATALITY: Surfing is the activity most dangerous in regards to the probability of being attacked by a shark. Followed by swimming and fishing. Yet the deadlist acitivity was swimming (13% of the attacks ended deadly), followed by fishing (6.8%) and only then surfing (6.3%).
- DEMOGRAPHICS: The vast majority of people attacked by a shark are male, most of them are young (the median is 28 and 75% are under 37).

## Further information:

The Data used can be found on: https://www.sharkattackfile.net/spreadsheets/GSAF5.xls
(It is still being updated, we retrieved the data on 21st September 2024.)

In the repo, you can find a presentation in which our steps in data cleaning and manipulating and our EDA results are explained. Also, you will find the Jupyter Notebook which contains our entire code and the results of our analysis with explanations/descriptions.

