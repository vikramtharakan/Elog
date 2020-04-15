# Elog
Create an NLP pipeline that categorizes Elog entries.

## Overview
The goal is to first extract the data in a json file from the Elog and import it into a workable format. Then we want to apply some sort of natural language processing algorithm on it to classify it into one of the three entry categories. <br>
Twist: The actual model created won't be able to work immediately as the data it is getting trained on is incorrectly tagged and the tags will also likely change. However the idea (initially) is to creat a backbone for a structure that can create a working model. We (as operators) will likely have to tag entries correctly for about a a long time (let's say a few months) before there will be enough data to comprehensively train this model

## Files
#### Relevant Files
<u>Data</u>
* <b>elog_etl.ipynb</b>: Jupyter notebook describing extracting/cleaning/storing the data
* <b>elog_all_data*.db</b>: Multiple files (likely 10 numbering 0-9) that contain all the cleaned data from 2007 to 2018. Had to divide it up due to space issues on Github. All of these files will be used to train an unsupervied model using LSA `LSA_model.ipynb`.
* <b>elog_data_2011.db</b>: Only contains cleaned, <i>tagged</i>, entries from 2007-2011 (the range we can "trust"). Will be used to train supervised NLP model in the Models section `model.ipynb`.

<u>Models</u>
* <b>model.ipynb</b>: Jupyter notebook describing the steps taken to create the supervised NLP learning model
* <b>LSA_model.ipynb</b>: Jupyter notebook describing the steps taken to create the unsupervised LSA learning model


<br>
#### Less Relevant Files
<u>Data</u>
* <b>elog_etl_practice.ipynb</b>: Notebook used practicing and experimenting during the cleaning stage



#### Files used for practice
* <b>elog_etl.practice.ipynb</b>: Jupyter notebook used to test out ideas for extracting/cleaning/storing data
* <b>elog.ipynb</b>: Jupyter notebook contains all the steps taken from extracting data to creating the model
* <b>elog_data.db</b>: Practicing writing data to database.