
# Mortality rates of Inmates in the Florida Department of Corrections

## What I wanted to get by scraping

I scraped data on the morality rates of inmates in the Florida Department of Corrections for six years starting in 2017. The data collected shows the name, DC number, institution name, manner of death determined by a medical examiner and the investigative status of all inmates from 2017 to 2023. Further, I scraped data of each inmate to find their race, sex, birth date, and custody type.

This collection of data could be useful for analyzing trends in inmate mortality rates in the Florida Department of Corrections, which could lead to policy changes that could improve the safety and well-being of inmates. Additionally, this data could be useful for conducting research on the health and mortality of incarcerated individuals, which is an area that is often overlooked. This data could also be used to create visualizations such as a map displaying the counties or other tools that could help educate the public and policymakers about the issue of inmate mortality.

## Steps taken to scrape this data

1. First, I had to get the partial urls for the six years storing the inmates information. I did this by using the get_urls() function to extract the href attributes of the relevant <a> tags on the main page. 
2. Then, I had to get the name, DC number, death date, institution name and manner of death for each inmate. I did this by extracting the data from each td element in the row, appending it to the data list and then creating keys for each row.
3. Next, I looped over the partial URLs for each year, passed them to the function and stored the resulting links in a list.
4.After that, I wrote a function to scrape the information from each inmate's page. This function takes in a URL and uses BeautifulSoup to parse the HTML and extract the relevant information, such as the inmate's name, race, sex, birthday and custody information. I did this by extracting the data from each th element in the row, appending it to the data list and then creating keys for each row.
5. Finally I wrote two separate csv files to store both informaton scraped.
    
## Challenges I faced
    
One challenge I faced was deciding how to create the csv files. Was I going to create one or two? Ultimately, I decided on creating two since some inmates didn't have information listed. With that being said, if I created one csv file then the information would have been mixed up and wrong when combined. 