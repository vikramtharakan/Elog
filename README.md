# Elog
Create an NLP pipeline that categorizes Elog entries.

## Overview
The goal is to first extract the data in a json file from the Elog and import it into a workable format. Then we want to apply some sort of natural language processing algorithm on it to classify it into one of the three entry categories. <br>
Twist: The actual model created won't be able to work immediately as the data it is getting trained on is incorrectly tagged and the tags will also likely change. However the idea (initially) is to creat a backbone for a structure that can create a working model. We (as operators) will likely have to tag entries correctly for about a a long time (let's say a few months) before there will be enough data to comprehensively train this model

## Files
#### Relevant Files
<b><u>Data</u></b>
* <b>elog_etl.ipynb</b>: Jupyter notebook describing extracting/cleaning/storing the data
* <b>elog_data.db</b>: Large file (144MB) stored using git's LFS library (see https://git-lfs.github.com/). This .db file was created using the elog_etl.ipynb notebook and contains 2 tables that will be used by the notebooks in the model section to train learning algorithms.
    <ol>
        <li><u>elog_data_2011:</u> Only contains cleaned, <i>tagged</i>, entries from 2007-2011 (the range we can "trust"). Will be used to train supervised NLP model in the Models section `model.ipynb`.</li>
        <li><u>elog_all_data:</u> contain all the cleaned data from 2007 to 2018. Very Large table. This will be used to train an unsupervied model using LSA in `Unsupervised_model.ipynb`.</li>
    </ol>

<b><u>Models</u></b>
* <b>model.ipynb</b>: Jupyter notebook describing the steps taken to create the supervised NLP learning model
* <b>Unsupervised_model.ipynb</b>: Jupyter notebook describing the steps taken to create the unsupervised LSA learning model

<br>

#### Less Relevant Files
<u>Data</u>
* <b>elog_etl_practice.ipynb</b>: Notebook used practicing and experimenting during the cleaning stage


