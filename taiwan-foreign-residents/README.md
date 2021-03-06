# Taiwan foreign residents by nationality, 2017 and 2022

Data downloaded from Taiwan's Ministry of the Interior National Immigration Agency
* [2022](https://www.immigration.gov.tw/5475/5478/141478/141380/309062/cp_news)
* [2017](https://www.immigration.gov.tw/5475/5478/141478/141380/141666/cp_news)

## The map
Data of the "Total" columns from the 2017 and 2022 were used to calculate population difference and saved into [tw-foreign-nationality.csv](https://github.com/ilenapeng/points-unknown-data/blob/main/taiwan-foreign-residents/tw-foreign-nationality.csv). In [taiwan-data-to-geojson.ipynb](https://github.com/ilenapeng/points-unknown-data/blob/main/taiwan-foreign-residents/taiwan-data-to-geojson.ipynb), tw-foreign-nationality.csv was merged with a geojson from the University of California, Berkeley, which was downloaded from the [University of Texas at Austin](https://geodata.lib.utexas.edu/catalog/stanford-fn648mm8787) to create [tw-foreign-nationality.geojson](https://github.com/ilenapeng/points-unknown-data/blob/main/taiwan-foreign-residents/tw-foreign-nationality.geojson). That geojson was then used to produce the map in Mapbox.

## The analysis
The raw data downloaded from Taiwan's Ministry of the Interior National Immigration Agency consisted of multiple tables, with the same column names, pasted vertically on top of each other. This data was copy-pasted into a wide format so that all tables would sit side-by-side, with only one row of column names. This data was then transposed into the format seen in the [2017-](https://github.com/ilenapeng/points-unknown-data/blob/main/taiwan-foreign-residents/2017-tw-foreign-nationality-reshape.csv) and [2022-tw-foreign-nationality-reshape](https://github.com/ilenapeng/points-unknown-data/blob/main/taiwan-foreign-residents/2022-tw-foreign-nationality-reshape.csv) CSVs. This was then loaded into taiwan-analysis.ipynb to calculate the numbers used in the text.

## Table
For the mini charts in the Datawrapper table (created with this [Datawrapper tutorial](https://academy.datawrapper.de/article/197-how-to-add-bar-charts-line-charts-to-tables), I also downloaded the following additional data and copy-pasted all the ???Total??? columns to create [tw-foreign-nationality-each-year.csv](https://github.com/ilenapeng/points-unknown-data/blob/main/taiwan-foreign-residents/tw-foreign-nationality-each-year.csv)
* [2021](https://www.immigration.gov.tw/5475/5478/141478/141380/265881/cp_news)
* [2020](https://www.immigration.gov.tw/5475/5478/141478/141380/230106/cp_news)
* [2019](https://www.immigration.gov.tw/5475/5478/141478/141380/185516/cp_news)
* [2018](https://www.immigration.gov.tw/5475/5478/141478/141380/141636/cp_news)

To format the numbers in Google Sheets to have + and - signs before them and commas for the thousands, I used this:
````+#,##;-#,##;#,##````. And for the percentages: ````+0.00%;-0.00%;0.00%````
