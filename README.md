# Airline-Reviews-Analysis-with-PySpark

Airline Reviews Analysis with PySpark
This project focuses on analyzing airline reviews using PySpark, a powerful Apache Spark library for big data processing. The dataset used for this analysis contains information about airline reviews, including various aspects like overall rating, review details, and connectivity features.

Getting Started
Prerequisites
Make sure you have Python, PySpark, and required libraries installed. You can install PySpark using:

![image](https://github.com/Revealis/Airline-Reviews-Analysis-with-PySpark/assets/126680990/b96f6f89-e246-4015-9528-3b5db66cae23)

Usage
Import necessary libraries:

![image](https://github.com/Revealis/Airline-Reviews-Analysis-with-PySpark/assets/126680990/af8d9c21-a399-452c-8574-620ec16feec3)

Create a Spark session and read the CSV file:

![image](https://github.com/Revealis/Airline-Reviews-Analysis-with-PySpark/assets/126680990/3f479d7e-8632-4bd9-8ab4-915a3aadca5a)

Define a schema for the DataFrame:

![image](https://github.com/Revealis/Airline-Reviews-Analysis-with-PySpark/assets/126680990/06a8122a-5c28-41f0-848e-dd4bdeddddc0)

Perform data cleaning and handling missing values:

![image](https://github.com/Revealis/Airline-Reviews-Analysis-with-PySpark/assets/126680990/91ae9121-0c02-46ba-b871-4450f754ae4a)

Analyze the data:

![image](https://github.com/Revealis/Airline-Reviews-Analysis-with-PySpark/assets/126680990/0398ae76-4738-45b4-b5dd-7fa4562f97b6)


+---+-------------+--------------------+-----------------+-------------------+--------------+--------------------+---------------+---------------+--------------------+--------------+-----------+-----------------+-------------+-------------+-----------+----------------+----------------+---------------------+-------------------+
|Pid|OverallRating|        ReviewHeader|             Name|           Datetime|VerifiedReview|          ReviewBody|TypeOfTraveller|       SeatType|               Route|     DateFlown|SeatComfort|CabinStaffService|GroundService|ValueForMoney|Recommended|        Aircraft|FoodAndBeverages|InflightEntertainment|WifiAndConnectivity|
+---+-------------+--------------------+-----------------+-------------------+--------------+--------------------+---------------+---------------+--------------------+--------------+-----------+-----------------+-------------+-------------+-----------+----------------+----------------+---------------------+-------------------+
| 33|           10|"""Excellent serv...|   Peter Costello|   7th October 2023|          true|Excellent service...|   Solo Leisure|    First Class|London to New Yor...|  October 2023|          5|                5|            5|            5|        yes|      Boeing 777|               5|                    4|                  5|
| 77|            8|"""Cabin crew wer...|          E Smyth|   13th August 2023|          true|Easy check in a T...| Family Leisure| Business Class|     London to Miami|   August 2023|          4|                5|            4|            4|        yes|            A380|               5|                    5|                  5|
|111|           10|"""In-line with c...|         S Warten|      2nd July 2023|          true|Flight fine. In-l...|   Solo Leisure|  Economy Class|    Berlin to London|     July 2023|          5|                5|            4|            5|        yes|            A320|               3|   2.6482643245503974|                  5|
|146|            9|"""Service was go...|          E Smyth|      29th May 2023|          true|Busy day at LHR a...| Family Leisure|Premium Economy|  London to New York|        May-23|          4|                4|            4|            4|        yes|  Boeing 777-300|               3|                    5|                  5|
|185|            4|"""downright rude...|     Andrew Pybus|     6th April 2023|          true|Obviously many ai...|       Business|Premium Economy| London to Hong Kong|    April 2023|          2|                2|            4|            3|         no|      Boeing 787|               3|                    3|                  5|
|188|            9|"""a very solid e...|           C Down|    31st March 2023|          true|Boarding at Mumba...|   Solo Leisure|  Economy Class|    Mumbai to London|    March 2023|          4|                5|            4|            5|        yes|  Boeing 777-200|               3|                    5|                  5|
|233|           10|"""crew are a cre...|       S Anderson|  31st January 2023|          true|Organised boardin...|       Business|  Economy Class|London Heathrow t...|  January 2023|          5|                5|            5|            5|        yes|            A320|               4|   2.6482643245503974|                  5|
|244|            9|"""a good drinks ...|          E Smyth|  17th January 2023|          true|Easy check in and...| Couple Leisure| Business Class|London Heathrow t...|  January 2023|          3|                5|            4|            4|        yes|  Boeing 777-200|               5|                    5|                  5|
|290|            9|"""has returned t...|  Peter Pomeranze|  30th October 2022|          true|A great flight. T...|   Solo Leisure| Business Class|London to Los Ang...|  October 2022|          5|                4|            3|            5|        yes|       A350-1000|               5|                    5|                  5|
|291|            9|"""this flight wa...|  Peter Pomeranze|  30th October 2022|          true|I am happy to say...|   Solo Leisure| Business Class|Copenhagen to Hea...|  October 2022|          3|                5|            4|            5|        yes|            A320|               5|   2.6482643245503974|                  5|
|293|            9|"""A very positiv...|        R Hardell|  24th October 2022|          true|A very positive e...| Couple Leisure| Business Class|   Atlanta to London|  October 2022|          5|                4|            5|            4|        yes|   Boeing 787-10|               4|                    5|                  5|
|296|            1|"""Very rude and ...|    Ben Mallinson|  22nd October 2022|          true|We boarded our fl...| Couple Leisure|  Economy Class|London to San Fra...|  October 2022|          1|                1|            1|            1|         no|            A380|               3|                    3|                  5|
|310|           10|"""Couldnâ€™t fau...|  Jennifer Foster|23rd September 2022|         false|I would like to t...|   Solo Leisure|Premium Economy|Heathrow to Mexic...|September 2022|          5|                5|            5|            5|        yes|     Unspecified|               5|                    5|                  5|
|311|           10|"""personnel was ...|  Gaspard de Laaf|20th September 2022|          true|British Airways p...|   Solo Leisure|  Economy Class|     London to Tampa|September 2022|          5|                5|            5|            5|        yes|     Unspecified|               5|                    5|                  5|
|312|            4|"""Should be more...|Elizabeth Vaughan|16th September 2022|         false|Good flight apart...|   Solo Leisure|  Economy Class|Sydney to London ...|September 2022|          1|                3|            4|            2|        yes|     Unspecified|               2|                    5|                  5|
|327|           10|"""amazing at her...|   Josephine Vega|   10th August 2022|         false|My husband, paren...| Couple Leisure|  Economy Class|  London to New York|     July 2022|          5|                5|            5|            3|        yes|     Unspecified|               5|                    5|                  5|
|334|            8|"""A good flight ...|          E Smyth|     23rd July 2022|          true|Flight on A380 SF...| Family Leisure| Business Class|San Francisco to ...|     July 2022|          4|                5|            4|            4|        yes|            A380|               4|                    4|                  5|
|343|            8|"""Overall a good...|          E Smyth|      9th July 2022|          true|Check in and secu...| Family Leisure| Business Class|London to Los Ang...|     July 2022|          4|                4|            5|            4|        yes|            A350|               4|                    5|                  5|
|373|            9|"""Overall it was...|      Daniel Cook|      2nd June 2022|          true|Recent trip to Bo...|       Business|  Economy Class|    London to Boston|        May-22|          4|                5|            5|            3|        yes|Boeing 777-300ER|               5|   2.6482643245503974|                  5|
|394|           10|"""thank you for ...|       C Barteres|    29th April 2022|          true|I would like to t...|   Solo Leisure|  Economy Class|SÃ£o Paulo to Mil...|    April 2022|          5|                5|            5|            5|        yes|     Unspecified|               5|                    5|                  5|
+---+-------------+--------------------+-----------------+-------------------+--------------+--------------------+---------------+---------------+--------------------+--------------+-----------+-----------------+-------------+-------------+-----------+----------------+----------------+---------------------+-------------------+


Some examples:

![image](https://github.com/Revealis/Airline-Reviews-Analysis-with-PySpark/assets/126680990/de828dea-82cd-41c4-9b98-2a13ebbedd4c)
::

![image](https://github.com/Revealis/Airline-Reviews-Analysis-with-PySpark/assets/126680990/33ee7781-aab4-467a-8384-c6f759bb158e)


::

![image](https://github.com/Revealis/Airline-Reviews-Analysis-with-PySpark/assets/126680990/f0f0d13e-ef56-46ea-93fd-bff42ec876b2)

::

![image](https://github.com/Revealis/Airline-Reviews-Analysis-with-PySpark/assets/126680990/1e1b5f03-1489-41c5-97e8-6f9aa46af5f5)












