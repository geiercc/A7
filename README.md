# A7

The goal of this project was to perform an analysis to answer three primary research questions:

1. How masking policies changed the progression of confirmed COVID-19 cases from February 1, 2020 through October 15, 2021?

2. What is the relationship between Covid-19 infection rate and unemployment rate in Baltimore County?

3. What is the relationship between Covid-19 infection rate and crime reports in Baltimore County?



The tables in the raw data file are as follows:

- **unemployment**
- columns:
  - date: month and year (date)
  - Year: year (int)
  - Month: month (int)
  - labor force: labor force count (int)
  - employment: employed count (int)
  - unemployment: unemployed count (int)
  - unemployment rate: unemployment rate (decimal)

- **mask-use-by-county**
- columns:
  - COUNTYFP: county FP code (int)
  - NEVER: probability of never wearing a mask (decimal)
  - RARELY: probability of rarely wearing a mask (decimal)
  - SOMETIMES: probability of sometimes wearing a mask (decimal)
  - FREQUENTLY: probability of frequently wearing a mask (decimal)
  - ALWAYS: probability of always wearing a mask (decimal)

- **maryland_unemployment**
- columns:
  - State: State name (string)
  - Filed week ended: the end of the filed unemployment claim (date)
  - Initial Claims: number of claims (int)
  - Reflecting Week Ended: the end of the reflecting week (date)
  - Continued Claims: number of continued claims (int)
  - Covered Employment: number of those on covered employment (int)
  - Insured Unemployment Rate: insured unemployment rate (decimal)


- **crime_data**
- columns:
  - Date: month and year (date)
  - Year: year (int)
  - Month: month (int)
  - Arson: count of arson cases in given month (int)
  - Assault: count of assault cases in given month (int)
  - Burglary: count of burglary cases in given month (int)
  - Homicide: count of homicide cases in given month (int)
  - Motor Vehicle Theft: count of motor vehicle theft cases in given month (int)
  - Sexual Assault: count of sexual assault cases in given month (int)
  - Robbery: count of robbery cases in given month (int)
  - Total: count of total cases in given month (int)


- **CONVENTIENT_us_metadata**
- columns:
  - Province_State: State value (string)
  - Admin2: County (string)
  - Population: population of county (int)
  - Lat: latitude (decimal)
  - Long: longitude (decimal)

- **CONVENTIENT_us_confirmed_cases**
- columns:
  - contains columns with all states and daily confirmed covid cases in the form of an int

Limitations:

The most significant limitation I faced in my analysis was the lack of publicly available granular data for both crime reports and unemployment rate. While I had daily data for both Covid-19 cases and whether a masking mandate was in effect, I could only find monthly data for crime reports and unemployment rate in Baltimore County. Due to this lack of data, I was unable to find significant relationships and further analysis would be needed to draw more accurate conclusions. Even when using the weekly data from the state of Maryland, it only included unemployment rate of those on unemployment benefits, a limitation as it didn’t include all those unemployed.
I was also unable to make comparisons across 2020 and 2021 for crime reports due to changes in reporting. This made it hard to measure the effect of Covid-19 infection rate on crime report count as the pandemic went on, as I could only look into one year at a time. Additionally, there was no credible information on crime report counts from before 2020 that I could access to attempt to understand the baseline for crime report counts before the pandemic started.
Another limitation is the assumption I made in each analysis of there being no confounding factors. For instance, when I investigated mask mandate vs Covid-19 infection rate I assumed mask mandates were the only factors that could be affecting infection rate, while in reality many other factors are at play including vaccinations and social distancing. While there were no other factors considered, I believe some meaningful conclusions can still be drawn just from looking at these two factors in my analysis.


Reflection: 
I initially wanted to understand the relationship between masking mandates and Covid-19 infection rate, as well as between crime reports, unemployment rate and Covid-19 infection rate. My first research question was “How did masking policies change the progression of confirmed Covid-19 cases from February 1, 2020 to October 15, 2021 in Baltimore County?”. By creating a visualization, I was able to see that lower infection rate seemed to follow implementation of a masking mandate, with the rate starting to rise again after the mandate was lifted. 
My second research question was if Covid-19 infection rate and unemployment rate in Baltimore County were correlated with each other. My hypothesis was that they would be positively correlated, while the null hypothesis stated no correlation between the two variables. I ended up failing to reject this null hypothesis as I found no statistically significant correlation between these two variables. Even looking at a more granular level of weekly insured unemployment rate in the state of Maryland yielded no significant correlation. Additionally, the cross correlation for this data yielded no meaningful relationship either, as the optimal lag time was 7 months. It seemed that the state stay-at-home order might have been a better indicator for the rise in unemployment rate, especially as unemployment rate began declining as the initial order ended, even with the fluctuations in infection rate. 
Finally, I asked if Covid-19 infection rate and crime report count in Baltimore County were correlated. My hypothesis was that they would be positively correlated, with a null hypothesis that there was no correlation. I also ended up failing to reject this null hypothesis with no statistically significant correlation in the year 2020 or 2021. 
This analysis should inform an understanding of human centered data science as one must consider the meaning of results outside of what is statistically significant. Other studies have shown relationships between unemployment and crime, Covid-19 and unemployment, and masking mandates and decrease in Covid-19 cases and the reader should always ensure they are considering multiple credible sources. This study has been made reproducible if the reader wished to reproduce it on their own and see the limitations first-hand. Questions such as those asked in this study are important to understand so that the real effects on people can be understood and measures can be taken to improve upon things such as unemployment or crime rate. The first step in solving these problems is to ask and understand these human centered questions.


For more information see A7 Written report in the Reports folder.
