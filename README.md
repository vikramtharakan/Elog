# Elog
Create an NLP pipeline that categorizes Elog entries.

## Overview
The goal is to first extract the data in a json file from the Elog and import it into a workable format. Then we want to apply some sort of natural language processing algorithm on it to classify it into one of the three entry categories. <br>
Twist: The actual model created won't be able to work immediately as the data it is getting trained on is incorrectly tagged and the tags will also likely change. However the idea (initially) is to creat a backbone for a structure that can create a working model. We (as operators) will likely have to tag entries correctly for about a a long time (let's say a few months) before there will be enough data to comprehensively train this model

## Files
#### Relevant Files
* <b>elog_etl.ipynb</b>: Jupyter notebook describing extracting/cleaning/storing the data
* <b>model.ipynb</b>: Jupyter notebook describing the steps taken to create the model
* <b>elog_data_2011.db</b>: Cleaned and tagged entries from 2011. The only accurate data we have at the moment. Will hopefully add another accuracte dataset in the near future
* <b>elog_all_data.db</b>: All entries from 2007-2018, excluding tags (disregarding 2019 onwards because downtime was weird. May want to include this, tbd). Can use this for unsupervised learning approach (try and learn FACET and LCLS).


#### Files used for practice
* <b>elog_etl.practice.ipynb</b>: Jupyter notebook used to test out ideas for extracting/cleaning/storing data
* <b>elog.ipynb</b>: Jupyter notebook contains all the steps taken from extracting data to creating the model
* <b>elog_data.db</b>: Practicing writing data to database.