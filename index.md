# CATALONIA CELL COVERAGE (2015 - 2017)



## Motivation

The dataset I have chosen  is the [Government of Catalonia](https://catalangovernment.eu/) released [data](https://analisi.transparenciacatalunya.cat/en/Ci-ncia-i-Tecnologia/Dades-recollides-per-l-aplicaci-Cobertura-M-bil-20/g9ma-vbt8/data) about cell coverage which shows the data regarding the service provider, operator, network, location, speed (upload and download) and many more things about any device at a particular day and time at a certain location. So, it made me wonder that i can use the data for some machine learning projects, in which i can use this data for predictions like which regions requires more towers if there are more congestions in the network, also it can be used by government to monitor any suspicious activities by frequential data about specific device. Also, the same data can be used to visualize different things like different regions and the number of population in that region using which operator and network and show some analytics about the popular networks and many more things. Data Science enthusiasts are always looking for something useful in the data so that it can useful for some visualization to show some discrepancy or to summarize different aspects about the data. I being a machine learning lover, love to use dat to predict something as it helps to get something out of data and helps with somethings which can ease the effort of doing it manually. This data helps in predicting many different things of which i have described some of them above, it only depends how we transform the data accordingly and pass it onto a machine learning model with pre-processing data earlier.



## About Data 

The Data is available as google provided [public dataset](https://console.cloud.google.com/marketplace/details/gencat/cell_coverage?project=riddler-quiz&folder&organizationId). But it can be found on the official website with recently updated data here. There are different data sets according to the region you are in, on google public dataset. To get the recent dataset, it can be downloaded from here or can accessed using the api provided by them.
The following description is from the developers only: 
**“ The GenCat Mobile Coverage app is an initiative of the Government of Catalonia to crowdsource data collection on the   state of mobile telephone network coverage in Catalonia. The platform uses an Android app to record citizens data through their mobile devices on the level of coverage per operator, network (2G, 3G and 4G) and the device's location. This dataset contains the platform data over the 2015-2017 period. This data might be used to analyze the quality of mobile coverage in Catalonia of the four main operators (Movistar, Vodafone, Orange and Yoigo) and filter data according to the technology used (2G, 3G or 4G). Additionally the data enables the identification of areas in Catalonia that need to improve their mobile coverage with the final goal of helping to improve the efficiency of basic services for the general public.”**



## Description

### Table Description Info 
![Image](Screen Shot 2020-05-04 at 8.41.20 PM.png)

### Table Schema
![Image](Screen Shot 2020-05-04 at 6.08.57 PM.png)
![Image](Screen Shot 2020-05-04 at 6.09.09 PM.png)

### Data Snapshot



## Obtaining Data And Pre-Processing 

The dataset contains unfiltered data, so it requires pre-processing before making visualizations out of it. The Data can be obtained in different ways:
1. Directly from [Google Public Dataset](https://console.cloud.google.com/marketplace/details/gencat/cell_coverage?project=riddler-quiz&folder&organizationId) .
2. It can be crawled from the [API](https://analisi.transparenciacatalunya.cat/resource/g9ma-vbt8.json).
3. It can be downloaded from [here](https://analisi.transparenciacatalunya.cat/en/Ci-ncia-i-Tecnologia/Dades-recollides-per-l-aplicaci-Cobertura-M-bil-20/g9ma-vbt8/data).
	
__The data is unprocessed and contains certain unwanted material. So, preprocessing was required on bigquery before doing the visualizations on the data. I was going to download the data and then apply preprocessing to the data and then upload the data to Google Cloud Storage. But the main problem here, was that the data was in spanish which would have been  a problem for me to run queries on big query. So, I resorted to  big query as google dataset has 2 versions which have 2 different languages, one for EU region and another for US region. So, I’m using the US version data for my project. The pre-processing done on data is to remove the null values and unknown values from the data when running queries as of now as I’m using the google public dataset i just need to keep in mind to check for null and unknown values while executing the queries before showing the analysis, otherwise analysis will have discrepancies and will not give appropriate  analysis and visualization.__

## Big Query


### - How did you load your data to BigQuery?

I am already using the data stored in bigquery. But, initially i tried to to process the data and then load the data into bigquery but the data that was download needed to be translated into English, i prefered doing queries on Big-Query with dataset already on it.

### - After loading the data to BigQuery, describe what table(s) you’d have and what the schema(s) would be like. 
  
Table mobile_data_2015_2017 will be used for the analysis part and which further can be used to preprocess the data for some other useful data as per analysis. 

![Image](Screen Shot 2020-05-04 at 6.08.57 PM.png)
![Image](Screen Shot 2020-05-04 at 6.09.09 PM.png)


## Analytics


## Challenges

## Future Work



## Why Big Query? 

```markdown
Syntax highlighted code block

# Header 1

## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ameyay98/PersonalProject/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
