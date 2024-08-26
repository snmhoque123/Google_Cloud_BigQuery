# City of San Francisco Tree Project
The city of San Francisco mayor wants to start an annual tree appreciation program, which will involve decorating trees along streetsides. As a Data Analyst, the task is to provide the mayor’s office with a list of the top 10 addresses where mature trees have been planted along the streets. With this information, they can plan to have trees decorated before the event begins and the decorations cleaned up once it is complete. 

In this activity, the following tasks has been completed: 

- Select this data from the Street Trees dataset and transport it into a target table

- Find the 10 addresses with the most trees planted along the street 

- Find the number of trees at each address

The Street Trees dataset* is publicly available on BigQuery and contains more than 190 thousand rows of data about trees planted in San Francisco from 1955 to the present. It has information about each tree maintained by the San Francisco Department of Public Works in the city, including each tree’s unique ID, address where it was planted, plot size, geographic coordinates, and more.

*This dataset is publicly available and provided by  
[https://data.sfgov.org//](https://data.sfgov.org//), the San Francisco’s Department Publishing Plans portal. This data is provided on an “as-is” basis and is subject to change at any time without notice. Please visit the source to get the latest version.


### SQL Code:
```SQL
SELECT
    address,
    COUNT(address) AS number_of_trees
FROM
    `bigquery-public-data.san_francisco_trees.street_trees`
WHERE
    address != "null"
GROUP BY address
ORDER BY number_of_trees DESC
LIMIT 10;
```

### [Click the Project Sample Link](https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1squery-a-public-dataset-azizul!2sus-central1!3se96f6e27-61e4-450f-a292-e7b075f12816!2e1)

The Project Screenshot from the Google Cloud Platform BigQuery as follows:
![Screenshot](https://github.com/snmhoque123/Google_Cloud_BigQuery/blob/main/Sample_Screenshot.png)


### [Click Data Visualization using Looker Studio](https://lookerstudio.google.com/s/rFbjzR-CrzU)

The output data can be visualized using Looker Studio:
![](https://github.com/snmhoque123/Google_Cloud_BigQuery/blob/main/Data_visualization.png)


