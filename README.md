# MIS-311
**1. Data overview**
   
The Bird of India Dataset provides various recorded information on bird species observed in India which is not only a biological research resource, but also a strategic asset. This data may be modeled from Citizen science projects like eBird which are contributed through observations and recordings by bird lovers. The main purpose of this data is to help researchers and conservationists observe the health of bird populations in India, monitor their distribution and conservation status. Beside that, this data can also help offer specialized birding trips using either uncommon species to offer an experience that is more exclusive and costly, or common species to ensure a memorable experience. Data analytics will help transform raw information into actionable decisions.

<img width="722" height="399" alt="image" src="https://github.com/user-attachments/assets/6d03fa05-8c28-429e-ac8f-225df4a8add9" />

It includes 202 rows ( excludes headings) and 4 columns: name, scientific name, last observation and total observations.
- Name: Common name of the bird 
- Scientific name: Scientific name of the bird 
- Last observation: Date when the bird was last seen
- Total observations: Total number of times the bird was observed
This dataset provides valuable information by identifying prominent or under-monitored species, and it is also essential for making strategic decisions about tourist initiatives, creating environmental monitoring technologies, or modifying conservation funding.

**2. Data Cleaning**
Identify Missing value and how to handle these missing value:

<img width="718" height="436" alt="image" src="https://github.com/user-attachments/assets/f96c98b2-4700-4de8-8c95-2bac0d50a3ad" />

Filtering the name column by unselecting all then choosing blanks.
The result is that there is no missing value in this initial dataset

**Identify any duplicate rows and remove duplicate rows if necessary**

<img width="760" height="321" alt="image" src="https://github.com/user-attachments/assets/345509c4-c2eb-448b-b4a1-fd8ede168f77" />

Data → Data Tool → Remove Duplicate
After identifying the missing value, we can see that there is no missing value in this dataset so the number of rows has not changed, still there are 203 rows. However, after identifying duplicate rows by using the “Remove Duplicate” tool, the result shows that there are three duplicate values. I delete these three rows, and the row is 199 rows. This elimination ensures that each unique bird species is represented by only one record, preventing incorrectness in the calculations of total observations. This is because  the overall number of species recorded will be incorrectly calculated if these three entries are not eliminated, misleading us about the data's coverage.

**3. Descriptive Statistics** 

<img width="328" height="404" alt="image" src="https://github.com/user-attachments/assets/8cb89a2e-df49-4f9e-a166-302df4c0a941" />

Table: Key Insight 1 of Bird in India

<img width="346" height="390" alt="image" src="https://github.com/user-attachments/assets/350e3995-f37b-4a0b-831b-3dbacbdf04f7" />

Table: Key insight 2 of Bird in India

**Insight 1: Imbalance in Monitoring Intensity**

<img width="730" height="373" alt="image" src="https://github.com/user-attachments/assets/3b4f7c43-9fd6-4d3c-b147-d886d93c2894" />

The Total Observations column was used to select and sort the entire information range, including the Name and Total Observations columns, in the following order: (Largest to Smallest). This method makes it easy to see at a glance which bird species were observed the most and the number of observations decreasing from large to small. This direct sorting strongly demonstrates that the data is over-concentrated in a small number of species. This concentration implies that the observing community's efforts are not distributed equally. For conservation organizations, this presents concerns because it makes it impossible to accurately assess the status of rarer species, whose populations are probably dropping without being noticed in time.

**Insight 2: Total number of species are observed by year**

<img width="742" height="455" alt="image" src="https://github.com/user-attachments/assets/80a128a6-07f8-4775-ad06-2ef6932a9baf" />

In order to ensure that they are accurately counted and do not result in errors in the date calculations, rows having a value of "No Observations" in the Last Observation column are first handled independently by sorting the data. The YEAR() function is then used to convert all of the remaining valid date values into a single "Year" column. And then using the COUNTIF function to count the number of bird species in four main years: count the number of bird species in four main categories: 2024, 2023, 2022, and the No Observed category.

This data shows how active the watching community is on a regular basis. The high number of species observed in 2024 and 2023 demonstrates recent active engagement. However, the presence of species that have never been observed or have data from 2022 or earlier raises the risk of data obsolescence. These species create serious temporal data gaps, requiring conservation organizations to prioritize new data collection campaigns to ensure the reliability and timeliness of information.







